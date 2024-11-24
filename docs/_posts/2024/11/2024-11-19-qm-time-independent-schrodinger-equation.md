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

## The free particle
$V(x) = 0$, the general solution is

$$\begin{align}\Psi(x, t) &= \frac{1}{\sqrt{2 \pi}} \int_{\infty}^{\infty} \psi(k) e^{i \left(kx - \frac{\hbar k^2}{2m}t\right)}dk \\ \psi(k) &= \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{+\infty}\Psi(x, 0)e^{-ikx}dx\end{align}$$

## The delta function potential
$E < V(-\infty) \& V(+\infty)$ Then bound state, otherwise scattering state

For given potential $V(x) = -\alpha \delta(x)$, $E<0$ (bound states)

$$\psi(x) = \frac{\sqrt{m\alpha}}{\hbar} e^{-m\alpha|x|/\hbar^2}, E=-\frac{m\alpha^2}{2\hbar^2}$$

$E>0$ (scattering states)

$$\begin{align}\psi(x)&=Ae^{ikx}+Be^{-ikx}(x<0) \\ &=Fe^{ikx}(x>0)\end{align}$$

with

$$B=\frac{i\beta}{1-i\beta}A, F=\frac{1}{1-i\beta}A, \beta=\frac{m\alpha}{\hbar^2 k}$$

and

$$\begin{align}R&=\frac{|B|^2}{|A|^2} = \frac{1}{1+\left(2\hbar^2 E/m \alpha^2 \right)^2} \\ T&=\frac{|F|^2}{|A|^2} = \frac{1}{1+\left( m\alpha^2 / 2\hbar^2 E \right)} \end{align}$$

$R$ is reflection coefficient, $T$ is transmission coefficient.

## The finite square well

$$V(X) = -V_0 (|x| < a), 0 (|x| > a)$$
