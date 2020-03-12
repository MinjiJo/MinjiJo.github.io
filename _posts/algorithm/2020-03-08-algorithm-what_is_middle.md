---
layout: post
title: PROGRAMMERS 가운데 글자 가져오기
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, 자바]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 - 가운데 글자 가져오기](https://programmers.co.kr/learn/courses/30/lessons/12903?language=java){: target="\_blank"}

## 문제
단어 s의 가운데 글자를 반환하는 함수, solution을 만들어 보세요. 단어의 길이가 짝수라면 가운데 두글자를 반환하면 됩니다.

제한사항
- s는 길이가 1 이상, 100이하인 스트링입니다.

## 제출한 답안

```java
class Solution {
  public String solution(String s) {
      int l = s.length();
		String answer = "";
		
		if(l%2==1) {
			s.substring((l-1)/2, (l-1)/2+1);
			answer = s.substring((l-1)/2, (l-1)/2+1);
		} else {
			s.substring(l/2-1, l/2+1);
			answer = s.substring(l/2-1, l/2+1);
		}
		
	    return answer;
  }
}
```

## 모범 답안

```java
class Solution {
  String solution(String word){
    return word.substring((word.length()-1) / 2, word.length()/2 + 1);
  }
}
```

## 포인트

- if로 경우를 나누지 않아도 한 줄로 substring을 써서 나타날 수 있음