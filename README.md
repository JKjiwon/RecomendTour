# RecomendTour (여행지 추천 Rest API)
## 프로젝트 소개
* Django를 이용한 회원(User), 여행지(Lcation) 정보 저장용 REST API 구현
* 여행지 정보에 대한 CRUD 시스템 구현
* JWT 토큰을 이용한 Authentication 및 Authorization 구현

## 코드 다운로드
Repository 를 클론

`git clone https://github.com/JKjiwon/RecomendTour.git`


## project dependencies 설치

먼저 pipenv 를 통해 가상환경을 구성하고, 다음 명령어를 입력

`pipenv install -r requirements.txt`

`pipenv install -r requirements-dev.txt --dev`

## 데이터 베이스 설치

`python manage.py makemigrations`

`python manage.py migrate`


## 서버 실행
`python manage.py runserver` **http://0.0.0.0:8000/** 로 접근

## End Points
* 인증( JWT Token) 발급 및 갱신 관련

|HTTP|Path|Permission|목적|
|---|---|---|---|
|POST|/users/login|NONE|로그인 시  JWT Token 반환|
|POST|/users/refresh|JWT Token|JWT Token을 검증 후 새로운  토큰 반환|
|GET|/users/validate|JWT Token|JWT Token을 검증|


* 회원(User) 리소스 관련 API

|HTTP|Path|Permission|목적|
|---|---|---|---|
|POST|/users|NONE|유저 생성|
|GET|/users|JWT Token + SuperUser|모든 유저 정보 조회|
|GET|/users/{id}|JWT Token + SuperUser|{id}의 유저 정보 조회|
|GET|/users/me|JWT Token|요청한 유저의 정보 반환|
|PUT|/users/me|JWT Token|요청한 유저의 정보 수정|
|PUT|/users/me/changepssword|JWT Token|유저 비빌번호 변경
|DELETE|/users/me|JWT Token|요청한 유저의 정보 삭제|

|HTTP|Path|Permission|목적|
|---|---|---|---|
|GET|/users/me/favs|JWT Token|요청한 유저의 좋아하는 여행지 조회

|PUT|/users/me/favs|JWT Token|요청한 유저의 좋아하는 여행지 수정
