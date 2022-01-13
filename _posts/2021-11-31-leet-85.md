---
layout: post
title: LeetCode 85. Maximal Rectangle
tags: [leetcode, ps]
comments: false
---

## [문제](https://leetcode.com/problems/maximal-rectangle/)
Given a rows x cols binary matrix filled with 0's and 1's, find the largest rectangle containing only 1's and return its area.

### Example
![Example]({{ site.baseurl }}/images/leetcode85-example.jpg)

```
Input: matrix = [["1","0","1","0","0"],["1","0","1","1","1"],["1","1","1","1","1"],["1","0","0","1","0"]]
Output: 6
Explanation: The maximal rectangle is shown in the above picture.
```

### Constraints
- `rows == matrix.length`
- `cols == matrix[i].length`
- `0 <= row, cols <= 200`
- `matrix[i][j]` is `'0'` or `'1'`.

## 해결 방법
직사각형의 면적: `row 방향으로 연속으로 이어진 블럭의 개수` * `min(각 row 별로 연속으로 이어진 column의 개수)` 라는 점에 착안하여 문제 해결

전체 2차원 배열을 (1) column-wise / (2) row-wise 한번씩 traverse 하면서 위 두 요소를 계산하여 직사각형의 최대 면적을 계산함

- Traverse 1: `각 row 별로 연속으로 이어진 column의 개수` ("column 길이"라고 하자) 계산
  - 특정 (row, col)을 기준으로 `matrix[col] == matrix[col+1] == ... == matrix[col+cnt]` 인 연속된 클럭의 개수 `cnt` 계산
  - 예시: 아래 그림의 각 블럭 오른쪽의 숫자를 계산

- Traverse 2: `row 방향으로 연속으로 이어진 블럭의 개수`를 세면서 위 단계에서 계산해 놓은 column 길이의 최소값을 구해서 곱함
  - 예시: 아래 그림에서 왼쪽 상단의 (row, col)을 기준으로 row 방향으로 연속으로 이어진 5개의 블럭에 대해 확인하면서 가능한 직사각형의 최대값을 계산. (1) 1 * 3 = 3, (2) 2 * 2 = 4, (3) 3 * 2 = 6, (4) 4 * 1 = 4, (5) 5 * 1 = 5 중 최대값은 (3)번 단계의 6으로 계산 가능

![Solution]({{ site.baseurl }}/images/leetcode85-solution.PNG)
