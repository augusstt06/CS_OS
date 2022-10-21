> 이 글은 "혼자 공부하는 컴퓨터 구조 + 운영체제"를 읽고 이해한 내용을 복습하기 위해 작성하는 글입니다.

> 이미지 출처 : 혼자 공부하는 컴퓨터 구조 + 운영체제

## 보조 기억 장치

### 1. 하드디스크 / 플래시 메모리

1. 하드 디스크 (자기 디스크)

   - 자기적 방식으로 데이터를 저장하는 보조기억장치

2. 플래시 메모리

   1. SLC 타입

      - 한 셀에 1 비트를 저장할 수 있는 메모리

      - 한 셀로 2개의 정보를 표현 가능 / 다른 타입에 비해 빠른 입출력 가능

   2. MLC 타입

      - 한 셀로 4개의 정보 표현 가능

   3. TLC 타입

      - 한 셀로 8개의 정보 표현 가능

   ![플래시 메모리](https://velog.velcdn.com/images/cnffjd95/post/108421c2-6384-41fa-8039-5b2675761c17/image.jpg)

### 2. RAID

- 주로 하드디스크와 SSD를 사용하여 여러개의 물리적 보조 기억장치를 하나의 논리적 보조기억장치로 사용하는 기술

* RAID 레벨

1. RAID 0

   - 데이터를 저장할때 여러 하드 디스크에 번갈아가며 데이터를 저장

   - 하드 디스크 중 1개라도 문제가 생기면 다른 하드 디스크의 정보를 읽는데 문제가 생긴다.

2. RAID 1

   - 하드디스크의 복사본을 만들어 저장하는 방식

   - 원래의 하드디스크와 복사본 모두 데이터를 저장한다.

   - 하드 디스크 갯수가 한정 되었을때 사용가능한 용량이 적어진다.

3. RAID 4

   - RAID 1처럼 복사본을 만들어서, **오류검출/복구를 위한 정보(패리티 비트)**를 저장한 장치를 둔다.

   - RAID 1보다 적은 하드 디스크로 안전하게 데이터를 보관한다.

   - 데이터를 저장할때 마다 패리티 디스크에도 데이터를 작성하므로, 병목현상이 발생한다.
     ![RAID 4](https://velog.velcdn.com/images/cnffjd95/post/98e5905b-14ba-4e99-8618-372d59332b3c/image.jpg)

4. RAID 5

   - RAID 4의 단점을 보완하기 위해 하드디스크마다 패리티를 둔다.

   - 패리티를 분산 저장하여 병목현상 해결
     ![RAID 5](https://velog.velcdn.com/images/cnffjd95/post/20071289-0899-4018-8108-aeb362610cb4/image.jpg)

5. RAID 6

   - 기본적으로 RAID 5와 같다.

   - 서로 다른 2개의 패리티를 둔다.

   - 새로운 정보를 저장할때마다 함께 저장할 패리티가 2개이므로 RAID 5보단 느리다.

   ![RAID 6](https://velog.velcdn.com/images/cnffjd95/post/7db1ab15-fe7a-45ff-bf3f-3132b16436b3/image.jpg)