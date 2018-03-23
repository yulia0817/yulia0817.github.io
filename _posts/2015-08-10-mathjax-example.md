---
layout: post
title:  "Lottie 사용법"
date:   2018-03-15
excerpt: "Littie"
tag:
- Lottie 
- After Effect
- BodyMovin
- test
- Android
comments: true
---

## Introduction
* iOS, Android, React Native 등에서 사용
* After Effet 애니메이션을 실시간으로 렌더링하는 라이브러리
* JSON 형식으로 추출한 애니메이션 데이터 사용
* API14 이상 안드로이드 버전 필요
## Usage

#### After Effect
* 일반 설정에서 네트워크 허용
* ZXP Installer로 플러그인 설치 후 `Window>Extensions BodyMovin` 활성화
* Download에 bodymovin으로 render하여 json 파일 생성

#### Android Studio
* Gradle dependencies에 [github](https://github.com/airbnb/lottie-android) 최신 버전 확인하여 추가
~~~
dependencies {
  compine 'com.airbnb.android:lottie:2.2.5'
}
~~~
* xml
~~~
<com.airbnb.lottie.LottieAnimationView
    android:id="@+id/animation_view"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    app:lottie_autoPlay="true"
    app:lottie_fileName="---.json" //assets에 추가한 json파일명 적확히 기입
    app:lottie_loop="true"/>
~~~    
* JAVA Code
~~~
LottieAnimationView animationView = (LottieAnimationView) findViewById(R.id.animation_view);
animationView.setAnimation("data.json");
animationView.loop(true);
animationView.playAnimation();
~~~

<figure>
	<a href="https://github.com/airbnb/lottie-android/raw/master/gifs/Example2.gif"><img src="https://github.com/airbnb/lottie-android/raw/master/gifs/Example2.gif"></a>
	<figcaption><a href="https://airbnb.design/lottie/" title="Lottie">Lottie</a>.</figcaption>
</figure>


$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
$$
