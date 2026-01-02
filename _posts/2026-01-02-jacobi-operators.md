---
title: "A cute theorem of Jacobi"
date: 2026-01-02
---

## What is done?

Yesterday, Fatima, Sunny, and I were reading about moment problems, and we came across the notion of *Jacobi operators*. Today I will write about a theorem of Jacobi, showing how every matrix is congruent to a *tridiagonal* matrix (only nonzero entries on the diagonal, immediately above the diagonal, or immediately below the diagonal). 

## Jacobi normal form

We start with a certain normal form theorem. Recall that two matrices $A, B$ are *congruent* if there is a matrix $P$ such that $P^{\intercal}AP = B.$ This notion of course comes from the theory of quadratic forms. 

Jacobi proved 

> **Theorem (Jacobi Normal Form).** Let $M$ be a (square) symmetric matrix with coefficients in a field $k.$
> Then $M$ is congruent to a *tridiagonal matrix* -- that is, a matrix whose only nonzero entries are on the diagonal, or on entries immediately above or below the diagonal.

Let's see how. 

> **Remark**. The tridiagonal matrix congruent to $M$ is necessarily also symmetric, since symmetry is stable under congruence.
> **Remark**. While I will not prove it here, using the standard tricks employed in the proof of Smith normal form, one can allow $k$ to be a PID instead of just a field.

## The proof of Jacobi's theorem

We will explain the proof for $3\times 3$ matrices, since in general the proof is only notationally more complicated. Write our symmetric matrix as
$$ 
M = \begin{pmatrix} a & x & y \\ x & b & z \\ y & z & c \end{pmatrix}.
$$

Our goal: get rid of $y.$ I find this easier to understand when we work with quadratic forms, so look at the associated quadratic form
$$
aX^2 + bY^2 + cZ^2 + 2xXY + 2yYZ + 2zZX.
$$

We are trying to kill the $YZ$ term. For this quadratic form manipulation to be valid, let me also assume that the characteristic is not 2. 

If $b \neq 0,$ we can subtitute $Y' = Y - \frac{y}{b}Z$ to kill this $YZ$ term. If $c \neq 0,$ similarly we can do a substitution involving $Z.$

When $x \neq 0,$ we can substitute $X' = X - \frac{y}{x}Z$ to use the $XY$ term to kill the $YZ$ term. A similar trick works when $z \neq 0.$

Assume now that $b=c=x=z=0.$ Then our quadratic form is just $aX^2 + 2yYZ.$ When $a \neq 0,$ we substitute $X' = X + Y - \frac{y}{a}Z$ to kill this $YZ$ term. 

Finally, when $a = 0$ as well, we just swap $X$ and $Y$ to kill the $YZ$ term. After this work, we conclude.
