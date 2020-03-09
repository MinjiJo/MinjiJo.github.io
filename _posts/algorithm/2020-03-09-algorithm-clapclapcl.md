---
layout: post
title: PROGRAMMERS 수박수박수박수박수박수?
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 - 수박수박수박수박수박수?](https://programmers.co.kr/learn/courses/30/lessons/12922?language=java){: target="\_blank"}

## 문제
길이가 n이고, 수박수박수박수....와 같은 패턴을 유지하는 문자열을 리턴하는 함수, solution을 완성하세요. 예를들어 n이 4이면 수박수박을 리턴하고 3이라면 수박수를 리턴하면 됩니다.

제한 조건
- n은 길이 10,000이하인 자연수입니다.

## 제출한 답안

```java
class Solution {
  public String solution(int n) {
      String a = "수";
      String b = "박";
      
      String answer = "";
      
      if(n%2==0){
          for(int i = 1; i <= n/2; i++){
              answer += a;
              answer += b;
          }
      } else {
          for(int i = 1; i <= (n-1)/2; i++){
              answer += a;
              answer += b;
          }
          
          answer += a;
      }
      return answer;
  }
}
```

## 모범 답안 1

```java
public String solution(int n){
    return new String(new char [n/2+1]).replace("\0", "수박").substring(0,n);
}
```
## 모범 답안 2

```java
public String solution(int n){
    String result = "";
    for (int i = 0; i < n; i++)
      result += i % 2 == 0 ? "수" : "박";
        return result;
}
```
## 포인트

![](/assets/post-img/algorithm/programmers_clapclapcl.PNG)
출처 : <https://jhnyang.tistory.com/122>