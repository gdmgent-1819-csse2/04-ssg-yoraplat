---
layout: page
title: Opdracht 2
permalink: /opdracht2/
---

### Adding the clock

Use the vectors to create a clock
~~~~
const time = new Date()

        console.log((time.getHoursVector() * -30) - time.getMinutesVector()/2)


        for(let i = 0; i < 0.45; i+=0.0001) {
            const secondsVector = new Vector2(0, i)
            secondsVector.rotateVector(time.getSeconds() * -6)
            this.properties.positions.push(secondsVector.x, secondsVector.y)
            this.properties.colors.push(...this.colors.white) 

            if(i <= 0.35) {
                const minutesVector = new Vector2(0, i)
                minutesVector.rotateVector(time.getMinutes() * -6)
                this.properties.positions.push(minutesVector.x, minutesVector.y)
                this.properties.colors.push(this.colors.white)
            }


            if(i <= 0.15) {
                const hoursVector = new Vector2(0, i)
                hoursVector.rotateVector((time.getHours() * -30) - time.getMinutes()/2)
                this.properties.positions.push(hoursVector.x, hoursVector.y)
                this.properties.colors.push(this.colors.white)
            }
        }

        for(let i = 0; i < 360; i++) {
            v.rotateVector(1)
            this.properties.positions.push(v.x, v.y)
            this.properties.colors.push(...this.colors['green'])
        }

        this.drawScene()
~~~~
[jekyll-organization]: https://github.com/jekyll
