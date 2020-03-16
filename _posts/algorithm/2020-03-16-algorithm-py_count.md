---
layout: post
title: PROGRAMMERS 문자열 내 p와 y의 개수
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, 자바]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 - 문자열 내 p와 y의 개수](https://programmers.co.kr/learn/courses/30/lessons/12916?language=java){: target="\_blank"}

## 문제
대문자와 소문자가 섞여있는 문자열 s가 주어집니다. s에 'p'의 개수와 'y'의 개수를 비교해 같으면 True, 다르면 False를 return 하는 solution를 완성하세요. 'p', 'y' 모두 하나도 없는 경우는 항상 True를 리턴합니다. 단, 개수를 비교할 때 대문자와 소문자는 구별하지 않습니다.

예를 들어 s가 pPoooyY면 true를 return하고 Pyy라면 false를 return합니다.

제한사항
- 문자열 s의 길이 : 50 이하의 자연수
- 문자열 s는 알파벳으로만 이루어져 있습니다.

## 제출한 답안

```java
class Solution {
  boolean solution(String s) {
        boolean answer = true;
        int aa = 0;
        int bb = 0;
        
        for(int i = 0; i < s.length(); i++){
            String a = s.substring(i,i+1);
            if(a.equals("p") || a.equals("P")) {
            	aa = aa+1;
            } else if(a.equals("y") || a.equals("Y")) {
            	bb = bb+1;
            }
        }
        
        if(aa==bb) {
        	answer = true;
        } else {
        	answer = false;
        }

        return answer;
    }
}
```

## 다른 사람 풀이 1
```java
class Solution {
    boolean solution(String s) {
        s = s.toUpperCase();

        return s.chars().filter( e -> 'P'== e).count() == s.chars().filter( e -> 'Y'== e).count();
    }
}
```

## 다른 사람 풀이 2
```java
class Solution {
    boolean solution(String s) {
        s = s.toLowerCase();
        int count = 0;

        for (int i = 0; i < s.length(); i++) {

            if (s.charAt(i) == 'p')
                count++;
            else if (s.charAt(i) == 'y')
                count--;
        }

        if (count == 0)
            return true;
        else
            return false;
    }
}
```

## 다른 사람 풀이 3
```java
class Solution {
    boolean solution(String s) {
        return s.toUpperCase().split("P").length ===  s.toUpperCase().split("Y").length;
    }
}
```

## 포인트
- toUpperCase(); 혹은 toLowerCase(); 를 이용하면 대문자 혹은 소문자로 통일할 수 있기 때문에 변수를 여러가지로 안 써도 된다.
- String.chars()는 String을 Stream으로 변환해주는 것인데, 배열처럼 나온다고 보면 된다.
- arr.filter(callback[, thisArg]) 는 콜백함수와 생략 가능한 thisArg로 이루어져 기존의 배열에서 필터링 후 새로운 배열이 만들어지는 메서드다.
- e -> 'P' == e 는 arrow function이고, 이것은 function(e){return 'P' == e}이다.
- 따라서 s.chars().filter(e -> 'P' == e)는 String s를 Stream, 즉 배열 형식으로 변환한 후 'P' == e인 값만 남긴 새로운 배열이 만들어진 상태이다.
- 이 Stream의 count()를 세는 것이다.
- 개인적으로 1번은 어떻게 저런 생각을 하지, 라는 느낌이었고, 2번은 +, -를 한다는 생각이 대단했고, 3번은 직관적이고 깔끔해서 한 눈에 의미 파악을 할 수 있는 좋은 풀이였다.