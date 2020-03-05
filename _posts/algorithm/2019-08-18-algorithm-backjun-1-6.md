---
layout: post
title: 백준 알고리즘 no.1000 A+B
category: 알고리즘 문제풀이
permalink: /algorithm/:year/:month/:day/:title/
tags: [알고리즘, 자바]
comments: true
---

## 출처

[문제출처 - 백준 알고리즘 1단계(입출력과 사칙연산) 中](https://www.acmicpc.net/problem/1000){: target="\_blank"}

## 문제

두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

## 입력

첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

## 출력

첫째 줄에 A+B를 출력한다.

## 제출

 <pre>
import java.util.*;
public class Main{
	public static void main(String args[]){
		Scanner sc = new Scanner(System.in);
		int a, b;
		a = sc.nextInt();
		b = sc.nextInt();
		System.out.println(a + b);
	}
}
</pre>

## 숏코드

<pre>
import java.util.*;
class Main{
    public static void main(String[]t){
        Scanner x=new Scanner(System.in);
        System.out.print(x.nextInt()+x.nextInt());}}
</pre>

## 포인트

- 시스템에 입력하는 기능을 쓰기 위해서는 다음 코드를 작성해야 한다.
    <pre>import java.util.*;
    Scanner sc = new Scanner(System.in);
  </pre>
