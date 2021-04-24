Git Page 
https://github.com/mdn/django-locallibrary-tutorial

@@가상환경 실행하기!!
cd C:\#Project\GIT\etcProject\DjangoWep\venv\Scripts
activate.bat

================2021-04-24================
#####################
##5. 홈페이지 만들기
https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Home_page




#####################
##4. 관리사이트 생성
https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Admin_site
관리자 생성 및 데이터 관리, 내부 UI, 데이터 바인딩에 대한 내용이 담겨있음


관리자를 생성해준다.
python3 manage.py createsuperuser

kjky12/kjky123@naver.com/!QAZ2wsx




#####################
##3. 모델 생성
https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models

model파일에 작업하며 소스코드의 정보를 통해 데이터베이스를 생성해줌.
특징으로는 모델이 바뀔때마다 해줘야함, 정의된 정보로 새로 구조가 구축되기 때문

py manage.py makemigrations
py manage.py migrate


================2021-04-22================
#####################
##2. 실제 프로젝스 생성
https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/development_environment

1. 실제 사용할 프로젝트 경로 생성
mkdir django_projects
cd django_projects

2. 프로젝트 
django-admin startproject locallibrary
cd locallibrary

3. 앱(카탈로그) 생성 -> 이게 페이지 인듯
py manage.py startapp catalog
아래와 같은게 생김
views.py, models.py, tests.py, admin.py(관리 사이트), apps.py(애플리케이션)
migrations(데이터 베이스)

4. 추가한 앱 등록
settings.py를 열고INSTALLED_APPS에 추가!!
    # Add our new application
    'catalog.apps.CatalogConfig', #This object was created for us in /catalog/apps.py


5. 데이터 베이스 셋업 관련
python3 manage.py makemigrations : 설치된 모든 애플리케이션에 대한 마이그레이션을 생성 하지만 적용하지는 않습니다. 
python3 manage.py migrate : 데이터베이스에 마이그레이션을 적용하는 것입니다(sqlite가 생성됌)

5. 장고 서버 실행
py manage.py runserver

#####################
##1. 개발환경 셋팅 및 장고 프로젝트 생성테스트
https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/skeleton_website

1. 장고 설치
pip3 install django

2. 장고 버전 확인
py -m django --version

3. 장고관련 테스트 폴더 생성 및 이동
mkdir django_test
cd django_test

4. 장고 기본 틀 생성
django-admin startproject mytestsite
cd mytestsite

5. 장고 서버 실행
py manage.py runserver