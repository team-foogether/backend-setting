1. gradle에 h2 추가
```
dependencies {
        :
    runtimeOnly 'com.h2database:h2'
        :
}
```

2. h2 설치
> 주의! Version 1.4.199를 사용해주세요.
> 1.4.199 버전 다운로드 링크
윈도우 설치 버전: https://h2database.com/h2-setup-2019-03-13.exe
윈도우, 맥, 리눅스 실행 버전: https://h2database.com/h2-2019-03-13.zip


**h2 설치한 곳/bin** 가서 h2.bat 더블 클릭

![이미지 008](https://user-images.githubusercontent.com/36287324/82755614-b2d19880-9e0f-11ea-8c2f-f323e2a6190f.png)

그럼 페이지가 나타남.
![이미지 009](https://user-images.githubusercontent.com/36287324/82755646-e9a7ae80-9e0f-11ea-99ff-86e113c8e67f.png)

여기서 원래 주소는
`http://10.0.75.1:8082/login.jsp?jsessionid=7adb6bc7de78562b06927887fde633b4`

여기서 앞에 부분만 `localhost:8082`로 변경
![이미지 010](https://user-images.githubusercontent.com/36287324/82755683-2a9fc300-9e10-11ea-845b-39bf4289494f.png)


왜냐하면 처음에 **DB파일을 생성할 경로를 지정해줘야함**
원하는 경로 설정 - `C:/Users/[사용자이름]/Desktop/h2-db`
- jdbc:h2:[원하는 경로 설정]/[원하는 DB 이름]

	- 나는 h2를 다른 곳에 설치했으므로 `~`에 현재 프로젝트의 경로로 바꿔줌
 이렇게 하면 h2를 파일 모드로 실행 가능
 ![이미지 011](https://user-images.githubusercontent.com/36287324/82755733-7fdbd480-9e10-11ea-9136-2a40d74a36e3.png)
- **`[원하는 경로]에서 [원하는DB이름].mv.db` 파일 생성 확인**
![이미지 012](https://user-images.githubusercontent.com/36287324/82757315-98e98300-9e1a-11ea-9424-b1a61f49b36c.png)

파일 생성이 권한도 있어야 되고 해서 Session키를 물고 있어야함. 그래서 **처음 DB파일 생성할때만 파일모드로 접근하고 이후에는 JDBC URL에 Network mode(tcp)로 접근**
- **이후 부터는 jdbc:h2:tcp://[설정한 경로]/[DB 이름] 이렇게 접속**
