![원티드 프리온보딩 백엔드 코스](https://static.wanted.co.kr/images/events/3178/58ac3248.jpg)

# Intro
<div align="center">

| name | title | profile link | email |
|------|-------|--------------|-------|
| 윤성원 | 팀장 | [@lfoyh6591](https://github.com/lfoyh6591) | lfoyh6591@naver.com |
| 사재혁 | 팀원 | [@saJaeHyukc](https://github.com/saJaeHyukc) | wogur981208@gmail.com |
| 박대준 | 팀원 | [@Chestnut90](https://github.com/Chestnut90) | cowzon90@gmail.com |
| 이슬기 | 팀원 | [@simseulnyang](https://github.com/simseulnyang) | happysseul627@gmail.com |

</div>
</br>

안녕하세요. 

원티드에서 진행하는 <large>**프리온보딩 백엔드 코스 C팀**</large>입니다.

저희가 과제 수행 시에 기술스택, 수행해야 할 과제 정보 및 진행 현황, 프로젝트를 진행하고 지키고자 협약한 규칙에 대한 내용이 정리된 다음의 목차를 클릭하시면 원하시는 내용을 확인할 수 있습니다.

</br>

* [Tech](#tech)
* [Projects](#projects)
* [Conventions](#conventions)
    * [Git](#git)
    * [Code](#code)

</br>

---
## Tech
</br>
<div align="center">
  
  <img src="https://img.shields.io/badge/python 3.11.5-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/django 4.2.5-092E20?style=for-the-badge&logo=django&logoColor=white"> 
  <img src="https://img.shields.io/badge/django rest framework 3.14.0-092E20?style=for-the-badge&logo=django&logoColor=white">
</div>
</br>

---
## Projects

* [MADUP](https://github.com/PreOnboarding-Team-C/Madup)
    * [Github Project | Madup](https://github.com/orgs/PreOnboarding-Team-C/projects/1/views/2)
    * [Trello | Madup](https://trello.com/b/s0PLzIuF/madup) 

</br>

---
## Conventions
> ### Git
* git commit title rules
    * :tada:Init: 프로젝트 개시
    * :sparkles:Feat : 새로운 기능 추가
    * :bug:Fix : 버그 수정
    * :fire:Remove : 코드 삭제
    * :memo:Docs : 문서 수정
    * :white_check_mark:Test : 테스트 코드, 리팩토링 테스트 코드 추가
    * :recycle:Refact : 코드 리팩토링
    * :rocket:Deploy : 배포
    * :hammer:Chore : 빌드 업무 수정, 패키지 매니저 수정
* git commit message tempaltes
    ```bash
   ################
   # <타입> : <제목> 의 형식으로 제목을 아래 공백줄에 작성
   # 제목은 50자 이내 / 변경사항이 "무엇"인지 명확히 작성 / 끝에 마침표 금지
   # 예) :sparkles:Feat : 로그인 기능 추가 # 이슈번호
   
   # 바로 아래 공백은 지우지 마세요 (제목과 본문의 분리를 위함)
   
   ################
   # 본문(구체적인 내용)을 아랫줄에 작성
   # 여러 줄의 메시지를 작성할 땐 "-"로 구분 (한 줄은 72자 이내)
   # '왜'라는 것에 초점을 맞춰 작성
   
   ################
   # 꼬릿말(footer)을 아랫줄에 작성 (현재 커밋과 관련된 이슈 번호 추가 등)
   # 해결 -> Closes(종료), Fixes(수정), Resolves(해결)
   # 참고 -> Ref(참고), Related to(관련), See also(참고)
   # 예) Close #7
   
   ################
   # :tada:Init: 프로젝트 개시
   # :sparkles:Feat : 새로운 기능 추가
   # :bug:Fix : 버그 수정
   # :fire:Remove : 코드 삭제
   # :memo:Docs : 문서 수정
   # :white_check_mark:Test : 테스트 코드, 리팩토링 테스트 코드 추가
   # :recycle:Refact : 코드 리팩토링
   # :rocket:Deploy : 배포
   # :hammer:Chore : 빌드 업무 수정, 패키지 매니저 수정
   ################

    "
    ```
    * 팀 전원 feature -> develop branch에서 PR 이후, 리뷰를 진행하도록 한다. (팀원 전원)
    * 코드 리뷰 과정에서 이루어지는 것
      - 일관된 아키텍처를 유지하고 있는지
      - 다른 해결 방법에 대한 의견 제시
      - 버그가 발생할 수 있는 가능성 제시
      - 기술적인 지식, 노하우 공유
      - 히스토리 전달
* git branch rules
    * `feature/#{issue_no}-{short-description}` 예) `feature/#5-test-code`
    * 작업 전 issue 를 생성한다.(issue엔 assignees, label이 포함되어야 함)
    * short description의 공백은 '-'로 대체하고, 3 단어 내외로 간단한 업무 설명을 영어로 기재한다.
    * branch의 head는 `main`으로, `main`에서 브랜치를 생성하고, `pull request` 요청 전 코드 리뷰를 받아야 한다.
    ```bash
    # checkout 전 branch는 main이어야 함.
    git checkout -b $BRANCH_NAME
    ```
    * 리뷰 요청에 따라 수정 혹은 동의를 얻을 시 `merge`가 가능하다.(단, `merge`는 팀장만 가능하다.)
    * `merge`후 local과 remote에 생성된 해당 브랜치는 삭제하도록 한다.
    ```bash
    git branch -D $BRANCH_NAME
    git push origin --delete $BRANCH_NAME
    ```
* git issue or bug rule
    * 템플릿에 맞게 작성한다.
    
> ### Code
* linting: [PEP8](https://peps.python.org/pep-0008/)
* code formatation rules
    * 과제에서 추가 요구 사항이 없는 한, `class`명은 UpperCamelCase를 사용하도록 한다.
    * 과제에서 추가 요구 사항이 없고, 내장 함수가 아닌 경우 `def`명은 snake_case 사용을 지향한다.
    * 최대한 코드 일관성을 유지하기 위해 pre-commit을 사용한다 (black, isort, flake8)
---
