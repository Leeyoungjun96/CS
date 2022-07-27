##URI(Uniform Resource Identifier)

###"URI는 로케이터(locator), 이름(name) 또는 둘다 추가로 분류될 수 있다"
Uniform : 리소스 식별하는 통일된 방식
Resource : 자원, URI로 식별할 수 잇는 모든 것(제한 없음)
Identifier : 다른 항목과 구분하는데 필요한 정보

###URI안에 URL(Resource Locator), URN(Resource Name)이 포함
URL - Locator : 리소스가 있는 위치를 지정
URN - Name : 리소스에 이름을 부여
위치는 변할 수 있지만, 이름은 변하지 않는다.

###URL 문법 
• scheme://[userinfo@]host[:port][/path][?query][#fragment]
• https://www.google.com:443/search?q=hello&hl=ko

프로토콜(https) : 어떤 방식을 자원에 접근할 것인가 하는 약속 규칙
http는 80포트, https는 443 포트를 주로 사용, 포트는 생략 가능

호스트명(www.google.com) : 도메인명 또는 IP 주소를 직접 사용 가능

포트번호(443) : 일반적으로 생략, 생략시 http는 80, https는 443

패스(/search) : 리소스 경로, 계층적 구조

쿼리 파라미터(q=hello&hl=ko) : key=value 형태, ?로시작하며 &로 추가 가능, query parameter/query string 등으로 불림, 웹서버에 제공하는 파라미터/문자 형태
