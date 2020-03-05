---
layout: post
title: PROGRAMMERS 입양 시각 구하기(1) (MySQL)
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, mySQL]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 연습 입양 시각 구하기(1)](https://programmers.co.kr/learn/courses/30/lessons/59412){: target="\_blank"}

## 문제 및 정답 화면

![](/assets/post-img/algorithm/programmers_groupby_2.PNG)

## 제출

<pre>
SELECT HOUR(DATETIME) HOUR, COUNT(DATETIME) COUNT
FROM ANIMAL_OUTS
WHERE HOUR(DATETIME) BETWEEN 9 AND 19
GROUP BY HOUR(DATETIME);
</pre>

## 포인트

- 여기서 WHERE와 GROUP BY의 순서가 바뀌게 되면 뜻이 달라지므로 주의해야 한다.
