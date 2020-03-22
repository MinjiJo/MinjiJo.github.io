---
layout: post
title: PROGRAMMERS 문자열을 정수로 바꾸기
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, 자바]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 - 문자열을 정수로 바꾸기](https://programmers.co.kr/learn/courses/30/lessons/12925?language=java){: target="\_blank"}

## 문제
문자열 s를 숫자로 변환한 결과를 반환하는 함수, solution을 완성하세요.

제한 조건
- s의 길이는 1 이상 5이하입니다.
- s의 맨앞에는 부호(+, -)가 올 수 있습니다.
- s는 부호와 숫자로만 이루어져있습니다.
- s는 0으로 시작하지 않습니다.

## 제출한 답안

```java
class Solution {
  public int solution(String s) {
      int answer = Integer.parseInt(s);
      return answer;
  }
}
```

## 다른 사람 풀이
```java
class Solution {
  public int solution(String str) {
            boolean Sign = true;
            int result = 0;

      for (int i = 0; i < str.length(); i++) {
                char ch = str.charAt(i);
                if (ch == '-')
                    Sign = false;
                else if(ch !='+')
                    result = result * 10 + (ch - '0');
            }
            return Sign?1:-1 * result;
    }
}
```

## 포인트
- Integer.parseInt(s) 는 string을 정수로 변환할 수 있는지 확인할 때 쓰인다.
- parseInt를 자잘하게 나눠서 생각하면 저 풀이가 나올 것 같다. 알고리즘적으로 생각하는 것 자체가 대단했다.