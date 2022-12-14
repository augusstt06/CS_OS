> 이 글은 "혼자 공부하는 컴퓨터 구조 + 운영체제"를 읽고 이해한 내용을 복습하기 위해 작성하는 글입니다.

> 이미지 출처 : 혼자 공부하는 컴퓨터 구조 + 운영체제

## 교착상태

### 1. 교착상태란?

- 일어나지 않을 사건을 기다리며 진행이 멈춰버리는 현상
  ![교착상태](https://velog.velcdn.com/images/cnffjd95/post/a2fedbef-11a8-4f98-a3da-e76be52c738f/image.jpg)
- 자원할당 그래프로 표현이 가능
  - 프로세스-원, 자원의 종류-사각형
  - 사용가능한 자원의 갯수는 사각형 내 점으로 표현
  - 프로세스가 어떠한 자원을 할당받아 사용중이라면, 자원에서 프로세스로 화살표
  - 프로세스가 어떤 자원을 기다리고 있으면 프로세스에서 자원 화살표
    ![교착그래프](https://velog.velcdn.com/images/cnffjd95/post/edeff429-9333-4f80-98bb-f515be6e6cab/image.jpg)
- 교착상태가 발생하는 이유
  - 상호배제
    - 한 프로세스가 사용하는 자원을 다른 프로세스가 사용 할 수 없을때
  - 점유/대기
    - 프로세스가 자원을 보유한채 다른 자원을 기다렸기 때문
    - 자원을 할당받은 상태에서 다른 자원의 할당을 기다리는 상태
  - 비선점
    - 자원을 사용하는 프로세스의 작업이 끝나야지만 이용이 가능하기 때문
    - 어떤 프로세스도 다른 프로세스의 자원을 가져오지 못했기 때문.
  - 원형대기
    - 자원 할당 그래프가 원의 형태로 그려지는 것

### 2. 교착 해결법

#### 1. 예방

- 상호배제, 점유/대기, 비선점, 원형대기 4가지의 조건을 만족시키지 않게 할당.
- 상호배제
  - 모든 자원을 공유가능하게 한다는 것. 현실적으로 무리
- 점유/대기
  - 자원의 활용률이 낮아질수 있음.
    - 당장 자원이 필요해도 기다리는 프로세스, 사용되지 않으면서 장기간 할당되는 자원이 발생
- 비선점
  - 모든 자원이 선점가능하지 않기에 범용성의 문제
- 원형대기
  - 모든 자원에 번호를 붙이고 오름차순으로 자원을 할당하면 가능
  - 시스템 내에 모든 자원에 어떤번호를 붙이는지에 따라 특정자원의 활용률이 저하 될 수 있음

#### 2. 회피

- 안전 상태
  - 교착 없이 안전하게 프로세스 들에게 자원을 할당 할 수 있는 순서(안전순서열)가 배정된 상태
- 불안전 상태
  - 안전순서열이 없는 상황
