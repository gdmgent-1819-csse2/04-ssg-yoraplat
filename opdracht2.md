---
layout: page
title: Opdracht 2
permalink: /opdracht2/
---

### Adding the clock

Use the vectors to create a clock.

To make your clock update every second use:
~~~~
window.addEventListener('canvasUpdate', event => {
       setInterval(() => {
           this.canvasUpdateHandler(event)
       }, 1000)
       // 1000ms = 1s
   }, false);
~~~~

To add the middlepoint of your clock use:
~~~~
this.data.positions.push(0, 0)
this.data.colors.push(...this.colors.white)
~~~~

To create the clock itself use:
~~~~
const now = new Date()
const second = now.getSeconds();
const minute = now.getMinutes();
const hour = now.getHours();
const time = `${hour} : ${minute} : ${second}`
document.getElementById('watch').innerHTML = time
~~~~

Define the clock pointers:
~~~~
// Draw clock pointers
const seconds = new Vector2(0, .4)
seconds.rot(-6 * now.getSeconds())

// Draw Seconds pointer
console.log(+ now.getSeconds() * -6)
this.data.positions.push(seconds.x, seconds.y)
this.data.colors.push(...this.colors['yellow'])
            
// Draw Minutes pointer
const minutes = new Vector2(0, .5)
minutes.rot(now.getMinutes() * -6)
this.data.positions.push(minutes.x, minutes.y)
this.data.colors.push(...this.colors['white'])
            
// Draw Hours pointer
const hours = new Vector2(0, .35)
hours.rot(now.getHours() * -6)
this.data.positions.push(hours.x, hours.y)
this.data.colors.push(...this.colors['magenta'])
console.log(this.data.positions)  
~~~~

This will draw all the clock pixels inside the canvas:
~~~~
this.drawScene()
~~~~