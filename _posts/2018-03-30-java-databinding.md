---
layout: post
title:  "REST API"
date:   2018-03-29
excerpt: "REST API"
tag:
- Android Studio
comments: true
---


## 사용방법

* Gradle에 추가

~~~
android {
    ...

    dataBinding {
        enabled = true
    }
}
~~~

* layout 감싸기

~~~
<layout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools">

<RelativeLayout
    android:layout_width="match_parent"
    android:layout_height="match_parent">
        <Button
        android:id="@+id/btnOK"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="OK"/>
  </relativelayout>

 </layout>
 ~~~

 * Java 


~~~
public class MainActivity extends AppCompatActivity {

 // MainActivity의 경우 ActivityMainBinding 자동 생성
    ActivityMainBinding mBinding;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        mBinding = DataBindingUtil.setContentView(this, R.layout.activity_main);

        //mBiding.(layout에서 지정한 id)
        mBinding.btnOK.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

            }
        });

    }
}
~~~

## 안될 경우

* Gradle 등 오타체크를 하고 싱크를 한 번 더 해본 후 다시 빌드
* MainAtivity일 경우. 소문자로 main, activity 등을 시도하지 말고 대문자(ActivirtMainBinding)로 작성