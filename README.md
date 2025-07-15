# [OWASP 취약점 실습] [유다인]


1. docker 설치 (cmd에서 설치)
   
2. docker pull bkimminich/juice-shop
   
   docker run -d -p 3000:3000 bkimminich/juice-shop 각각 cmd에 입력 후 owasp juice shop 설치 완료


3. owasp juice shop으로 이동, 로그인에 ' OR 1 = 1 -- 입력 후 비밀번호 아무거나 친 후 성공



4. f12 누르고 admin 검색
   이떄 path 옆에 있는 것 위주로 확인
   
   http://localhost:3000/#/administration로 이동하면 admin 계정으로 로그인 된 것 확인 가능

5. 숨겨진 점수판 페이지 찾기-

   
   4번 과정과 동일하게 점수를 영어로 변경한 score을 검색하면 똑같이 path 근처에 있는 계정 이름 확인 가능
   
   http://localhost:3000/#/score-board로 이동하면 해킹 챌린지 문제를 풀 수 있음





문제 1번. <iframe src="javascript:alert(`xss`)">를 사용하여 DOM XSS 공격 수행


문제를 풀려고 시도하면
For this challenge, we'll take a close look at the Search field at the top of the screen. 라고 안내 문구가 뜬다.

"이번 과제에서는 화면 상단에 있는 검색 필드를 자세히 살펴볼 것입니다." 라는 뜻

문구에 따라 문제에 나와있는 <iframe src="javascript:alert(`xss`)"> 문구를 검색 필드에 그대로 치면 'xss'라고 문구가 뜬다. 



<img width="727" height="251" alt="스크린샷 2025-07-15 184637" src="https://github.com/user-attachments/assets/5d7dbc19-4e33-4388-9086-a79e61cd1404" />




<img width="811" height="216" alt="스크린샷 2025-07-15 184619" src="https://github.com/user-attachments/assets/558f91d2-cacc-42ab-a255-40bc69fe5224" />

















