## setting
<img src="https://user-images.githubusercontent.com/36287324/82849694-f6252780-9f33-11ea-90d2-d7077f6bd408.png" width="30%"/>

Name, Artifact, Description, Package 는 각자에 맞춰서 변경

<img src="https://user-images.githubusercontent.com/36287324/82770058-1db3bb80-9e72-11ea-95dc-169fd61672b5.PNG" width="30%"/>


## h2 의존성 등록
현재 database 연결해놓은 것이 없으니 database 만들기 전까지 메모리 db인 h2 등록

**build.gradle에 추가**
`compile 'com.h2database:h2'`

**application.properties에 추가**(선택)
`spring.jpa.show-sql=true` 
