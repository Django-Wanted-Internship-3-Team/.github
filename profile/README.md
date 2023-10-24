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
  <img src="https://img.shields.io/badge/django 4.2.6-092E20?style=for-the-badge&logo=django&logoColor=white"> 
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
* git commit title rules [^1]
    * feat : 새로운 기능 추가
    * fix : 버그 수정
    * docs : 문서 수정
    * style : 코드 포맷팅, 세미콜론 누락, 코드 변경이 없는 경우, linting
    * refactor : 코드 리팩터링
    * test : 테스트 코드, 리팩터링 테스트 코드 추가
    * chore : 빌드 업무 수정, 패키지 매니저 수정
* git commit rules
    ```bash
    # example of git conventions
    git commit -m "feat : get_user_infornation 추가

    광고주 정보 호출 기능을 ./advertiser/view.py 내 AdvertiserListView 클래스에 추가
    "
    ```
    * 팀 전원 push or pull request 이후, 리뷰를 진행하도록 한다.
    * 코드 실명제를 통해, assignee, reviewer 확인이 가능할 테지만 특정인의 리뷰 요청이 필요한 경우 issue에서 @{name}으로 호출한 뒤 review를 요청하도록 한다.
    * description은 1~3줄 내외로 작성하도록 한다.
* git branch rules
    * `feature/#{issue_no}-{short-description}` 예) `feature/#5-test-code`
    * 작업 전 issue 를 생성한다.(issue엔 assignees, labels, project, milestone이 포함되어야 함)
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
* git fork rules
    * 종료된 일감의 추가 수정 혹은 다른 기능 개발이 필요하다고 판단될 때엔 `fork`해서 진행하도록 합니다.
    ```bash
    # 이때 $FORKED_REMOTE_NAME은 organization remote name과 겹치지 않도록 함.
    git remote add $FORKED_REMOTE_NAME $FORKED_REPO_URL
    git checkout -b $BRANCH_NAME
    # push 전 orgarnization에서 변동된 내용이 반영되어있다면 fetch upstream으로 conflict 발생 지점을 해결 필요함. 
    git push -u $FORKED_REMOTE_NAME $BRANCH_NAME
    ```

* git issue rules
    
   <span style="color:#888888">이슈 생성 규칙과 프로젝트 관련해서는 추가 협의 후 다시 정리하겠습니다.</span>
> ### Code
* linting: [PEP8](https://peps.python.org/pep-0008/)
* code formatation rules
    * 과제에서 추가 요구 사항이 없는 한, `class`명은 UpperCamelCase를 사용하도록 한다.
    * 과제에서 추가 요구 사항이 없고, 내장 함수가 아닌 경우 `def`명은 snake_case 사용을 지향한다.
* code contribution rules
    * class 하단에 아래와 같이 표기한다. 
    * 리뷰어가 없을 시엔 '-'로 표기한다.
    ```python
    class FisrtFunction:
        """
        Assignee : 이름
        Reviewer : -
        """
        def get_results:
            pass
    ```



---

[^1]: [Git - 커밋 메시지 컨벤션](https://doublesprogramming.tistory.com/256)
