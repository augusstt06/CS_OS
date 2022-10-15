## Computer Structure & Operating System

> "혼자 공부하는 컴퓨터구조 + 운영체제" 책을 공부하며 정리하는 Repository

1. Data

   - 정보 단위

     1. Bit (비트) : 0,1을 나타내는 가장 작은 정보 단위

     2. n 비트는 2 \*\* n가지의 정보를 표현 가능하다.

   - 2진법, 16진법

     1. 2진법

        - 0, 1로 모든 수를 표현하는 방법

        - 2진법에서의 음수 표현은 2의 보수를 구하여 해당 값을 음수로 표현한다.

        - 2진법 숫자의 모든 0,1을 뒤집고 1을 더한다.

        - 장점
          - 하나의 이진수는 하나의 비트로 표현할수 있기 떄문에 컴퓨터가 이해하는 정보를 직접적으로 표현 가능
        - 단점
          - 0,1로 모든 숫자를 표현하다 보니 자릿수가 매우 길어지는 단점

     2. 16진법
        - 2진법의 단점을 보완하기 위해 사용한다.
        - 2진수 > 16진수, 16진수 > 2진수로 변환이 용이하여 사용한다.

   - 문자 집합

     - 컴퓨터가 인식/표현할 수 있는 문자의 모음

     - 문자 인코딩

       - 문자 집합에 속한 문자를 0,1로 변환하여 컴퓨터가 이해할 수 있는 문자로 변환하는 과정

     - 문자 디코딩
       - 0,1로 이루어진 문자코드를 사람이 이해할 수 있는 문자로 변환하는 과정
     - 표준 인코딩 방식
       - 유니코드 문자 집합 (UTF-8)
         - UTF-8로 인코딩한 결과의 바이트는 유니코드 문자에 붕될 값의 범위에 따라 달라진다.

   - 프로그래밍 언어

     > 고급언어로 작성된 코드가 실행되려면 반드시 저급언어(명령어)로 변환되어야 한다.

     - 고급 언어

       > 실행 속도 : 컴파일 언어 > 인터프리터 언어

       - 사람이 이해하고 작성하기 쉽게 만들어진 언어
       - 종류

         1. 컴파일 언어

            - 컴파일러에 의하여 소스코드 전체가 저급언어로 변환되어 실행되는 언어 ( ex :
              C언어 )

            - 소스코드 > 컴파일러에 의한 컴파일 > 목적코드 (저급언어)

            - 소스코드를 탐색하는 중, 오류가 있다면 컴파일에 실패한다.

         2. 인터프리터 언어

            - 인터프리터에 의하여 소스코드가 한줄 씩 실행되는 언어 ( ex : Python )

            - 인터프리터 :소스코드를 한 줄씩 저급언어로 변환하여 실행 해 주는 도구

            - 한 줄씩 실행하여 변환하기 때문에 전체 컴파일을 기다릴 필요가 없다.

            - 컴파일 언어와 다르게, 소스코드 내 오류코드 직전까지는 정상적으로 실행된다.

     - 저급 언어

       - 컴퓨터가 직접 이해하고 실행 할 수 있는 언어

       - 종류

         1. 기계어

            - 0,1의 명령어 비트로 이루어진 언어 (명령어 모음)

         2. 어셈블리어

            - 기계어는 오로지 컴퓨터만을 위해 만들어 졌기 때문에 보다 쉽게 사람이 이해하기 위해 만들어진 언어

   * 목적파일 / 실행 파일
     - 목적 파일 : 목적 코드로 이루어진 파일
     - 실행 파일 : 실행 파일로 이루어진 파일
     - 링킹 : 목적 파일에 없는 기능들을 해당 목적파일과 연결하는 과정

2. CPU 작동원리

   - ALU : 레지스터를 통해 피연산자를 받아들이고, 제어신호를 받아들인다.

     - 결괏값을 메모리가 아닌 레지스터에 저장한다.

     - 결과 계산 값과 플래그를 내보낸다 ( 플래그 : 연산 결과에 대한 추가적인 정보상태)

     - 플래그 들은 플래그 레지스터라는 레지스터에 저장된다.

   - 제어장치 : 제어신호를 내보내고 명령어를 해석하는 부품

     1. 클럭 신호를 받아들인다

     2. 해석해야 할 명령어를 받아들인다

     3. 플래그 레지스터 속 플래그 값을 받아 들인다.

     4. 시스템 버스(제어버스)로 전달된 제어신호를 받아들인다.

   - 레지스터 :