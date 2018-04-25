---
layout: post
title:  "Kotlin Class"
date:   2018-03-29
excerpt: "Sealed Class"
tag:
- Kotlin
comments: true
---

## 생성자 : constructor

#### Usage
* java와 달리, class 내부에 생성자를 만들지 않고, constructor 키워드로 생성자 만듬 -> constructor 생략 가능

~~~
class Person constructor(name:String, age:Int){ }
// = class Person(name:String, age:Int){ }
~~~


## Sealed Classes

#### Introductoion
* 상속을 제한하기 위해 사용하는 class(내부 상속 가능, 외부 모듈 X)
* 일종의 ADT(Algebraic Data type : 대수 데이터 타입)
* 제한된(하나의 타입 가능, 다른 타입x) 클래스 계층구조를 나타냄
* 추상 클래스로, 추상 멤버를 가질 수 있으나 직접 인스턴스를 가질 수 없음

<!-- #### Enum & Sealed Class
~~~
//Enum
//Sealed Class
~~~ -->

#### Usage
* Sealed Class 선언 : 클래스 앞에 Sealed 키워드 입력
~~~
sealed class Expr 
~~~
* Kotlin Context에서 `when`과 함께 사용 가능
~~~
fun eval(expr: Expr): Double = when(expr) {  
    is Const -> expr.number
    is Sum -> eval(expr.e1) + eval(expr.e2)
    NotANumber -> Double.NaN
}
~~~
