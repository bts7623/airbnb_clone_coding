# airbnb_clone_coding

Cloning Airbnb with Python, Django, Tailwind and more...

# History

#### 2020.03.27: #0 Introduction

# Concept

#### #0.0 ~ #0.5 Introduction

- 대충 이번 프로젝트를 왜 장고를 이용하는지에 대한 내용
- 이번 프로젝트는 VSCode와 Django를 통해 만든다.
  - VSCode는 모든 언어에 사용할 수 있고 무료이다.
  - 파이썬 프로그램은 Flask 등의 IDE?가 있는데 해당 Tool은 Micro Project 등을 만들 때 존다.
- Django는 다양한 Module과 Template을 제공해서 대부분의 기능을 쉽게 끌어다 쓸 수 있다.
  - 로그인 ,사용자 인증, 이메일 인증, 보안 등
- Django는 큰 프로젝트를 만드는데 적합하고 때에 따라 Django의 룰을 강제로 따라야한다.
- 다이나믹한 Front가 아니면 React를 꼭 쓰지 않아도 되고 이번 경우는 Django가 더 적합하다.

---

### #1 Environment Setup

#### #1.0 The Package Installer for Python

- pip : Package Installer for Python
  - pip를 쓸 경우 PC에 global로 설치한다.
  - 이는 추후 다른 버전의 장고를 깔았을 때 버전 충동로 프로젝트를 손상시킨다.
- pipenv를 사용하여 global하게 설치하지 않고 설치할 수 있다. (다음 강에서 진행)
  - 이는 하나의 PC에 다양한 버전의 장고를 설치할 수 있고 각각의 버전에서 프로젝트를 돌릴 수 있다.
  - 하지만 pip를 통해 설치를 하게 되면 그것이 불가능하다.
  - react, nodeJS쪽에서는 npm이라는 녀석이 같은 기능을 하는 것 같다.

#### #1.1 Meet Pipenv

- 패키지 관리 세계의 최고들을 가져오는 것 목표로 함(nodeJS의 npm, Rust의 cargo 등의 역할을 하고자하는듯)
- 위와 같은 패키지 매니저가 없던 파이썬을 위해 만든 패키지 매니저가 Pipenv
- global로 설치되지 않고 버블에다가 패키지를 설치함
- pip install --user pipenv를 이용해서 pipenv를 global로 설치하고 pipenv를 이요하여 장고를 버블설치한다.
- pip environment 의 준말인듯
- 참고 링크
  - [Pipemv Doc](https://pipenv-fork.readthedocs.io/en/latest/)

#### #1.2 Creating our Env and Installing Django

- Project를 생성할 폴더를 만들고 해당 폴더에서 pipenv --three 를 입력해서 가상환경을 만든다.
  - three는 Python 3.xx버전으로 한다는 것이다.
- 해당 폴더안에 Pipfile이 생성된다.
- 'code .'을 입력해서 해당 폴더를 VSCode로 열면 Pipfile이 있다.
- 현재 우리는 가상공간을 생성하였고 그 안에 버블에 접근해야한다.
  - VSCode에서 Terminal을 열어서 pipenv shell을 입력하여 들어가준다. > 버블 안에 들어왔다.
  - 버블 안에 들어온 상태에서 DJango를 설치해준다.
- pipenv install Django==2.2.5
  - 2020.03.30 기준 DJango의 버전은 3.이 넘어갔지만 강좌 수강을 위해 2.2.5버전을 설치한다.
  - 버전을 입력하지 않으면 최신버전으로 설치된다.
- Django가 설치되면 Pipfile에 Package에 표기된다.
  - Terminal에 django-admin을 입력해서 설치를 확인한다.
- 기타
  - powershell, cmd에서 명령어 'code'를 치면 VSCode가 열린다. 'code .'을 입력하면 해당 폴더를 VSCode로 연다.

#### #1.3 Creating the Github Repository

- GitHub에 Repository 생성해서 올리는데, 니콜라스는 다 명령어로 하네 흠..
- git init 하고 .gitignore 파일 생성해서 commit
- 참고 링크
  - [gitignore python](https://github.com/github/gitignore/blob/master/Python.gitignore)
