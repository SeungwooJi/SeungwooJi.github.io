---
layout: post
author: SeungwooJi
tags: [overview, moonwalk]
---

블로그에 댓글 기능을 추가하기 위해 블로그 댓글 시스템을 제공하는 도구인 Utterances 라이브러리를 사용하여 블로그에 댓글 기능을 추가하는 과정을 다룬 글입니다 이 글을 보고 Utterances를 이용한 댓글 기능 추가할 수 있게 설명하는 방식으로 추가했던 과정을 다룹니다.

## Utterances의 장점
1. 광고가 없고 가볍습니다. 또한 무료로 이용 가능합니다
2. GitHub Issue 활용
- Utterances는 GitHub Issue를 사용하여 댓글을 저장하고 관리합니다. 이는 이슈 트래킹 시스템을 활용하여 댓글을 관리할 수 있게 해줍니다. 각각의 댓글은 별도의 GitHub Issue로 기록되어 이슈의 강력한 트래킹 및 관리 기능을 활용할 수 있습니다.
3. 간편한 통합
- Utterances는 간단한 JavaScript 코드를 통해 블로그나 웹사이트에 쉽게 통합될 수 있습니다. 별도의 댓글 서버나 데이터베이스 설정이 필요 없으며, 몇 줄의 코드만으로 댓글 시스템을 도입할 수 있습니다.
4. 보안 및 권한 관리
- GitHub 계정 인증을 사용하기 때문에 댓글 작성자를 GitHub의 계정으로 식별할 수 있습니다. 이는 댓글의 보안을 높이고, 권한 관리를 GitHub에서 직접 수행할 수 있도록 합니다.
5. 데이터 백업 및 이전 가능
- Utterances를 사용하면 댓글이 GitHub Issue로 저장되기 때문에 데이터의 백업이 간편합니다. GitHub 이슈를 다른 저장소로 이전하면 댓글 데이터를 손쉽게 옮길 수 있습니다.
6. 테마 설정 가능
- Utterances는 몇 가지 테마를 제공하며, 블로그 테마에 적합한 스타일을 선택할 수 있습니다. github-light와 github-dark 테마 중 선택할 수 있습니다.

## 블로그에 Utterance를 이용하여 댓글 기능 추가하기
### 1. GitHub 저장소 생성:
- Utterances를 사용하기 위해서는 GitHub 저장소가 필요합니다. 댓글을 저장할 저장소를 만들어 주세요.
저는 별도의 저장소를 만들지 않았고 현재 깃허브 블로그 Repository를 이용했습니다 (Repository는 Public으로 만들어주세요.)

### 2. Utterances 앱 설치 및 스크립트 추가
1.  [링크로 이동하여](https://github.com/apps/utterances) Utterances 앱을 GitHub에 설치합니다 Utterances GitHub 앱은 댓글을 저장소의 Issue로 매핑시켜주는 역할을 합니다.
2. 위 링크로 이동했으면 Learn more at https://utteranc.es을 눌러 다시 한 번 이동합니다.
- ![Utterances.png](images/utteranc.png)
3. 그러면 이러한 화면이 보여질 것인데 repo: 부분에 댓글을 저장할 저장소의 주소를 입력해주세요 (github아이디/저장소이름)
4. Blog Post - Issue Mapping   부분에서
블로그의 개별 포스트와 GitHub Issue를 연결하는 방식을 결정해주세요 저 같은 경우는 맨 위 **issue title contains page pathname**을 선택했습니다.
5. 그 후 자신이 원하는 테마를 선택하면
- ![.Utterances.png](images/utteranc2.png)
6. 이러한 <Javascript> 태그를 생성해 줍니다 Utterances를 블로그에 통합하기 위해 블로그 템플릿에 생성된 코드를 추가해줍니다 저 같은 경우에는 **_layout/post.html** 부분에 생성된 <Javascript> 태그를 추가했습니다

### 3. 변경 사항 반영
1. 적용한 내용을 반영하기 위해 터미널에서
```bash
git add .
git commit -m "Utterance 댓글 기능 추가"
git push -u origin main
``` 
를 입력하여 저장소에 푸시합니다

### 4. 댓글 기능 확인
- 블로그 주소로 들어가 정상적으로 댓글 위젯이 작동하는지 확인합니다.

- ![Utterances3.png](images/utteranc3.png)
- ![Utterances4.png](images/utteranc4.png)

- 정상적으로 작동하는 것을 확인할 수 있습니다.
