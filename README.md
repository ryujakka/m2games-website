# Project M2 Studio 공식 홈페이지

GitHub Pages에서 동작하는 정적 웹사이트입니다. HTML/CSS/JS만 사용하며 별도 서버가 필요하지 않습니다.

## 구성
- `index.html` 스튜디오 메인
- `kkongji.html` 게임 소개, Steam 링크, 스크린샷 확대, YouTube 트레일러
- `news.html` 개발 소식
- `site-config.js` 콘텐츠 설정
- `admin.html` 로컬 전용 콘텐츠 편집기 (공개 업로드 금지)
- `assets/` 로고·배경·스크린샷 교체 폴더

## 콘텐츠 변경 (관리 화면)
1. ZIP을 압축 해제합니다.
2. 컴퓨터에서 `admin.html`을 엽니다.
3. 원하는 텍스트, 링크, 이미지 경로, 공지사항을 편집합니다.
4. `설정 파일 다운로드`를 클릭합니다.
5. 다운로드된 `site-config.js`를 홈페이지 폴더의 같은 이름 파일과 교체합니다.
6. 이미지도 `assets/`에 복사합니다. 이미지 확장자는 JPG, PNG, WEBP, SVG 모두 가능합니다.
7. 사이트 파일을 GitHub에 업로드/커밋하면 변경 내용이 배포됩니다.

관리 화면은 **실시간 서버 관리 시스템이 아닙니다**. 로그인/인증/서버 저장 기능이 없으며, GitHub에 직접 쓰지 않습니다. 공개 저장소에는 `admin.html`을 올리지 마세요.

## GitHub Pages 배포
1. GitHub에 새 **Public** 저장소를 만듭니다.
2. `admin.html`을 제외한 홈페이지 폴더의 **내용물**을 저장소 최상위(root)에 업로드합니다.
3. Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)` → Save.
4. Pages가 제공하는 URL에서 접속을 확인합니다.
5. Settings → Pages → Custom domain에 `www.m2games.kr`를 입력합니다.
6. 도메인 등록업체 DNS에 `www` CNAME → `<GitHub사용자명>.github.io`를 설정합니다. 루트 `m2games.kr`도 연결하려면 GitHub 공식 문서의 apex A/AAAA 레코드를 설정합니다.
7. DNS 반영 후 Enforce HTTPS를 활성화합니다. 이미 다른 서비스에 쓰는 DNS 레코드가 있다면 충돌 여부를 먼저 확인하세요.

공식 문서: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

## 주의
- `steamUrl`에는 실제 Steam 상점 URL을 입력하세요. 미입력 상태에서는 버튼이 비활성화됩니다.
- `trailerUrl`에는 YouTube 영상 URL을 입력하세요. 미입력 상태에서는 안내 문구가 나옵니다.
- 사이트는 한국어/영어 메뉴 전환을 제공하지만 **콘텐츠 문구는 현재 공통**입니다. 별도 번역 콘텐츠 편집 기능은 추가 구현이 필요합니다.
- 스튜디오 로고/스크린샷은 예시 SVG이며 실제 자료가 아닙니다.
- 민감한 API 키, 비밀번호, 비공개 문서를 `site-config.js`에 넣지 마세요. GitHub Pages 파일은 공개됩니다.
