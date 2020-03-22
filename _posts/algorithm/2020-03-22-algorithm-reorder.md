---
layout: post
title: PROGRAMMERS 문자열 내 마음대로 정렬하기
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, 자바]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 - 문자열 내 마음대로 정렬하기](https://programmers.co.kr/learn/courses/30/lessons/12915?language=java){: target="\_blank"}

## 문제
문자열로 구성된 리스트 strings와, 정수 n이 주어졌을 때, 각 문자열의 인덱스 n번째 글자를 기준으로 오름차순 정렬하려 합니다. 예를 들어 strings가 [sun, bed, car]이고 n이 1이면 각 단어의 인덱스 1의 문자 u, e, a로 strings를 정렬합니다.

제한 조건
- strings는 길이 1 이상, 50이하인 배열입니다.
- strings의 원소는 소문자 알파벳으로 이루어져 있습니다.
- strings의 원소는 길이 1 이상, 100이하인 문자열입니다.
- 모든 strings의 원소의 길이는 n보다 큽니다.
- 인덱스 1의 문자가 같은 문자열이 여럿 일 경우, 사전순으로 앞선 문자열이 앞쪽에 위치합니다.

## 제출한 답안

```java
import java.util.Arrays;
import java.util.Comparator;

class Solution {
  public String[] solution(String[] strings, int n) {
      String[] answer = {};
		Arrays.sort(strings, new Comparator<String>() {

			@Override
			public int compare(String arg0, String arg1) {

				if (arg0.charAt(n) == arg1.charAt(n)) {
					return arg0.compareTo(arg1);
				}

				return arg0.charAt(n) - arg1.charAt(n);
			}
		});

		answer = new String[strings.length];

		for (int i = 0; i < strings.length; i++) {
			answer[i] = strings[i];
		}
		return answer;
  }
}
```

## 다른 사람 풀이
```java
import java.util.*;

class Solution {
    public String[] solution(String[] strings, int n) {
        String[] answer = {};
        ArrayList<String> arr = new ArrayList<>();
        for (int i = 0; i < strings.length; i++) {
            arr.add("" + strings[i].charAt(n) + strings[i]);
        }
        Collections.sort(arr);
        answer = new String[arr.size()];
        for (int i = 0; i < arr.size(); i++) {
            answer[i] = arr.get(i).substring(1, arr.get(i).length());
        }
        return answer;
    }
}
```

## 포인트
- list에 넣을 때 아예 첫 글자를 따로 빼내서 기본정렬한다는 생각! 진짜 대단하다.
- Comparable은 기본 정렬기준을 구현하는데 사용되는데, 배열은 Arrays.sort() 이고 ArrayList는 Collections.sort()를 이용해야 한다.
- 기본 정렬기준이 아닌 다른 정렬기준을 이용하기 위해서는 Comparator를 이용해야 하고 compareTo() 메소드를 오버라이드 하여 원하는 정렬 조건을 넣어주어야 한다.