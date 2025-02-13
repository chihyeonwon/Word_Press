워드프레스(WordPress)는 전 세계적으로 가장 많이 사용되는 CMS(Content Management System) 중 하나지만, 그만큼 보안 취약점도 자주 발견됩니다.

### 1. 주요 보안 취약점
① 플러그인 및 테마의 취약점     
서드파티 플러그인과 테마는 보안 점검이 부족한 경우가 많아 해킹의 주요 경로가 됩니다.
예: 플러그인 취약점을 이용한 SQL 인젝션(SQLi), 원격 코드 실행(RCE) 등.
② 관리자 페이지(로그인) 취약점     
기본적으로 /wp-admin 또는 /wp-login.php 경로에서 로그인하는데, **브루트포스 공격(무차별 대입 공격)**이 쉽게 이루어질 수 있음.
해결책: 강력한 비밀번호 사용, 로그인 제한 플러그인 적용, CAPTCHA 사용.
③ XML-RPC 취약점     
xmlrpc.php 파일을 이용한 DDoS 공격 및 패스워드 크래킹이 가능.
해결책: 필요하지 않다면 XML-RPC 비활성화.
④ 파일 업로드 취약점      
워드프레스는 미디어 파일 업로드 기능을 제공하는데, 악성 코드가 포함된 파일을 업로드하여 원격 코드 실행이 가능할 수 있음.
해결책: MIME 타입 검사 및 실행 가능한 확장자 제한.
⑤ SQL 인젝션(SQLi) 공격     
데이터베이스 쿼리 조작을 통해 관리자 계정 탈취 또는 데이터 유출이 가능.
해결책: 최신 업데이트 적용 및 입력값 검증 강화.
⑥ 크로스사이트 스크립팅(XSS)     
악성 스크립트를 삽입하여 방문자의 브라우저에서 실행되도록 유도.
해결책: 입력값 필터링 및 CSP(Content Security Policy) 설정.
### 2. 주요 공격 기법      
① 브루트포스 공격        
약한 관리자 비밀번호를 대상으로 무차별 대입 공격 수행.
대응 방법: 2단계 인증(2FA) 활성화, 로그인 시도 제한 설정.
② 악성 플러그인 및 테마 이용     
신뢰할 수 없는 출처에서 플러그인 및 테마를 다운로드하면 악성 코드 포함 가능.
대응 방법: 공식 워드프레스 마켓플레이스에서만 다운로드.
③ 백도어 삽입      
취약한 플러그인, 테마, 파일 업로드 기능을 이용해 백도어(backdoor) 파일을 삽입.
대응 방법: 정기적인 코드 검사 및 보안 플러그인 사용.
④ 피싱 및 소셜 엔지니어링 공격      
관리자를 속여 악성 링크 클릭 또는 가짜 로그인 페이지 입력을 유도.
대응 방법: 관리자 계정 보안 교육 및 URL 확인 철저.
⑤ 워드프레스 REST API 공격         
취약한 REST API 엔드포인트를 이용해 게시물 수정, 계정 정보 탈취 가능.
대응 방법: REST API 접근을 제한하는 보안 플러그인 사용.
