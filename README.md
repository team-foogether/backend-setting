# backend-setting
backend-setting in fing

## setting
- java 8
- maven 3.6.3
- springboot 2.3.0
  - lombok
  - Spring Data JPA
- MySQL 8
- Workbench 8


## structure
`[] : package`
`** : 이름`
```
[web]
  - [controller]
  - [dto]
     - **ResponseDto.java
     - **RequestDto.java
  - [domain]
     - [User] - example
         - User.java
     - [Board] - example
         - Board.java
  - [service]
     - **ImpleService.java
     - **Service.java
  - [config]
     - [dto]
     - **Config.java
  - [repository]
     - **Repository.java
```


# MicroService 도출
(20.05.23.sat)
이전에 작성한 요구사항 정의서를 바탕으로 마이크로서비스를 도출함.

- 총 10개 서비스(담당자)
  - (김하은) **회원**
  - (이여진) **마이페이지**
  - (김희운-알람 및 결제 / 김하은 - SNS로그인, 안나연 - 위치정보) 
     **알람, 결제, 위치정보, SNS 로그인(카카오, 네이버, 구글) API**
  - (이여진) **관리자**
  - (안나연) **모이자**
  - (권보윤) **판매상품**
  - (안나연) **댓글**
  - (권보윤) **후기**
  - (김희운) **공간대여** 
  - (이여진) **사용자 신고(사용자가 신고)**

## event storming
<img src="https://user-images.githubusercontent.com/36287324/82732532-c6fe9280-9d48-11ea-84c5-68b520ea790b.jpg" width="90%"></img>

- 회원
![2  회원](https://user-images.githubusercontent.com/36287324/82768723-bf83da00-9e6b-11ea-9c1b-db18de6c0a15.jpg)

- 마이페이지
![3  마이페이지](https://user-images.githubusercontent.com/36287324/82768750-f1953c00-9e6b-11ea-9abb-1ceb35e97274.jpg)

- 외부 시스템
  - 알람 및 결제
  - SNS 로그인
  - 위치 정보
  ![4  알람](https://user-images.githubusercontent.com/36287324/82768765-fa860d80-9e6b-11ea-8330-cf93e4a10892.jpg)
  
- 관리자
![5  관리자](https://user-images.githubusercontent.com/36287324/82768756-f6f28680-9e6b-11ea-85fa-c925505b39ff.jpg)

- 모이자
![6  모임](https://user-images.githubusercontent.com/36287324/82768757-f823b380-9e6b-11ea-83ed-eda4579d58a4.jpg)

- 판매상품
![7  판매상품](https://user-images.githubusercontent.com/36287324/82768759-f8bc4a00-9e6b-11ea-9a2d-764028442b9e.jpg)

- 댓글
![8  댓글](https://user-images.githubusercontent.com/36287324/82768760-f954e080-9e6b-11ea-94b5-5b1f6137d5cb.jpg)

- 후기
![9  후기](https://user-images.githubusercontent.com/36287324/82768762-f9ed7700-9e6b-11ea-9159-0c5ec2eeba44.jpg)

- 공간대여
![10  공간대여](https://user-images.githubusercontent.com/36287324/82768763-f9ed7700-9e6b-11ea-8a01-880d9515b9cf.jpg)

- 사용자 신고
![11  사용자 신고](https://user-images.githubusercontent.com/36287324/82768764-fa860d80-9e6b-11ea-9d5d-2ae21ef00bdd.jpg)

# API 명세서 작성

# Domain Modeling
