---
layout: post
title: PROGRAMMERS 두 정수 사이의 합
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, 자바]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 - 두 정수 사이의 합](https://programmers.co.kr/learn/courses/30/lessons/12912?language=java){: target="\_blank"}

## 문제
두 정수 a, b가 주어졌을 때 a와 b 사이에 속한 모든 정수의 합을 리턴하는 함수, solution을 완성하세요.
예를 들어 a = 3, b = 5인 경우, 3 + 4 + 5 = 12이므로 12를 리턴합니다.

제한 조건
- a와 b가 같은 경우는 둘 중 아무 수나 리턴하세요.
- a와 b는 -10,000,000 이상 10,000,000 이하인 정수입니다.
- a와 b의 대소관계는 정해져있지 않습니다.

## 제출한 답안

```java
class Solution {
  public long solution(int a, int b) {
      long answer = 0;
		if(a <= b) {
			for(int i=a; i<=b; i++) {
				answer += i;
			}	
		} else {
			for(int i=b; i<=a; i++) {
				answer += i;
			}
        }
		return answer;
  }
}
```

## 다른 사람 풀이
```java
class Solution {
    public long solution(int a, int b) {
        return sumAtoB(Math.min(a, b), Math.max(b, a));
    }

    private long sumAtoB(long a, long b) {
        return (b - a + 1) * (a + b) / 2;
    }
}
```
## 포인트

- 등차수열의 합 공식을 이용한 풀이! 대단하다.
- Math.min(a, b) => 둘 중 min 값을 가져오고, Math.max(a, b) => 둘 중 max 값을 가져온다.
- Math.min, max 를 이용해서 조건을 따로 나누지 않아도 된다는 것도 포인트!