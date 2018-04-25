---
layout: post
title:  "Github 설정 및 프로젝트 올리기"
date:   2018-03-28
excerpt: "Github"
tag:
- Github
comments: true
---

## 주요 명령어
* git init : 깃 저장소 초기화
* git status : 깃 저장소 상태 체크

## 사용 방법

#### 1st Step : Github.com 가입 후 Repository 만들기

#### 2nd Step : GitBash 앱 설치 후 명령어 입력

~~~
$ cd ProjectSavedFolderName
$ cd ProjectName
$ git init
$ git status
$ git remote add origin https://github.com/githubId/githubRepositoryName.git
~~~

* ProjectSavedFolderName : 내 컴퓨터에 프로젝트를 저장한 폴더 이름
* ProjectName : 내 컴퓨터에 저장한 프로젝트 이름
* githubId : 1st Step에서 github에 가입한 아이디gitgi
* githubRepositoryname : 1st Step에서 만든 Repository 

#### 3rd-1 Step : TortoiseGit 사용하여 Commit
* ProjectName 폴더에서 오른쪽 버튼 을 누른 후 Git Commit 선택
* Push Push Push (중간에 Github Id, Pw 입력)

#### 3rd-2 Step : GitBash로 새로운 Branch 생성 후 push
~~~
$ git checkout -b newBranchName // 새로운 branch 생성
$ git push origin newBranchName // id, pw 입력 후 push
~~~

