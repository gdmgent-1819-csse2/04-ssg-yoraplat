---
layout: page
title: Opdracht 1
permalink: /opdracht1/
---
# Vector classes

To create vectors you have to import them from the library.
Then declare a new constant as the vector you want to use.

~~~~
const v1 = new Vector2(10, 41);
const v2 = new Vector2(14, 40);
~~~~

To use the different functions you wrote:

~~~~
v1.add(v2)
~~~~
This will add your two vectors together. To subtract two vectors use:
~~~~
v1.sub(v2)
~~~~

To see the result of the calculations, simply use console.log() to log the results.
~~~~
console.log(v1.add(v2));
console.log(v1.sub(v2));
~~~~

~~~~
constructor() {
    console.log("Vector 2");
        const v1 = new Vector2(10, 41);
        const v2 = new Vector2(14, 40);
        console.log("Add: v1 + v2 ");
        console.log(v1.add(v2));
        console.log("Sub: v1 - v2 ");
        console.log(v1.sub(v2));
        console.log("scale: v1 * ");
        console.log(v1.scalar(2));
        console.log("Norm: Length of vector");
        console.log(v1.norm());
        console.log("Dot Product");
        console.log(v1.dotProduct(v2));
}
~~~~

[jekyll-organization]: https://github.com/jekyll
