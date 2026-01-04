---
title: "Doubling the arc of a lemniscate"
date: 2026-01-03
---

## What is done? 

In the 2026-01-01 Post, we introduced elliptic integrals of the first kind. These allowed you to compute arclengths along a lemniscate. We now start our study of elliptic integrals more seriously, by explaining Fagnano's discovery of how to *double* the arc of a lemniscate.

That is, suppose you are given an arc on the lemniscate; how does one produce the arc of exactly double the length? The analogous problem for circles is solved by the double angle trigonometric identities
$$
\sin(2\theta) = 2\sin\theta\cos\theta,
$$
$$
\cos(2\theta) = \cos^2(\theta) - \sin^2(\theta).
$$

We are following the introduction to Siegel's *Topics in Complex Function Theory.*

## Setup

For convenience, we are going to rotate our lemniscate a little bit, and consider
$$
(x^2 + y^2)^2 = 2xy,
$$
instead of the lemniscate considered last time. This has the effect of shifting the incomplete elliptic integral constant from $k=1/\sqrt{2}$ to $k=i.$ Thus our incomplete elliptic integral, giving arclengths of the lemniscate, now becomes 
$$
L(x) = \int_0^x \frac{dr}{\sqrt{1-r^4}},
$$
or equivalently
$$
L(\phi) = \int_0^{\phi} \frac{d\theta}{\sqrt{1+\sin^2\theta}}.
$$

## Fagnano's substitution

To derive the double angle identities from arclength integrals, one uses
$$
\arcsin(r) = \int_0^r \frac{dr}{\sqrt{1-r^2}}.
$$

Then one does this integral by a substitution
$$
r = \frac{2t}{1+t^2},
$$

allowing one to integrate this rationally. Fagnano decided that, since our integral has a $\sqrt{1-r^4}$ in it, we should substitute
$$
r^2 = \frac{2t^2}{1+t^4}.
$$

After some algebra, this gives
$$
\int_0^r \frac{dr}{\sqrt{1-r^4}} = \sqrt{2}\int_0^t \frac{dt}{\sqrt{1+t^4}}.
$$

Unfortunately, the final answer still has a square root in it! So, unlike the rational parametrization of the circle, we still have a tricky to integrate function in this integrand. As Siegel writes, "[this substitution] seems to offer no advantages whatsoever." 

## Fagnano's great observation

However, Fagnano realized that our substitution is actually *not* as pointless as it seems. First, make the substitution
$$
t^2 = \frac{2u^2}{1-u^4},
$$
to rewrite our integral as
$$
\sqrt{2}\int_0^t\frac{dt}{\sqrt{1+t^4}} = 2\int_0^u \frac{du}{\sqrt{1-u^4}},
$$
after a lot of algebra. But wait! This means
$$
\int_0^r \frac{dr}{\sqrt{1-r^4}} = 2\int_0^u\frac{du}{\sqrt{1-u^4}},
$$
and so to double the arc of the lemniscate ending at the radius $r,$ we just produce the arc ending at $u.$ Now we just solve for $u$ in terms of $r.$ First, note that
$$
t^2 = \frac{2u^2}{1-u^4}
$$
implies
$$t^2 \cdot (u^2)^2 + 2u^2 - t^2 = 0,$$
so that
$$
u^2 = \frac{-1 + \sqrt{t^4 + 1}}{t^2}.
$$

Similarly, 
$$
r^2 = \frac{2t^2}{1+t^4}
$$
implies 
$$
t^2 = \frac{1 - \sqrt{1 - r^4}}{r^2}.
$$
Here, we choose the sign assuming $t, r \in [0,1].$ 

Putting this all together,
$$
u^2 = \frac{r^2}{1 - \sqrt{1-r^4}} \cdot \left(-1 + \sqrt{\frac{2 - 2\sqrt{1 - r^4}}{r^4}}\right).
$$

In particular, one can construct $u$ from $r$ using only compass and straightedge! 
