---
layout: post
title:  "Observable"
date:   2018-03-29
excerpt: "Observable"
tag:
- RxJava
category:
- RxJava
comments: true
---

## Introduction

#### Observable 

* 데이터 흐름에 맞게 알림을 보내 구독자가 데이터를 처리할 수 있게 함, Observable Pattern 구현

#### Observer Pattern 

* 객체의 상태 변화를 관찰하는 Observer 목록을 객체에 등록
* 상태 변화가 있을 때마다 메소를 호출하여 객체가 직접 목록의 각 Observer에게 변화를 알림
* 보통 단일 함수를 통해 변화를 알림

#### 구독자에게 전달하는 알림

* onNext : Observable이 데이터의 발행을 알림
* onComplete : 모든 데이터 발행을 완료했음을 알림. 단 한 번 발생
* onError : Observable에서의 Error를 알림. Observable 실행 종료


## 함수

#### just()
* 인자로 넣은 데이터를 차례로 발행하기 위해 Observable 생성
* 1~10의 타입이 같은 값

~~~
public static <T> Observable<T> just(T item)
public static <T> Observable<T> just(T item1, T item2)
public static <T> Observable<T> just(T item1, T item2, T item3
public static <T> Observable<T> just(T item1, T item2, T item3, T item4)
public static <T> Observable<T> just(T item1, T item2, T item3, T item4, T item5)
public static <T> Observable<T> just(T item1, T item2, T item3, T item4, T item5, T item6)
public static <T> Observable<T> just(T item1, T item2, T item3, T item4, T item5, T item6, T item7)
public static <T> Observable<T> just(T item1, T item2, T item3, T item4, T item5, T item6, T item7, T item8)
public static <T> Observable<T> just(T item1, T item2, T item3, T item4, T item5, T item6, T item7, T item8, T item9)
~~~

* 값은 그대로 출력

~~~
public class ObservableStudy {
    public void emit() {
        Observable.just(1,2,3)
                .subscribe(System.out::println)
    }
}
~~~

~~~
1
2
3
~~~


#### subscribe()

+++
!!! 학습중에 정리한 내용입니다. 개선할 부분이 있다면 메일 주시면 감사하겠습니다.
[참고] RxJava 프로그래밍 by 유동환, 박정준