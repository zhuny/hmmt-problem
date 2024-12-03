---
layout: default
title: POW 2024 02, Well-mixed permutation
date: 2024-12-03 20:25 +0900
tags: POW
---

[Ref](https://mathsci.kaist.ac.kr/pow/2024/2024-02-well-mixed-permutations/)

# POW
## Problem
A permutation $\phi \in S_n$ is called a well-mixed if $\phi([k]) \ne [k]$ for each $1 \le k < n$. How many well-mixed permutation for $n=15$

## Answer - Idea Sketch
Any permutation $\phi$에 대해서, $\Psi : S_n \rightarrow P([n])$를 $\Psi(\phi) = \left \\{ k : \phi([k]) = [k] \right \\}$ 라 하자.
$\Psi$의 함수값은 문제 조건에 따라 항상 $n$을 포함하고 있다.
우리의 목적은 $\Psi^{-1}(\\{n\\})$를 구하는 것이다.

특정 값에 대해서 inverse를 구하기는 쉽지 않지만, 한가지 아는 사실이 있다.
어떤 $[n]$의 subset $A = \\{a_1, a_1+a_2, ... , a_1+a_2+...+a_i=n\\}$에 대해서
$A \subseteq \Psi(\phi)$인 $\phi$의 수의 합은 $\prod a_j !$과 같다는 것이다.

