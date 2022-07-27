#### HTTP API - 컬렉션
    • 회원 관리 시스템 (API 설계 - POST 기반 등록)
        • POST - 신규 자원 등록 특징
            • 클라이언트는 등록될 리소스의 URI를 모른다.
                • 회원등록 /members -> POST
                • POST /members
            • 서버가 새로 등록된 리소스 URI를 생성해준다.
                • HTTP/1.1 201 Created
                  Location: /members/100
            • 컬렉션(Collection)
                • 서버가 관리하는 리소스 디렉토리
                • 서버가 리소스의 URI를 생성하고 관리
                • 여기서 컬렉션은 /members

#### HTTP API - 스토어
    • 파일 관리 시스템 (API 설계 - PUT 기반 등록)
        • PUT - 신규 자원 등록 특징
            • 클라이언트가 리소스 URI를 알고 있어야 한다.
                • 파일 등록 /files/{filename} -> PUT
                • PUT /files/star.jpg
            • 클라이언트가 직접 리소스의 URI를 지정한다.
            • 스토어(store)
                • 클라이언트가 관리하는 리소스 저장소
                • 클라이언트가 리소스의 URI를 알고 관리
                • 여기서 스토어는 /files

• POST와 PUT의 차이점은 관리를 누가 하냐에 따라 달라진다

#### HTML FORM 사용
    • HTML FORM은 GET,POST만 지원
    • 컨트롤 URI
        • GET, POST만 지원하므로 제약이 있음
        • 이런 제약을 해결하기 위해 동사로 된 리소스 경로 사용
        • POST의 /new, /edit, /delete가 컨트롤 URI
        • HTTP 메서드로 해결하기 애매한 경우 사용(HTTP API 포함)

목록(GET), 등록(POST), 조회(GET), 수정(PATCH, PUT, POST), 삭제(DELETE)

• 문서(document)
    • 단일 개념(파일 하나, 객체 인스턴스, 데이터베이스 row)
    • EX) /members/100, /files/star.jpg
• 컬렉션(collection)
    • 서버가 관리하는 리소스 디렉터리
    • 서버가 리소스의 URI를 생성하고 관리
    • EX) /members
• 스토어(store)
    • 클라이언트가 관리하는 자원 저장소
    • 클라이언트가 리소스의 URI를 알고 관리
    • EX) /files
• 컨트롤러(controller), 컨트롤 URI
    • 문서, 컬렉션, 스토어로 해결하기 어려운 추가 프로세스 실행
    • 동사를 직접 사용
    • EX) /members/{id}/delete