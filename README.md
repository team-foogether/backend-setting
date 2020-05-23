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

<img src="https://user-images.githubusercontent.com/36287324/82732532-c6fe9280-9d48-11ea-84c5-68b520ea790b.jpg" width="90%"></img>


# API 명세서 작성

# Domain Modeling
