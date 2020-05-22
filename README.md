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

