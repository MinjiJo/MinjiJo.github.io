---
layout: post
title: PROGRAMMERS 직사각형 별찍기
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 - 직사각형 별찍기](https://programmers.co.kr/learn/courses/30/lessons/12969?language=java){: target="\_blank"}

## 문제
이 문제에는 표준 입력으로 두 개의 정수 n과 m이 주어집니다.
별(*) 문자를 이용해 가로의 길이가 n, 세로의 길이가 m인 직사각형 형태를 출력해보세요.

제한 조건
- n과 m은 각각 1000 이하인 자연수입니다.

## 제출한 답안

```java
public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();

        for(int i=0; i<b; i++) {
            for(int j=0; j<a; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
        sc.close();
    }
}
```
## 포인트

- 트리 찍기 느낌의 문제. for문을 사용하면 간단하게 풀 수 있는 문제였다.