---
layout: default
title: sylow theorems
date: 2024-01-14 00:42 +0900
---

# Sylow theorem
Finite group $G$에 대해서, 그 order가 $p^a m$이라고 하자.
여기서 $m$은 $p$로 나뉘지 않는다.

1. Sylow $p$-subgroup이 항상 존재한다. 즉, order가 $p^a$인 subgroup이 항상 존재한다.
2. 모든 Sylow $p$-subgroup은 서로 conjugate 하다.
3. Sylow $p$-subgroup의 수를 $n_p$라고 했을 때, $n_p = 1 \mod p$이다. 또한, $n_p \| m$이다.

# Application
## Group of order $pq$
여기서 $2 \lt p \lt q$라 하자.
Sylow theorem에 의해, P, Q를 각각 Sylow $p$, $q$-subgroup 이라고 하자.
둘 다 order가 소수이기 때문에 cyclic group이다.

그 갯수 $n_q$는 $p$의 약수이며, $q$로 나눈 나머지가 1이다.
그런데, $p$의 약수는 $p$와 1 뿐이고, 이 중에서 $q$로 나눈 나머지가 1인 것은 1 뿐이다.
즉 Sylow $q$-subgroup은 유일하며 Q는 normal subgroup이 된다.

Case 1. 만약, $q \neq 1 \mod p$라 했을 때, $n_p$가 될 수 있는 값은 1 뿐이다.
$q$의 약수 중, $p$로 나눈 나머지가 1이 되는 값은 1 뿐이기 때문이다.
즉, Sylow $p$-subgroup 역시 유일하며, P가 normal subgroup이다.
$P$와 $Q$ 둘 다 normal subgroup이기 때문에, 둘은 commute하고 cyclic group이 유일하다.

Case 2. $q = 1 \mod p$ 이 경우에는 $n_p = q$일 가능성이 생긴다.
이 때에는 $P$와 $Q$의 semi-direct도 가능하다.

### Group of order 21
21은 3과 7의 곱이며, 7은 3으로 나눈 나머지가 1이다.
이 때에는 2개의 Group이 존재하며, 하나는 cyclic group이다.

또 다른 하나는,
$G = \left\lt a, b \| a^3 = b^7 = 1, aba^{-1} = b^2 \right\gt$ 이다.

## Group of order 30
$n_3$은 10의 약수면서 3으로 나눈 나머지가 1이므로, 가능한 수는 1과 10이다.
$n_5$은 6의 약수면서 5로 나눈 나머지가 1이므로, 가능한 수는 1과 6이다.

Order가 30인 group이 simple하다고 가정했을 때, $n_3$과 $n_5$는 모두 1이 될 수 없다.
1이 된다는 것은 해당 Sylow subgroup 이 normal subgroup이 된다는 것이기 때문에 simple이라는 가정에 위배된다.

그러면 $n_3 = 10$이 되며, order가 3인 element는 총 (3-1)*10=20개가 된다.
$n_5 = 6$이므로, order가 5인 element는 (5-1)*6=24개가 된다.
그러면 갯수의 합이 30개를 넘어서므로, $n_3$이나 $n_5$ 중 하나는 반드시 1이 되어야 하고
normal subgroup은 항상 존재한다. 즉, simple group이 아니다.
