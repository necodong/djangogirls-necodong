# NDC 챌린지 넥러닝 강의 목차

NDC 챌린지 용으로 만드는 김에 새싹반에서도 쓸 수 있도록 해보자
Django girls tutorial을 기반으로 진행

## 인터넷이란 무엇인가

약 10분 정도

https://tutorial.djangogirls.org/ko/how_the_internet_works/

먼저 인터넷이란 여러 서버, 수많은 컴퓨터들의 네트워크라는 점을 설명하기
다른 나라와 이렇게 빠르게 인터넷을 할 수 있는 이유는 해저 케이블이 있다는 점도 설명
웹 브라우저에 주소를 입력하거나 링크를 클릭하면 무슨 일이 일어나는지

(넥슨 직원들의 수준을 믿고 좀 더 기술적으로 가보기)

에를 들어 주소 창에 nexon.com을 입력할 경우 .com 에 등록되어 있는 사이트 목록을 가지고 있는 서버가 있음 이 서버에게 google.com의 IP 주소를 물어보게 됨
해당 서버가 nexon.com 의 IP 주소를 알려주면 웹 브라우저는 그쪽으로 요청을 보내게 된다.

이러한 시스템을 Doman Name System (DNS) 라고 함

웹 브라우저가 nexon.com 서버 IP 주소를 알아내어 성공적으로 요청을 받았다면 HTML이라는 텍스트를 받게 됨
여기서 curl 등을 이용해 https://www.nexon.com/Home/Game 의 HTML을 받는 걸 보여줘도 좋을 것 같다

이 HTML을 사람이 볼 수 있도록 표현하는 것이 웹 브라우저가 하는 일임


## Django 개발 환경 세팅하기

### 공통으로 vscode 설치하기

Visual Studio Code (vscode)는 Microsoft에서 개발한 무료 오픈소스 에디터로 요즘 개발자들이 가장 많이 사용하는 애디터 중 하나입니다.
이번 과정에서도 vscode를 사용하게 됩니다.

https://code.visualstudio.com/Download 에서 실행 파일을 다운로드하여 설치하면 됩니다.

## 커맨드라인 시작하기

https://tutorial.djangogirls.org/ko/intro_to_command_line/

이미 vscode을 설치했으므로 vscode을 열어서 터미널을 사용할 수 있음

상단 메뉴 바 터미널 -> 새 터미널을 통해 터미널을 열 수 있음

터미널을 열었으면 본격적으로 파이썬을 설치해본다

터미널을 시작하기 전에 알아둬야 할 것이 몇 가지 있음

1. 프롬프트 

명령 프롬프트라면 C:\(사용자 이름)>

맥이라면 ~ 으로 시작하면서 커서가 깜빡거리고 있음
이것을 프롬프트라고 하며 이 상태에서 원하는 명령어를 입력하면 됩니다.

2. 터미널은 탐색기 or finder의 역할을 함

윈도우애서 파일을 열거나 관리하기 위헤셔 탐색기라는 프로그램을 이용하게 되는데 터미널은 이 탐색기의 역할을 하게 됨

윈도우에서는 cd 맥에서는 pwd 임

https://tutorial.djangogirls.org/ko/intro_to_command_line/

을 한 번 따라해본다


## 파이썬 설치하기 (Windows)

현재 파이썬은 3.10 버전까지 출시되었으나 장고 걸스 튜토리얼에서는 편의상 3.6 버전을 사용하게 됩니다.

## Django 개발 환경 세팅하기 (Mac)

Mac에는 이미 파이썬이 설치되어 있지만 맥북의 종류에 따라 파이썬 버전이 다릅니다. 따라서 python 3.11 버전을 따로 설치해줘야 합니다.
먼저 homebrew가 설치되어 있지 않다면 터미널에 아래 명령어를 입력하여 설치합니다.

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

다음 brew install python@3.11 을 해서 파이썬 3.11을 설치합니다.

파이썬을 설치했다면 

python3 -m venv myvenv 를 해서 파이썬 가상환경을 만들어줍니다 (가상환경에 대한 설명 필요)

venv는 파이썬3부터 추가된 virtualenv 를 설치하지 않아도 가상환경을 만들어주는 도구입니다.
여기까지 했다면 맥에서는 source myvenv/bin/activate 를 통해 가상환경을 활성화 할 수 있습니다
프롬프트 왼쪽에 (myvenv) 라고 뜨면 성공입니다.

