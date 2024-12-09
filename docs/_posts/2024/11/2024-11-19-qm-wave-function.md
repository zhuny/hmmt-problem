---
layout: default
title: QM - 1. Wave Function
date: 2024-11-19 11:58 +0900
tag: QM
---

# Wave Function

## Schrodinger equation
Particles' wave function, $\Psi(x, t)$, by solving Schrodinger equation

$$i\hbar \frac{\partial\Psi}{\partial t} = - \frac{\hbar^2}{2m} \frac{\partial^2 \Psi}{\partial x^2} + V \Psi$$

## Normalization
$\left\| \Psi(x, t) \right\|^2$ is the probability density.

$$\int_{-\infty}^{+\infty} \left| \Psi(x, t) \right|^2 dx = 1$$

## Momentum
Average position and momentum

$$\left< x \right> = \int_{-\infty}^{+\infty} x \left | \Psi(x, t) \right |^2 dx$$

$$\left< p \right> = m \frac{d \left< x \right>}{dt} = -i\hbar \int \left( \Psi^* \frac{\partial \Psi}{\partial x} \right)dx$$

As operator

$$\left< Q(x, p) \right> = \int \Psi^* \left[ Q\left(x, -i\hbar \frac{\partial}{\partial x}\right) \right]\Psi dx$$

## The uncertainty principle

$$\sigma_x\sigma_p \ge \frac{\hbar}{2}$$
