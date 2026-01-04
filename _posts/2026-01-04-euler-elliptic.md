---
title: "Euler's angle addition, part 1"
date: 2026-01-04
---

## What is done? 

Last time, we made an analogy between the lemniscatic integral and the arcsine function. Today, we go slowly through the first part of Euler's paper "De integratione aequationis differentialis $(m dx)/\sqrt{1-x^4} = (n dy)/\sqrt{1-y^4}$". See [here](https://scholarlycommons.pacific.edu/euler-works/251/) for a link. 

## Euler's differential equation

Euler recast Fagnano's arc doubling as solving the following problem: Fagnano solved the differential equation
$$
\frac{dx}{\sqrt{1-x^4}} = \frac{2dy}{\sqrt{1-y^4}}.
$$

Let's start by understanding why this is. 

Let $x$ be the independent variable, and $y$ the independent variable. If $y(x)$ obeys Euler's ODE, then in the lemniscatic integral
$$
\int_0^x \frac{dx}{\sqrt{1-x^4}},
$$
if we substitute $y=y(x),$ we get
$$
\int_0^x \frac{dx}{\sqrt{1-x^4}} = 2\int_0^y \frac{dy}{\sqrt{1-y^4}}.
$$

## Euler's solutions

To begin, Euler will solve
$$
\frac{dx}{\sqrt{1-x^4}} = \frac{dy}{\sqrt{1-y^4}}.
$$

Of course $y=x$ is one solution, but Euler desired the *complete* solution, which should involve one constant of integration. Euler also "divined," as he put it, that
$$
x = -\sqrt{\frac{1-y^2}{1+y^2}}
$$
is another solution, as then
$$
dx = \frac{2y dy}{x(1+y^2)^2}
$$
and
$$
\sqrt{1-x^4} = \frac{2y}{1+y^2},$$
so that
$$
\frac{dx}{\sqrt{1-x^4}} = \frac{dy}{x(1+y^2)} = \frac{dy}{\sqrt{1-y^4}}.
$$

So now Euler has two solutions to this equation; this allowed him to guess the general solution. Note that our nontrivial solution can be rephrased as saying
$$
x^2 = \frac{1-y^2}{1+y^2},
$$
or 
$$
x^2 + y^2 + x^2y^2 = 1.
$$

Euler then guessed that the general solution is 
$$
x^2 + y^2 + C^2x^2y^2 = C^2 + 2xy\sqrt{1-C^4},
$$
or in other words
$$
x = \frac{C\sqrt{1-y^4} + y\sqrt{1-C^4}}{1+C^2y^2}.
$$

The solution $x = y$ corresponds to $C = 0.$ Siegel, again in *Topics in Complex Function Theory,* explains (in the first few pages of volume 1) how Euler might have derived such an identity using the same substitutions that Fagnano made, but it seems that probably Euler was telling the truth in his Latin paper: he observed the nontrivial solution, then thought very hard about how to make a simple 1-parameter family of solutions. 
