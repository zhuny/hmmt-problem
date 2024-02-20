---
layout: default
title: continued fraction of e
date: 2024-01-19 01:57 +0900
---

# e
자연상수의 (simple) continued fraction은 다음의 형태로 알려져 있습니다.

$$e = 2+\cfrac{1}{1+\cfrac{1}{2+\cfrac{1}{1+\cfrac{1}{1+\cfrac{1}{4+\cfrac{1}{1+\cfrac{1}{...}}}}}}}$$

앞쪽의 상수만 나열해 보자면, 1, 2, 1, 1, 4, 1, ... 즉, 3개의 항 $1, 2n, 1$가 규칙적으로 진행되는 형태입니다.
왜 이런 규칙적인 형태가 되었는지에 대해서 알아보겠습니다.

# Gauss's continued fraction
## 점화식
다음의 점화식이 있다고 생각해 보겠습니다.

$$f_{i-1} - f_{i} = \alpha_i f_{i+1}$$

그러면 $f_i / f_{i-1}$을 다음과 같이 나타낼 수 있습니다.

$$\cfrac{ {f}_{i}}{ {f}_{i-1}}=\cfrac{1}{1+{\alpha}_{i}\cfrac{ {f}_{i+1}}{ {f}_{i}}}$$

점화식이기 때문에 안에 있는 식을 계속 대입시키면...

$$\cfrac{ {f}_{i}}{ {f}_{i-1}}=\cfrac{1}{1+\cfrac{ {\alpha}_{i}}{1+\cfrac{ {\alpha}_{i+1}}{...}}}$$

가 됩니다. 이제 $e$를 계산하기 위한 적절한 $f_i$와 $\alpha_i$를 찾으면 됩니다.

## Series

$g_{a, b}$를 다음과 같이 정의하도록 하겠습니다.

$$ g_{a, b} = \frac{(b-1)!}{(a-1)!}\sum_{i=0}^{\infty}\frac{(a+i-1)!}{(b+i-1)!i!}(-1)^i$$

이 함수에 대해서 다음 두 식을 얻을 수 있습니다.

$$\begin{align}{g}_{a,b}-{g}_{a,b+1}&=\cfrac{(b-1)!}{(a-1)!}\sum_{i=0}^{\infty}\left(\cfrac{(a+i-1)!}{(b+i-1)!i!}-\cfrac{(a+i-1)!}{(b+i)!i!}\right){(-1)}^{i}\\&=\cfrac{(b-1)!}{(a-1)!}\sum_{i=0}^{\infty}\cfrac{(a+i-1)!}{(b+i-1)!i!}\cfrac{i}{b+i}{(-1)}^{i}\\&=\cfrac{(b-1)!}{(a-1)!}\sum_{i=1}^{\infty}\cfrac{(a+i-1)!}{(b+i)!(i-1)!}{(-1)}^{i}\\&=\cfrac{(b-1)!}{(a-1)!}\sum_{i=0}^{\infty}\cfrac{(a+i)!}{(b+i+1)!i!}{(-1)}^{i}\\&=\cfrac{-a}{b(b+1)}{g}_{a+1,b+2}\end{align}$$

또 다른 식으로는,

$$\begin{align}{g}_{a,b}-{g}_{a+1,b+1}&=\cfrac{(b-1)!}{(a-1)!}\sum_{i=0}^{\infty}\left(\cfrac{(a+i-1)!}{(b+i-1)!i!}-\cfrac{b(a+i)!}{a(b+i)!i!}\right){(-1)}^{i}\\&=\cfrac{(b-1)!}{(a-1)!}\sum_{i=0}^{\infty}\cfrac{(a+i-1)!}{(b+i-1)!i!}\cfrac{(a-b)i}{a(b+i)}{(-1)}^{i}\\&=\cfrac{(a-b)(b-1)!}{a!}\sum_{i=1}^{\infty}\cfrac{(a+i-1)!}{(b+i)!(i-1)!}{(-1)}^{i}\\&=\cfrac{(b-a)(b-1)!}{a!}\sum_{i=0}^{\infty}\cfrac{(a+i)!}{(b+i+1)!i!}{(-1)}^{i}\\&=\cfrac{b-a}{b(b+1)}{g}_{a+1,b+2}\end{align}$$

이제, $f_{2k} = g_{k+1, 2k+1}$이라 하고, $f_{2k+1} = g_{k+1, 2k+1}$이라 해 보겠습니다. 그러면,

$$\begin{align}{f}_{2k}-{f}_{2k+1}&={g}_{k+1,2k+1}-{g}_{k+1,2k+2}\\&=\cfrac{-k-1}{(2k+1)(2k+2)}{g}_{k+2,2k+3}\\&=\cfrac{-{f}_{2k+2}}{2(2k+1)}\end{align}$$

$$\begin{align}{f}_{2k+1}-{f}_{2k+2}&={g}_{k+1,2k+2}-{g}_{k+2,2k+2}\\&=\cfrac{k+1}{(2k+2)(2k+3)}{g}_{k+2,2k+4}\\&=\cfrac{ {f}_{2k+3}}{2(2k+3)}\end{align}$$

가 됩니다.

그러면, 여기서 $\alpha_{i}$의 값을 보면

$$\begin{align}{\alpha}_{2k+1}&=-\cfrac{1}{2(2k+1)}\end{align}$$ 

$$\begin{align}{\alpha}_{2k+2}&=\cfrac{1}{2(2k+3)}\end{align}$$ 

가 됩니다.

## Fraction
여기서 fraction을 계산하기 위해 다음 식을 보도록 하겠습니다.

$$(2k+1)\left(1+\cfrac{\cfrac{-1}{2(2k+1)}}{1+\cfrac{\cfrac{1}{2(2k+3)}}{A}}\right)$$

이 식을 정리하면,

$$2k+\cfrac{1}{1+\cfrac{1}{1+\cfrac{1}{(2k+3)A}}}$$

가 되어 재귀적으로 대입해 나갈 수 있습니다.

## Last part
여기서 $f_0 = g_{1, 1} = 1/e$이고, $f_1 = g_{1, 2} = 1 - 1/e$입니다. 먼저,

$$\begin{align}\cfrac{ {f}_{1}}{ {f}_{0}}&=\cfrac{1-\cfrac{1}{e}}{\cfrac{1}{e}}\\&=e-1\end{align}$$

입니다. 점화식 내용을 가져오면,

$$\begin{align}\cfrac{ {f}_{1}}{ {f}_{0}}&=\cfrac{1}{1+\cfrac{-1/2}{1+\cfrac{1/6}{...}}}\\&=1+\cfrac{1}{1+\cfrac{1}{3\times\left(1+\cfrac{-1/6}{1+\cfrac{1/10}{...}}\right)}}\end{align}$$

입니다. 가장 분모의 구간은 계속해서 재귀적으로 정의되어 우리가 아는 식이 됩니다.
위 두 식을 정리해서 e의 값을 계산해 보면,

$$\begin{align}e&=2+\cfrac{1}{1+\cfrac{1}{2+\cfrac{1}{1+\cfrac{1}{1+\cfrac{1}{4+...}}}}}\end{align}$$

가 됩니다.
