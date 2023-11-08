# 멀티미디어 실습

> 2023 가을학기에 진행한 git 수업 정리

## 2023-10-18
### 저장소
- 일반 폴더와 저장소의 차이는 `.git` 숨김폴더가 없냐 있냐이다.
  - 일반 폴더는 `.git` 숨김폴더가 없음
  - 저장소는 `.git` 숨김폴더가 있음
- `.git` 숨김폴더를 삭제하면 커밋 이력등도 같이 삭제됨

### 브랜치
- 브랜치 <-- 커밋을 가리키는 포인터
- 이슈를 만들고, 이슈에 해당하는 브랜치를 생성
  - `git branch` <-- 만들어진 브랜치 확인 
  - `git branch 브랜치명` <-- 새로운 브랜치 생성
- 작업을 시작할 땐, 생성한 브랜치로 전환(switch)함
  - `git switch 브랜치명`
  - `git checkout 브랜치명` <--checkout(확인하다, 조사하다)


## 2023-10-04
### 스테이징 영역
- IT프로젝트는 여러 파일을 동시에 다루게된다.

- 일반 문서 수정과 같이 '저장' 버튼 클릭만으로 한번에 수정한 파일들을 저장하게 하면, 불필요한 파일들이 커밋에 포합되는 일들이 발생한다.
  - 예시:
    - `.vs`: visual studio로 프로젝트 열었을 때 자동 생성되는 폴더    
- 그래서 staging area라는 영역을 따로 두고, 커밋에 포함시킬 코드(파일)만 스테이징 영역에 추가하게 한 다음, 커밋을 만든다.
  - 스테이징 영역에 파일을 추가할 때 쓰는 명령어: `git add 파일명`
### gitignore파일
-   루트 경로에 있는 `.gitignore`파일은 버전관리 하지 않을 파일의 목록을 관리하는 용도로 쓰인다.
- 사용하는 운영체제, 에디터, 프로그래밍 언어, SDK, 라이브러리 등의 종류에 따라 사람이 의도하지 않는 파일이 생성되는데, 이런 파일들은 버전관리 대상이 아니므로 `.gitignore` 파일에서 관리한다.
  - 예시: https://github.com/cmilr/Unity2D-Components/blob/master/.gitignore
  - 웹사이트
    - 구글에서 'git ignore generator' 로 검색
      - https://www.toptal.com/developers/gitignore
  - VSCode 익스텐션:
    - gitignore by CodeZombie

## 2023-09-27
- commit이란? git의 기본 단위로, 논리적 변경이 있을때 만듬(사진찍기와 유사)

- commit 메세지
  - 코드 변경분을 요약해서 설명해주는 메시지
- 명령어
  - git commit -m "커밋 메시지를 이곳에 입력"
  - git commit --message "커밋 메시지를 이곳에 입력"
- 얼마나 자주 커밋을 만들어야 하나
  - 너무 작지도, 크지도 않게 한다 (조직에따라, 프로젝트 성격에 따라 다름)
  - 커밋 단위가 너무 작을경우 불필요한 커밋들이 생성됨
  - 커밋 단위가 너무 클 경우 장애 났을 때 빠른 대응이 힘듬
  - 예시: 30분 안에 리뷰 가능하도록 커밋 크기 조절