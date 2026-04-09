# Secure Gallery

개인용 사진/영상을 암호화하여 Google Drive에 저장하고 감상하는 웹앱입니다.

## 주요 기능

- Google Drive 연동 (폴더 탐색, 그룹핑)
- 썸네일 그리드 갤러리 (무한 스크롤, 지연 로딩)
- 라이트박스 뷰어 (1/2/3장 보기, 슬라이드쇼, Ken Burns 효과 등)
- 즐겨찾기, 정렬 (이름/크기/날짜/셔플), Portrait/Lanscape 필터
- 오늘의 추천 폴더, 랜덤 이미지 제공
- 다중 선택 + 배치 액션 (삭제 및 즐겨찾기 등)
- 숨기기(휴지통) + 복원

## 기술 스택

- **프론트엔드:** 단일 HTML 파일
- **인증:** Google OAuth 2.0 (Google Identity Services)
- **암호화:** AES-256-GCM, PBKDF2 (클라이언트 사이드, Web Crypto API)
- **저장소:** Google Drive (암호화 파일)
- **호스팅:** GitHub Pages

## 보안

모든 파일은 업로드 시 로컬에서 AES-256-GCM으로 암호화된 후 Google Drive에 저장됩니다. 복호화는 브라우저에서만 수행되며, 비밀번호와 Google 계정 인증 없이는 접근할 수 없습니다.
