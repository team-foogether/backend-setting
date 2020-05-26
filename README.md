# backend-setting
backend-setting in fing

## setting
- java 8
- gradle 3
- springboot 2.3.0
  - lombok
  - Spring Data JPA
  - Devtools
  - Spring Web
- MySQL 8
- Workbench 8
- STS 4

> [참고] [eclipse-setting](https://github.com/team-fing/backend-setting/blob/master/eclipse-setting.md)


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
  - (김희운-알람 및 결제 / 권보윤 - SNS로그인, 안나연 - 위치정보) 
     **알람, 결제, 위치정보, SNS 로그인(카카오, 네이버, 구글) API**
  - (이여진) **관리자**
  - (안나연) **모이자**
  - (권보윤) **판매상품**
  - (안나연) **댓글**
  - (권보윤) **후기**
  - (김희운) **공간대여** 
  - (이여진) **사용자 신고(사용자가 신고)**

## event storming
- 파란색 : command
- 진노랑색 : event
- 보라색 및 연노랑색 : Actor
- 초록색 : Aggregate
- 진핑크색 및 빨간색 : outer system & hot issue

<img src="https://user-images.githubusercontent.com/36287324/82732532-c6fe9280-9d48-11ea-84c5-68b520ea790b.jpg" width="90%"></img>


- 회원

    <img src="https://user-images.githubusercontent.com/36287324/82768723-bf83da00-9e6b-11ea-9c1b-db18de6c0a15.jpg" width="70%"></img>

- 마이페이지

  <img src="https://user-images.githubusercontent.com/36287324/82768750-f1953c00-9e6b-11ea-9abb-1ceb35e97274.jpg" width="70%"></img>

- 외부 시스템
  - 알람 및 결제
  - SNS 로그인
  - 위치 정보
  
    <img src="https://user-images.githubusercontent.com/36287324/82768765-fa860d80-9e6b-11ea-8330-cf93e4a10892.jpg" width="70%"></img>

  
- 관리자

  <img src="https://user-images.githubusercontent.com/36287324/82768756-f6f28680-9e6b-11ea-85fa-c925505b39ff.jpg" width="70%"></img>


- 모이자

  <img src="https://user-images.githubusercontent.com/36287324/82768757-f823b380-9e6b-11ea-83ed-eda4579d58a4.jpg" width="70%"></img>


- 판매상품

  <img src="https://user-images.githubusercontent.com/36287324/82768759-f8bc4a00-9e6b-11ea-9a2d-764028442b9e.jpg" width="70%"></img>

- 댓글

  <img src="https://user-images.githubusercontent.com/36287324/82768760-f954e080-9e6b-11ea-94b5-5b1f6137d5cb.jpg" width="70%"></img>

- 후기

  <img src="https://user-images.githubusercontent.com/36287324/82768762-f9ed7700-9e6b-11ea-9159-0c5ec2eeba44.jpg" width="70%"></img>

- 공간대여

  <img src="https://user-images.githubusercontent.com/36287324/82768763-f9ed7700-9e6b-11ea-8a01-880d9515b9cf.jpg" width="70%"></img>

- 사용자 신고

  <img src="https://user-images.githubusercontent.com/36287324/82768764-fa860d80-9e6b-11ea-9d5d-2ae21ef00bdd.jpg" width="70%"></img>

# API 명세서 작성
[API 명세서 목록](https://github.com/team-fing/backend-setting/wiki)

# Domain Modeling
