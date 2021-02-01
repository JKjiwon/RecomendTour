# RecomendTour (여행지 추천 Rest API)
## 프로젝트 소개
* Django를 이용한 회원(User), 여행지(Lcation) 정보 저장용 REST API 구현
* 여행지 정보에 대한 CRUD 시스템 구현
* JWT 토큰을 이용한 Authentication 및 Authorization 구현

## 코드 다운로드
Clone the repository
`git clone https://github.com/JKjiwon/RecomendTour.git`


## project dependencies 설치

First create virtualenv, then enter the following command
먼저 pipenv를 통해 가상환경을 구성하고, 다음 명령어를 입력하세요

`pipenv install -r requirements.txt`

`pipenv install -r requirements-dev.txt --dev`

## 데이터 베이스 설치

`python manage.py makemigrations`

`python manage.py migrate`


## 서버 실행
`python manage.py runserver` **http://0.0.0.0:8000/** 로 접근

## End Points
* 인증( JWT Token) 발급 및 갱신 관련
|  <center>HTTP</center> |  <center>Path</center> |  <center>Permission</center> |  <center>목적</center> |
