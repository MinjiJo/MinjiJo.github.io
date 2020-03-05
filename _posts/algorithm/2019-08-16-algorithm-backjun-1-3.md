---
layout: post
title: 백준 알고리즘 no.10171 고양이
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, 자바]
comments: true
---

## 출처

[문제출처 - 백준 알고리즘 1단계(입출력과 사칙연산) 中](https://www.acmicpc.net/problem/10171){: target="\_blank"}

## 문제

아래 예제와 같이 고양이를 출력하시오.

<pre>
\    /\
 )  ( ')
(  /  )
 \(__)| </pre>

## 제출

 <pre>
 public class Main{
    public static void main(String[] args){
       System.out.println("\\    /\\");
       System.out.println(" )  ( ')");
       System.out.println("(  /  )");
       System.out.println(" \\(__)|");
       }
}                        </pre>

## 숏코드

<pre>
public class Main{
    public static void main(String[] args){
    System.out.print("\\    /\\\n )  ( ')\n(  /  )\n \\(__)|");}}
</pre>

## 포인트

- 자바에서는 역슬래쉬, 큰따옴표가 출력이 바로 안되기 때문에 둘 다 앞에 역슬래쉬를 하나 더 붙여 줘야 한다.
- println은 라인 변경, print는 그냥 출력. 이 때 \n을 붙여주면 줄 바꿈이 일어나기 때문에 반복해서 println을 사용하지 않더라도 한 줄 안에 모든 코드를 다 넣을 수 있다.
- 그리고 꼭 쉼표 빼먹지 말기!
