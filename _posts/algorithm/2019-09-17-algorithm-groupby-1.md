---
layout: post
title: PROGRAMMERS 동명 동물 수 찾기 (MySQL)
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, mySQL]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 연습 동명 동물 수 찾기](https://programmers.co.kr/learn/courses/30/lessons/59041){: target="\_blank"}

## 문제 및 정답 화면

![](/assets/post-img/algorithm/programmers_groupby_1.PNG)

## 제출

<pre>
SELECT NAME, COUNT(NAME)
FROM ANIMAL_INS
GROUP BY NAME
HAVING COUNT(NAME) >= 2;
</pre>

## 포인트

- GROUP BY 문에서는 WHERE가 아닌 HAVING으로 조건을 나타낸다.
