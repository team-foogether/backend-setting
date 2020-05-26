## setting
<img src="https://user-images.githubusercontent.com/36287324/82854211-bade2500-9f42-11ea-9277-a96557ec79a3.png" width="35%"/>

Name, Artifact, Description, Package 는 각자에 맞춰서 변경

<img src="https://user-images.githubusercontent.com/36287324/82854661-19f06980-9f44-11ea-8614-f836f1c6ba46.PNG" width="35%"/>
(수정) Spring Web 추가

## h2 의존성 등록
현재 database 연결해놓은 것이 없으니 database 만들기 전까지 메모리 db인 h2 등록

**build.gradle에 추가**
`compile 'com.h2database:h2'`

**application.properties에 추가**(선택)
`spring.jpa.show-sql=true` 
