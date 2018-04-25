---
layout: post
title:  "클래스와 인스턴스"
date:   2018-03-29
excerpt: "class, instance"
tag:
- Java
comments: true
---

## 개요

#### 클래스
- 연관되어 있는 변수와 메서드의 집합

#### 인스턴스 
- 클래스를 이용해 구체적인 결과를 만들어내는 것

#### 클래스&인스턴스 그리고 객체
- 보통 클래스와 인스턴스를 포괄적으로 객체라고 부르기도 함
- 클래스가 구체적인 실체인 인스턴스가 되었을 때 객체라고 부른다

## 예시

#### (예시1) 붕어빵 만들기
- 클래스=설계도 : 겉모양(붕어빵 틀), 겉재료
- 인스턴스들 : 찍어낸 붕어빵, 붕어빵의 내용물은 인스턴스 변수
 ex) 붕어빵A:아이스크림붕어빵, 붕어빵B:크림붕어빵, 붕어빵C:팥붕어빵, 붕어빵D:호두붕어빵

~~~
class 붕어빵틀 {
	static int 가격 = 500;
	static String 겉모양 = "붕어모양";
	static String 겉재료 = "밀가루"; 
	
	String 내용물;
	public 붕어빵틀(String strInner){
		내용물 = strInner;
	}
}

public class 붕어빵만들기 {
	public static void main(String[] args) {
	  붕어빵틀 myFish아이스크림 = new 붕어빵틀("아이스크림");
	  붕어빵틀 myFish크림 = new 붕어빵틀("크림");
	  붕어빵틀 myFish팥 = new 붕어빵틀("팥");
	  붕어빵틀 myFish호두 = new 붕어빵틀("호두");
		
	  System.out.println(myFish아이스크림.내용물);  // 인스턴스변수
	
	  System.out.println(붕어빵틀.가격);    // 클래스변수
	  System.out.println(붕어빵틀.겉모양);  // 클래스변수
	  System.out.println(붕어빵틀.겉재료);  // 클래스변수
		
	  System.out.println(myFish아이스크림.가격);  // 클래스변수를 인스턴스명으로 사용가능
	  System.out.println(myFish아이스크림.겉모양);  // 클래스변수를 인스턴스명으로 사용가능
	  System.out.println(myFish아이스크림.겉재료);  // 클래스변수를 인스턴스명으로 사용가능
	}
}

//참고 : http://m.post.naver.com/viewer/postView.nhn?volumeNo=6350086&memberNo=30800755&vType=VERTICAL
~~~

- 

#### (예시2) 스마트폰
- 스마트폰 설계도 : 클래스
- 스마트폰 완제품 : 인스턴스
- 하나의 설계도로 여러개의 제품을 만들어 낼 수 있음



!!! 개념 파악 및 정리 중 