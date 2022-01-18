### URI (uniform Resource Identifier)

URI? URL? URN?

URI는 로케이터(locator), 이름(name) 또는 둘 다 추가로 분류될 수 있다.

* URI의 뜻
    * Uniform
    * Resource
    * Identifier

* URL 전체 문법
    * scheme://[userinfo@]host[:port][/path][?query][#fragment]
    * https://www.google.com:443/search?q=hello&hl=ko

    * 프로토콜(https)
    * 호스트명(www.google.com)
    * 포트 번호(443)
    * 패스(/search)
    * 쿼리 파라미터(q=hello&hl=ko)

### 웹 브라우저 요청 흐름

* 웹 브라우저와 구글 서버가 있다고 가정

1. 웹 브라우저가 HTTP 요청 메시지 생성
2. SOCKET 라이브러리를 통해 전달
    * A. TCP/IP 연결 (IP, PORT)
    * B. 데이터 전달
3. TCP/IP 패킷 생성, HTTP 메시지 포함

패킷에는 출발지(IP, PORT), 목적지(IP, PORT), 전송 데이터(HTTP 메시지) 등이 존재

웹 브라우저에서 구글 서버로 요청 패킷을 전달한다. 
이후 구글 서버에서 패킷을 까 HTTP 요청 메시지를 확인한 후 HTTP 응답 메시지와 함께 응답 패킷을 웹 브라우저로 전송한다.


