---
title: "[블로그] Jekyll 테마 이용해 GitHub Blog 만들기"
date: 2023-10-16 10:00:00 +09:00
categories: [개인, 블로그]
tags: [GitHubBlog, Jekyll, Chirpy]
image: /assets/img/BlogImage/elice.png
published: true
pin: false
---

## (0) GitHub 블로그를 만들게 된 이유

공부한 내용을 개인적으로 정리하고자 TISTORY 블로그를 운영했었다. 

> 주소 : https://pharam.tistory.com

보다시피 전체 글도 14개밖에 안 되고, 날짜도 오래되었다.
정제된 언어로 글을 쓰는 것이 어려워 시간도 오래 걸렸고, 진행한 프로젝트에 대한 회고도 제대로 하지 않았던 터라 꾸준하게 올리지 못했다.

마침 우아한테크코스 자기소개서 문항에 **‘긴 시간 동안 몰입해 본 경험’**이 있고, 기업 공고의 우대 사항에 **‘지속적인 자기 성장 루틴을 가지고 계신 분’**이 있어 블로그를 다시 시작해보려는 마음을 갖게 되었다.

사용하던 TISTORY 블로그를 이어서 사용할까 생각했지만, 이왕이면 개발자다운 [GitHub.io](http://GitHub.io) 블로그를 만들어 운영해보고 싶었다. 
사실 최근에 GitHub 잔디 심기에 관심이 생겼는데, 프로젝트 커밋과 블로그 작성으로 모두 잔디를 심게 된다면 더욱 동기부여가 될 것 같았기 때문이다. 

웹 페이지를 처음부터 직접 만드는 것은 아직 한계가 있다고 느껴, Jekyll을 이용해 자동으로 생성하기로 했다. 세부적인 내용은 차차 수정해 나갈 예정이다.

<br>

## (1) GitHub 블로그 생성하기

1. Create a new Repository
	- Repository Name : [username.github.io](http://username.github.io/)
	- public & Add a README file 체크

2. Clone Repository to GitHub desktop
	- Open with GitHub Desktop을 눌러 Repository를 Clone한다.
	- 터미널에서 입력하는 방법도 있지만, 사용하고 있던 GitHub Desktop에서 진행하였다.

## (2) Jekyll 이용해 GitHub 블로그 꾸미기
Jekyll을 이용하면 손쉽게 블로그를 꾸밀 수 있다.

일반적인 방법으로 Jekyll을 설치하려고 했으나, 맥북 M1을 사용하고 있다 보니 ruby 오류가 발생했다. 그래서 M1 MAC 기준으로 설명해보려고 한다.

1. rebenv 설치 (brew가 없다면 설치해야 한다.)
	```
	brew install rbenv ruby-build
	```
	
2. 