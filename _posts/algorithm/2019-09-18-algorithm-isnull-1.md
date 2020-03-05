---
layout: post
title: PROGRAMMERS NULL 처리하기 (MySQL)
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, mySQL]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 연습 NULL 처리하기](https://programmers.co.kr/learn/courses/30/lessons/59410){: target="\_blank"}

## 문제

![](/assets/post-img/algorithm/programmers_isnull_1_1.PNG)
![](/assets/post-img/algorithm/programmers_isnull_1_2.PNG)

## 제출

![](/assets/post-img/algorithm/programmers_isnull_1_3.PNG)

<pre>
SELECT ANIMAL_TYPE, IFNULL(NAME, 'No name'), SEX_UPON_INTAKE
FROM ANIMAL_INS
ORDER BY ANIMAL_ID
</pre>

## 포인트

- 오라클에서 NVL(조건, 조건이 NULL일 때 표시할 내용)으로 쓰는 것을 MySQL에서는 IFNULL(조건, 조건이 NULL일 때 표시할 내용)으로 작성한다.
- 따라서 IFNULL(NAME, 'No name')은 NAME 칼럼에서 NULL 값이 오는 경우 No name으로 표시하겠다는 뜻이다.
