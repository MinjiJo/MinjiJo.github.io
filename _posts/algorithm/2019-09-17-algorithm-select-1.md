---
layout: post
title: PROGRAMMERS 상위 n개 레코드 (MySQL)
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, mySQL]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 연습 상위 n개 레코드](https://programmers.co.kr/learn/courses/30/lessons/59405){: target="\_blank"}

## 문제 및 정답 화면

![](/assets/post-img/algorithm/programmers_select_1.PNG)

## 제출

<pre>
SELECT NAME
FROM ANIMAL_INS
WHERE DATETIME = (SELECT MIN(DATETIME)
                 FROM ANIMAL_INS)
</pre>

## 포인트

- 서브쿼리를 활용해서 풀 수 있다.
- MIN(DATETIME)의 경우 가장 오래된 날짜를 가져오게 된다.
