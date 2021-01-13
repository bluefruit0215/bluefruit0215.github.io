---
layout: post
title:  "프로그래머스 SQL 고득점 Kit 풀이(SUM, MAX, MIN)"
subtitle:   ""
categories: sql
tags: 연습문제
comments: true
---

# SUM, MAX, MIN

## 1. 최댓값 구하기
#### 문제 설명
![problem2_1](../../../../assets/img/sql/problem2_1.PNG)
#### 풀이
`SELECT MAX(DATETIME) AS 시간 FROM ANIMAL_INS;`

## 2. 최솟값 구하기
#### 문제 설명
![problem2_2](../../../../assets/img/sql/problem2_2.PNG)
#### 풀이 1
`SELECT DATETIME AS 시간 FROM ANIMAL_INS ORDER BY DATETIME ASC LIMIT 1;`
#### 풀이 2
`SELECT MIN(DATETIME) AS 시간 FROM ANIMAL_INS;`

## 3. 동물 수 구하기
#### 문제 설명
![problem2_3](../../../../assets/img/sql/problem2_3.PNG)
#### 풀이
`SELECT COUNT(*) AS COUNT FROM ANIMAL_INS;`

COUNT(*)은 테이블의 전체 행 수를 나타냅니다(NULL값도 포함해서 count합니다).

## 4. 중복 제거하기
#### 문제 설명
![problem2_4](../../../../assets/img/sql/problem2_4.PNG)
#### 풀이
`SELECT COUNT(DISTINCT NAME) AS count FROM ANIMAL_INS;`

중복을 제거하기 위해 DISTINCT를 사용합니다.
