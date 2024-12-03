---
layout: default
title: Elliptic Curve And Cryptography
date: 2024-11-27 23:08 +0900
tags: Elliptic Curve
---

타원 곡선과 암호

# Elliptic Curve and Cryptography
## Elliptic Curve
어떤 Field $F$가 주어졌을 때, 다음을 만족시키는 점들의 집합을 타원 곡선이라 한다.

$$\begin{align}y^2 = x^3 + ax + b \\ a, b \in F, (x, y) \in F^2\end{align}$$

여기서는 Field는 finite로 제한한다. 즉, 원소의 field의 원소의 갯수는 $p^n$.

## Cryptography
이런 Group Theory의 경우에는 discrete logarithm을 기반으로 한 알고리즘이 주로 설계됩니다.
가장 좋은 예가 RSA입니다. 어떤 두 소수의 곱인 $N$을 공개하고 두 소수는 공개하지 않음으로써
어떤 문장을 암호화하기는 쉽지만, 복호화하기는 쉽지 않도록 합니다.
어떤 자연수 $s$를 공개 암호키로 사용하여 문장을 제곱($x^s$)하여 암호화합니다.
$x^s$ 값이 있다고 해도 $x$를 쉽게 알 수 없다는 점을 이용하는 것이 discrete logarithm입니다.

## Domain Parameters
타원 곡선을 통해 암호화를 할 때에도 discrete logarithm 기반입니다.
어떤 타원 곡선 위의 한 점을 공개적으로 사용할 때, 서로 각자가 정한 자연수제곱을 한 값을 서로
교환하여 하나의 symmetric-key를 생성합니다.

그런데 여기서 암호를 구축하기 위해서 타원 곡선 위의 한 점과, 타원 곡선의 order를 알아야 합니다.
실질적으로 field의 order가 굉장히 크기 때문에 brute force를 할 수도 없습니다.

## Schoof's algorithm
Schoof's algorithm을 이용해서 field의 order를 빠르게 구할 수 있습니다.

### Hasse's theorem
Field $\mathbb{F}_q$에 대해서, elliptic curve의 order $E$는 다음 식을 만족합니다.

$$\left| q+1-E \right| \le 2 \sqrt{q}$$

어떤 큰 $N \gt 4\sqrt{q}$에 대해서, 위 식의 왼쪽을 $t$라 두고 $t \mod N$을 구한다.
다만 이것만으로는 매리트가 없으며 $N$을 여러개의 서로다른 소수들의 곱으로 나타내서 작은 값에 대해서 계산해준다.
그 다음 CRT를 이용해 $t \mod N$를 구할 수 있다.
