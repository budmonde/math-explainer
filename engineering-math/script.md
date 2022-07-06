# The Engineering of Mathematics: How the design of math formulas bias our understanding

## Introduction

One of the most interesting and ____ features of mathematics is that many of the discoveries we've made in the past few millenia hold true even if humans never existed.
Discoveries such as the value of pi and the pattern of prime numbers could just as easily be discovered by some alien species, and their discoveries would match ours.
It's worth emphasizing that this is not true for other fields of science.
The design of a car engine, might look wildly different from what we're used to seeing if they were invented by aliens.
Heck, the idea of a car itself might not be applicable to some hypothetical civilization far far away.

Nevertheless, what ideas in math we choose to explore, and how we choose to express them has very strong implications on the results that we draw from them.
Consider Pythagoras' Theorem.
Around the time various civilizations discovered this key identity about the geometry of right triangles, the agricultural revolution was in full force, and hence the ability to measure distances on a flat surface must've been an important problem to solve.
<Find some citation about how for a specific civilization these discoveries were made by the people of the occupation of interest: farming planners etc>
As such, our sociatal biases indeed have a strong influence on how we engineer our math formulas, and decide what we can and can't do with them.

The effects of how we engineer our math formulas to suit our needs doesn't just show up in one-off simple examples such as the Pythagoras' Theorem.
Modern day mathematicians engineer mathematics on a daily basis, and have come up with many "mathematical inventions" that help solve the problems they run into.
In this video, I will be showcasing one such example in the context of the geometry of curves and explore what types of challenges we run into.
But before we hop into the engineering bits, let's first cover two pieces of genuine geometric discoveries that will be highly relevant to our main topic.

## Background

A curve is a squiggly line that you might imagine drawing with a pen on a piece of paper.
Formally, we might define it as a function "gamma", of time, where at any given time, the function gives us the "x" and "y" position of the pen on the paper.
And also let's say that the pen completes any curve in exactly 1 second of time.
So to draw the curve, we just evaluate the function at all times between 0, and 1.

Let's study the properties of this curve.
How curvy is it?
Where is it the **most** curvy?
Is this curve different than this other curve?

The function we used to represent the curve can help us answer these questions in a measurable and quantifiable way.
So let's try to analyze the function "gamma" and see what we can come up with.
The function "gamma" encodes the position of the pen at any time t.
So if we take the time derivative of the pen position, we will find its velocity.
So the derivative of gamma with respect to t is the velocity function, v.

At this point, you might spot a problem with our decision to represent a curve using any arbitrary function that traces the path of the curve.
There are an infinite possible functions that will trace out this curve.
For example, there might be a function that keeps the pen in place for the first 0.5s, and then accelerates for 0.1s, and decelerates to a stop over the last 0.4s.
Meanwhile, another function might complete the trace of the curve in 0.1s, return to the starting position in the next 0.1s, and so on 5 times over.

Let's address these issues by forcing the pen to always go at a constant speed throughout the entire 1 second duration.
The pen will still accelerate to change the direction of the pen's movement, but it will never change the speed at which the pen progresses.
This requirement allows us to weed out all the oddly behaving functions.

The last problem that this solution doesn't solve is the fact that there are two functions that fit the description for each curve.
One that goes from point A to point B, and another from point B to point A.
This is still an accomplishment since we've reduced the number of unique functions that map to the same curve down to two from infinity.
In the scope of our work, let's just say that these two curves are different.
So in essense, we are studying "directed curves", because each curve has a direction.

So now with this modification, the derivative of gamme with respect to t will produce a velocity function, v, but this time the magnitude of the velocity remains constant!
In this animation, you can see that the velocity vector moves across the curve, only changing its direction in the process.

The change
