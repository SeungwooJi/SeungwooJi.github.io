---
layout: post
author: SeungwooJi
tags: [overview, moonwalk]
---

## Google Analytics
    
Google Analytics는 웹사이트 및 앱의 트래픽을 추적하고 분석하기 위한 Google의 무료 웹 분석 서비스입니다  이 도구를 사용하면 사용자가 웹사이트나 앱에서 어떻게 상호작용하는지에 대한 풍부한 정보를 얻을 수 있습니다 이번 포스팅에서는 이 Google Analytics를 Jekyll 블로그에 적용하는 과정을 다루겠습니다


## 설정

### Google Analytics 계정 설정
 1.  [Google Analytics](https://analytics.google.com)로 이동하여 로그인하거나 측정 시작을 눌러 계정을 생성합니다. (아래 내용은 제 기준으로 작성됬으며 필요하신 설정을 체크 하신 후 진행하시면 됩니다.)
 - 계정 생성 (계정 이름)
 - 계정 데이터 공유 설정(저 같은 경우에는 모두 체크 후 다음으로 이동)
 - 속성 이름 (잘 모르겠지만 저는 계정 생성 할 때와 동일 한 이름으로 진행)
 - 보고 시간대, 통화 변경(대한민국)
 - 업종 - 컴퓨터 및 전자제품 선택
 - 비즈니스 규모 작음 선택
 - 비즈니스 목표
    - 리드 생성과 사용자 행동 검토 선택
- 동의함

- 플랫폼 - 웹 선택

![analytics2.png](images/analytics2.png)

- 데이터 스트림 설정 페이지가 뜨면 자신의 블로그 웹사이트 url과 스트림 이름 설정 후 스트림 만들기

![analytics1.png](images/analytics1.png)

### 2. Jekyll 블로그에 추적 코드 추가
1. Jekyll 블로그의 _config.yml 파일을 엽니다
2. analytics 관련 설정이 있는지 찾아보고, 적절히 수정하라는 설명이 있지만 저 같은 경우에는 관련 내용이 없었으므로 
3. 애널리스트 데이터 수집 및 수정에서 데이터 스트림을 클릭하고 맨 밑 태그 안내보기를 클릭
4. 직접 설치를 클릭해서 나온 Google 태그를 복사
3. _includes 폴더 내의 head.html 파일을 열어 \<head> 요소 바로 다음에 붙여넣습니다
4. 변경사항을 모두 저장하고 Github에 커밋 및 푸시합니다

테스트 결과 정상적으로 작동하는 것을 볼 수 있습니다.

![analytics3.png](images/analytics3.png)

![analytics4.png](images/analytics4.png)

