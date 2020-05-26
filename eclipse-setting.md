## setting
<img src="https://user-images.githubusercontent.com/36287324/82853870-d137b100-9f41-11ea-97f8-007a972142a5.png" width="35%"/>

Name, Artifact, Description, Package 는 각자에 맞춰서 변경

<img src="https://user-images.githubusercontent.com/36287324/82770058-1db3bb80-9e72-11ea-95dc-169fd61672b5.PNG" width="35%"/>


## h2 의존성 등록
현재 database 연결해놓은 것이 없으니 database 만들기 전까지 메모리 db인 h2 등록

**build.gradle에 추가**
`compile 'com.h2database:h2'`

**application.properties에 추가**(선택)
`spring.jpa.show-sql=true` 
