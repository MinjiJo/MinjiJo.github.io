---
layout: post
title: PROGRAMMERS 문자열 다루기 기본
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, 자바]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 - 문자열 다루기 기본](https://programmers.co.kr/learn/courses/30/lessons/12918){: target="\_blank"}

## 문제
문자열 s의 길이가 4 혹은 6이고, 숫자로만 구성돼있는지 확인해주는 함수, solution을 완성하세요. 예를 들어 s가 a234이면 False를 리턴하고 1234라면 True를 리턴하면 됩니다.

제한 사항
- s는 길이 1 이상, 길이 8 이하인 문자열입니다.

## 제출한 답안

```java
class Solution {
  public boolean solution(String s) {
      if(s.length() ==4 || s.length() == 6) {
        try {
            Integer.parseInt(s);
            return true;
        } catch (Exception e) {
            return false;
        }
      } else {
          return false;
      }
  }
}
```

## 다른 사람 풀이
```java
class Solution {
  public boolean solution(String s) {
        if (s.length() == 4 || s.length() == 6) return s.matches("(^[0-9]*$)");
        return false;
  }
}
```

## 포인트
- Integer.parseInt(s) 는 string을 정수로 변환할 수 있는지 확인할 때 쓰인다.
- " 12", "123 " 등의 공백이 있는 숫자의 경우 Integer.parseInt(s)는 false를 리턴하지만 Double.parseDobule(s)의 경우 trim이 적용되면서 true를 반환한다.
- 정규표현식도 가능하다는 것을 깨달았다.