---
layout: post
title: PROGRAMMERS 서울에서 김서방 찾기]
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘]
comments: true
---

## 출처

[문제출처 - PROGRAMMERS 코딩테스트 - 서울에서 김서방 찾기](https://programmers.co.kr/learn/courses/30/lessons/12919?language=java){: target="\_blank"}

## 문제
String형 배열 seoul의 element중 Kim의 위치 x를 찾아, 김서방은 x에 있다는 String을 반환하는 함수, solution을 완성하세요. seoul에 Kim은 오직 한 번만 나타나며 잘못된 값이 입력되는 경우는 없습니다.

제한 사항
- seoul은 길이 1 이상, 1000 이하인 배열입니다.
- seoul의 원소는 길이 1 이상, 20 이하인 문자열입니다.
- Kim은 반드시 seoul 안에 포함되어 있습니다.

## 제출한 답안

```java
class Solution {
  public String solution(String[] seoul) {
      String answer = "";
      for(int i = 0; i < seoul.length; i++){
          if(seoul[i].equals("Kim")){
              answer = "김서방은 " + i + "에 있다";
          }
      }
      return answer;
  }
}
```

## 다른 사람 풀이
```java
public String findKim(String[] seoul){
        //x에 김서방의 위치를 저장하세요.
        int x = 0;
    while(x<seoul.length){
      if(seoul[x] == "Kim")
        break;
      else x++;
    }


        return "김서방은 "+ x + "에 있다";
    }
```
## 포인트

- String을 비교할 때는 ==이 아니라 .equals()를 사용!(계속 안되서 왜지 왜지 생각하다가 퍼뜩 떠올랐다.)
- while을 써서 break;를 쓰면 찾는 순간 탐색을 그만하니까 시간이 더 줄어들 것 같다.
- int x = Arrays.asList(seoul).indexOf("Kim"); 방식으로 찾는 것도 보았는데, list로 바꾸지는 않아도 될 것 같지만 이런 방식도 있다! 정도로 알아두는 것도 좋을 듯.