---
layout: default
title: QM - 2. Time Independent Schrodinger Equation
date: 2024-11-19 12:23 +0900
tag: QM
---

# Time Independent Schrodinger Equation

## Stationary states
Solving by the method of separation of variables $\Psi (x, t) = \psi(x) \phi(t)$

$$\begin{align}\phi(t) &= e^{-iEt/\hbar} \\ -\frac{h^2}{2m}\frac{d^2 \phi}{d x^2} + V\Phi &= E\Phi\end{align}$$

Separable solutions have meaningfull

1. They are stationary state.
2. They are states of definite total energy called by Hamiltonian.
3. The general solution is a linear combination of separable solutions.

$$\Psi(x, t) = \sum_{n=1}^{\infty} c_n \psi_n (x)e^{-iE_n t/\hbar}$$

$\left\| c_n \right\|^2 $ is the probability that $E_n$ is measured

$$ \begin{align}\sum_{n=1}^{\infty} \left|c_n\right|^2 &= 1 \\ \left< H \right> &= \sum_{n=1}^{\infty} \left| c_n \right|^2 E_n \end{align}$$

## The harmonic Oscillator
Potential energy is $V(x) = \frac{1}{2}kx^2$.
Any potential is approximately parabolic in the neighborhood of a local minimum.

Let's define Ladder operator as,

$$\hat{a}_\pm = \frac{1}{\sqrt{2\hbar m \omega}} \left(\mp i\hat{p} + m\omega x \right)$$

Commutate - 

$$\begin{align}\left[ x, \hat{p} \right] &= i\hbar \\ \left[\hat{a}_{-} , \hat{a}_{+} \right] &= 1\end{align}$$

The solution for this equation

$$\begin{align}\psi_0 (x) &= \left( \frac{m\omega}{\pi\hbar} \right)^{1/4} e^{-\frac{mw}{2\hbar}x^2} \\ \psi_n (x) &= \frac{1}{\sqrt{n!}} \left(\hat{a}_{+} \right)^n \psi_0 (x) \end{align}$$
