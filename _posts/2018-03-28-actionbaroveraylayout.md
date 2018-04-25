---
layout: post
title:  "ActionBarOverayLayout-레이아웃 미리보기 오류"
date:   2018-03-28
excerpt: "Android layout preview error"
tag:
- Android Studio
comments: true
---

## 해결 방법
* `values>styles.xml` style AppTheme에 **Base.** 추가

#### BEFORE

~~~
<style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar">//변경 전
~~~

#### AFTER

~~~
<style name="AppTheme" parent="Base.Theme.AppCompat.Light.DarkActionBar">//변경후
~~~

---





