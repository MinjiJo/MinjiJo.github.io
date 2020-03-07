---
layout: post
title: PROGRAMMERS 같은 숫자는 싫어
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 - 같은 숫자는 싫어](https://programmers.co.kr/learn/courses/30/lessons/12906?language=java){: target="\_blank"}

## 문제
배열 arr가 주어집니다. 배열 arr의 각 원소는 숫자 0부터 9까지로 이루어져 있습니다. 이때, 배열 arr에서 연속적으로 나타나는 숫자는 하나만 남기고 전부 제거하려고 합니다. 단, 제거된 후 남은 수들을 반환할 때는 배열 arr의 원소들의 순서를 유지해야 합니다. 예를 들면,

- arr = [1, 1, 3, 3, 0, 1, 1] 이면 [1, 3, 0, 1] 을 return 합니다.
- arr = [4, 4, 4, 3, 3] 이면 [4, 3] 을 return 합니다.
배열 arr에서 연속적으로 나타나는 숫자는 제거하고 남은 수들을 return 하는 solution 함수를 완성해 주세요.

제한사항
- 배열 arr의 크기 : 1,000,000 이하의 자연수
- 배열 arr의 원소의 크기 : 0보다 크거나 같고 9보다 작거나 같은 정수

## 모범 답안

```java
public class Solution  {
		List<Integer> temp = new ArrayList<Integer>();
		int num = 10;
		for(int i : arr) {
			if(num != i) {
				temp.add(i);
			}
			num = i;
		}

		int[] answer = new int[temp.size()];
		for (int i = 0; i < temp.size(); i++) {
			answer[i] = temp.get(i);
		}

		return answer;
	}
```

## 포인트

- int num = 10을 생각하다니... 진짜 깔끔하다. 9보다 작거나 같은 정수까지 나오므로 10으로 비교해서 행렬의 첫번째 값을 무조건 넣은 후, 해당 배열의 값을 다시 num에 넣으면서 배열의 끝까지 비교해 정확한 답이 나올 수 있게 했다.
- 향상된 for문의 경우 **i == arr[i]**