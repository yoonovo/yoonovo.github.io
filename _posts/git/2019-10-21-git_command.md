---
layout: post
title:  "Git 명령어"
date:   2019-10-21 11:15:29 +0900
categories: Git
---

- __Git init__ : 새로운 프로젝트를 만들었을때 새로운 git 저장소를 만들어준다.

- __Git clone "원격 저장소 URL"__ : github나 gitlab에 올라가 있는 프로젝트를 복사해 가져오는 명령어이다.

- __Git branch "브랜치 이름"__ : 새로운 브랜치 추가

- __Git checkout "브랜치 이름"__ : 브랜치 이동

- __Git branch -D "브랜치 이름"__ : 브랜치 삭제

- __Git add "파일명"__ : 변경된 내용을 스테이징에 추가한다. 파일명은 경로까지 넣어야한다. 변경된 모든파일을 한번에 추가하고 싶다면 <span style="color:red;">git add .</span>로 입력하면된다.

- __Git commit -m "커밋메세지"__ : 스테이징에 올라간 내용을 커밋 메세지로 묶어 저장한다.  
<span style="color:red;">git commit -m "커밋 제목" -m "커밋 메세지`</span> 처럼 제목과 내용을 커밋 할 수도 있다.

- __Git commit --amend -m "변경항 커밋 메세지"__ : 바로 전의 저장된 커밋 메세지를 수정한다.  

- __Git push -u origin "브랜치 이름"__ : 원격 저장소에 변경된 내용을 갱신한다. 잘못 push 하게 되면 작업한 내용이 지워질 수 있으니 신중하게 해야된다.

- __Git merge "브랜치 이름"__ : 브랜치를 병합한다. push만큼 위험한 명령어로 이것도 잘못하면 작업내역이 바뀌거나 삭제될수 있으니 신중 해야한다.

- __Git log__ : 커밋된 내역들을 확인할 수 있다.  

- __Git remote -v__ : 원격 저장소의 url을 확인 할 수 있다.

- __Git remote set-url origin "원격저장소 주소"__ : 원격 저장소의 url을 바꿀수 있다.

- __Git remote add "새로운 원격브랜치 명" "원격저장소 주소"__ : 새로운 원격 저장소를 추가한다. 
기본적으론 origin이 생성되어 있다. 그러나 더 체계적으로 Git을 관리하고 싶다면 
공용 원격 저장소와 개인 원격 저장소로 나누어 관리하는 방법이 있는데 그때 사용하는 명령어 이다.
