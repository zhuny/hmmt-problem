---
layout: default
title: Cartoon Reading Sequence
date: 2024-03-07 21:07 +0900
tags: CodingTest
---

# 문제
이제는 웹툰이 대중화 되어 있어서,
정해진 너비 내에서 공간의 제약 없이 스크롤을 내리면서 읽어 내려 갈 수 있습니다.
하지만, 웹툰과 달리 만화의 경우는 사정이 다릅니다.
제약된 종이 공간 내에서 컷을 배치해야 하는 어려움이 있습니다.

컷은 줄글을 읽는 것과 똑같은 순서로 읽습니다.
먼저 왼쪽부터 오른쪽 순으로 읽고, 더 이상 오른쪽으로 갈 수 없는 경우 위에서 아래로 읽습니다.
여기서는 컷과 종이 모두 직사각형이라 가정합니다.

![CRS1](/assets/img/codingtest/CartoonReadingSequence1.png)

위의 예시를 보면 1, 2, 3, 4 순으로 읽는데, 가장 먼저 봐야 할 컷은 좌상단에 있는 1번입니다.
1 다음에 오른쪽에 있는 컷은 3이지만, 3의 세로 길이가 1과 2를 합한 길이와 같아서 1 다음 3을 읽기 전에 2를 읽어야 합니다.
그리고 1, 2, 3을 읽은 뒤 아래 있는 4번을 읽습니다.

![CRS2](/assets/img/codingtest/CartoonReadingSequence2.png)

이 경우는 제대로 된 배치가 아닙니다.
1을 읽은 다음 3을 읽으려고 보니 세로 길이가 더 길어서 1 밑에 있는 컷들을 읽어야 합니다.
그래서 2와 4를 읽고 나니 다음 컷으로 5번을 읽을 수도 3을 읽을 수도 없기 때문입니다.

이럴 때, 어떤 컷부터 읽어야 하는지 순서를 나타내는 배열을 반환하는 함수를 작성해 주세요.
만약 읽을 수 없는 경우 빈 배열을 리턴해 주세요.

# Input
solution이라는 함수는 `width`, `height`, `cut_list`를 파라미터로 받습니다.
* `width` : int, 종이의 가로
* `height` : int, 종이의 세로
* `cut_list` : 컷의 가로위치(int), 컷의 세로위치(int), 컷의 너비(int), 컷의 높이(int) 4개의 튜플로 이뤄진 cut의 리스트
