# Discrete Curves

## Outline

- 2D Curves are uniquely defined by their curvature
- How do we discretize the curve
- Curvature discretization is ambiguous


## What is a Curve

Let's consider what a curve is intuitively.
If we imagine ourselves setting a pen down on paper and tracing some smooth shape, we'd be drawing a curve.
So in a sense, we can consider relate the notion of what a curve is with a function, let's call it $\gamma$, that maps between the time, $t$, since the pen was set on the paper, and the location of the pen, $p$, at that point in time.
As we increment $t$ continuously, we'll progressively know what the curve looks like.
Formally, the function $\gamma$ is intuitively dubbed the "trace" of a curve, since it traces out a curve.

There are a few issues with relation that we need to reconcile first.
First, if the function $\gamma$ has any discontinuities, our curve will also end up with discontinuities.
So we need to enfore a rule to $\gamma$ that it must be a smooth function.

<!-- constant speed requirement also takes care of kinks that don't get sussed out discontinuities in $\gamma$ -->
Second, the "speed" at which you draw a curve will change the function $\gamma$, but the curve that gets traced out remains the same.
For example, for a simple case shown, if we start drawing the curve slowly but then finish it up very quickly, it will produce the same curve if we just drew the curve with a constant speed.
A very simple way to fix this issue is to assert that the pen must move with a constant speed on the paper.
This way, when we see a curve traced out, we can guarantee that the shape of the curve being drawn is its only feature.

Lastly, the direction of the trace of the curve also matters.
That is if we reverse the motion of the pen in the opposite direction, we still draw the same curve, but the functions have the opposite argument sign.
For now we can avoid dealing with this issue by simply saying that the curves we are considering also require a direction.
In other words, we can imagine every curve we draw also requires a direction to be specified.

Now if we incorporate all the constraints we've so far mentioned, namely that:
- The function $\gamma$ used for tracing the curve must be smooth
- The speed at which the curve is traced is constant
- We consider a curve with the same shape but different directions as different curves
we have a pretty decent working method for representing curves.

This method is called the *arc-length parameterized trace* of a curve, referring to the notion that the parameter used to trace the curve depends on the length of the curve that is being traced.

## Qualities of a Curve

For the scope of this video, we'll only be focusing on 2D curves, but many of the concepts we discuss also transfer over to the 3-dimensional case.

The properties of the function $\gamma$ provides lots of insight into the properties of the curve.
To make the intuition of the next section easier, let's move away from the analogy of $\gamma$ providing the position of a pen tip, but instead let's consider a car driving along a windy road.
In this analogy, the road is the curve that we are interested in, and the car is simply following wherever the curve leads it.

In this setup, the position of the car at any point in time $t$ is at $\gamma(t)$.
Then, the velocity of the car $v$ is equal to the rate of change of the position of the car, or,

$$
v = \frac{d \gamma(t)}{dt}
$$

But we already know one fact about $v$!
It's length is equal to 1 due to the constraint we set on what types of $\gamma$ functions we are allowed to choose.
So in fact, the velocity vector we found above 