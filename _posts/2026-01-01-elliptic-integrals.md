---
title: "Elliptic integrals of the first kind"
date: 2026-01-01
---

## What is done? 

test code 8

It is a shame that I don't know more about elliptic functions, so I am going to try and learn a few more things about them. To start, today I am going to say a few things about the arclengths of *lemniscates*.

## The lemniscate

Recall that the *lemniscate*, a figure-eight looking shape, has equation
\[
(x^2 + y^2)^2 = 2(x^2 - y^2).
\]

Geometrically, we can describe it as the locus of points \(P\) such that the *product* of the distance from \( P \) to \((-1, 0)\) with the distance from $P$ to \((1, 0)\) is equal to \(1.\) 

In polar coordinates, the lemniscate has a relatively simple expression. Fix an angle \(\theta.\) The point \((r, \theta)\) lies on our lemniscate if and only if 
\[
r^4 = 2r^2(\cos^2\theta - \sin^2\theta),
\]
or equivalently if
\[
r = \sqrt{\cos(2\theta)}.
\]

This let's us get a simple expression for the arclength, as in polar coordinates arclengths are given by
\[
L = \int_{\alpha}^{\beta} \sqrt{r^2 + \dot{r}^2} \, d\theta.
\]

We have
\[
\dot{r} = -\sin(2\theta) \cdot (\cos(2\theta))^{-1/2},
\]
so that
\[
L = \int_{\alpha}^{\beta} \sqrt{\cos(2\theta) + \sin^2(2\theta) \cdot (\cos(2\theta))^{-1}} \, d\theta.
\] 

We can simplify this a little bit. The term under the square root is just
\[
\frac{\cos^2(2\theta) + \sin^2(\theta)}{\cos(2\theta)} = \frac{1}{\cos(2\theta)},
\]
so that our arclength integral is just
\[
L = \int_{\alpha}^{\beta} \frac{d\theta}{\sqrt{1 - \frac{1}{2}\sin^2(\theta)}},
\]
where we use the double angle identity for cosine in the last step. 

## The elliptic integral of the first kind

This integral \(L\) is an instance of an *incomplete elliptic integral of the first kind*, usually defined as 
\[
F(\phi, k) := \int_0^{\phi} \frac{d\theta}{\sqrt{1 - k^2\sin^2\theta}}.
\]
This parameter \(k\) is often called the *elliptic modulus*, and our lemniscate has \(k = 1/\sqrt{2},\) a rather special value. 

## How do elliptic curves get into it? 

To end this discussion of elliptic integrals of the first kind, we explain how elliptic curves get into it. If we change variables 
\[
t = \sin(\theta), x = \sin(\phi),
\]
then we can rewrite \(F(\phi, k)\) as follows. 

Note that
\[
dt = \cos(\theta) \, d\theta,
\]
and so our integrand becomes
\[
\frac{dt}{\cos(\theta)} \cdot \frac{1}{\sqrt{(1-k^2\sin^2\theta}} = \frac{dt}{\sqrt{(1-t^2)(1-k^2t^2)}},
\]
so that
\[
F(\phi, k) = \int_0^x \frac{dt}{\sqrt{(1-t^2)(1-k^2t^2)}},
\]
from which we see the relevance to elliptic curves.
