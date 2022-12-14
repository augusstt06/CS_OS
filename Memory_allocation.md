> 이 글은 "혼자 공부하는 컴퓨터 구조 + 운영체제"를 읽고 이해한 내용을 복습하기 위해 작성하는 글입니다.

> 이미지 출처 : 혼자 공부하는 컴퓨터 구조 + 운영체제

## 연속 메모리 할당

### 1. 연속 메모리 할당이란

- 프로세스에 연속적인 메모리 공간을 할당하는 방식

1. 스와핑

   - 메모리에 적재된 프로세스 중 오랫동안 사용되지 않은 프로세스들을 임시로 보조기억장치 영역(**스왑 영역**)으로 보내고 생긴 공간에 다른 프로세스를 배치하는 것.
   - 프로세스 : 메모리 > 스왑영역 : 스왑 아웃
   - 프로세스 : 메모리 < 스왑영역 : 스왑 인

   ![스와핑](https://velog.velcdn.com/images/cnffjd95/post/f0907333-199a-4e0f-bf79-1bb67fe89b07/image.jpg)

2. 메모리 할당
   1. 최초 적합
      - 운영 체제가 메모리 내의 빈 공간을 순서대로 검색 하다가 적재 가능한 공간이 발견되면 프로세스를 배치하는 것.
      - 검색의 최소화, 빠른 할당
   2. 최적 적합
      - 운영체제가 모든 빈 공간을 검색한 후에 프로세스가 적재될 수 있는 **가장 작은 공간**에 배치하는 것.
        ![최적](https://velog.velcdn.com/images/cnffjd95/post/93b7db83-ba6d-4d30-b91d-58c3229e9b55/image.jpg)
   3. 최악 적합
      - 운영체제가 모든 빈 공간을 검색 한 후에 프로세스가 적재될 수 있는 **가장 큰 공간**에 배치하는 것.
        ![최악](https://velog.velcdn.com/images/cnffjd95/post/1780fe4b-60d4-4089-ad33-23b48a2d576b/image.jpg)
   - 외부 단편화
     - 프로세스들이 연속적으로 할당되는 환경에서는 메모리들 사이의 빈 공간이 생성 되는데, 그 공간보다 큰 프로세스들을 적재하기 어렵기 때문에 메모리 낭비로 이어지는 것.
