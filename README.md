# UniMate

대학 학칙을 질문하는 AI 챗봇과 학생 커뮤니티, 개인 시간표를 한곳에서 제공하는 모바일 웹 서비스입니다. 2025년 2학기 생성형 AI 활용 팀 프로젝트로 제작했습니다.

[서비스](https://mo-do-ri-project.vercel.app/) · [기획서](PRD.md) · [발표 자료](PPT.md)

## 주요 기능

- 학교별 학칙 자료를 바탕으로 답변하는 챗봇과 대화 기록 관리
- 게시글·댓글·좋아요, 학교·카테고리별 탐색 및 사진 첨부
- 개인 시간표 관리와 댓글·좋아요 알림
- 회원 프로필, 모바일 레이아웃과 라이트·다크 테마

## 내가 맡은 작업 — 박수진

팀 공동 프로젝트이며, 아래 항목은 `parksuejin1026` 계정의 커밋으로 확인되는 작업입니다.

| 영역 | 직접 구현·개선한 내용 | 대표 커밋 |
| --- | --- | --- |
| 커뮤니티 | 게시글 CRUD, 댓글·좋아요, 학교별 필터링, 익명 작성과 사진 첨부 | [게시판 구현](https://github.com/parksuejin1026/UniMate/commit/99bac089ba), [사진 첨부](https://github.com/parksuejin1026/UniMate/commit/a2691f5138) |
| 시간표 | 주간 그리드, 수업 추가·삭제, 상세·확인 모달 및 저장·조회 API | [시간표 구현](https://github.com/parksuejin1026/UniMate/commit/129b134c4a) |
| 알림 | 알림 목록 UI, 읽음·모두 읽음 처리 및 API 연동 | [알림 센터](https://github.com/parksuejin1026/UniMate/commit/90ff91f6c6) |
| 채팅·데이터 | 채팅 API와 MongoDB 스키마 작업, 채팅 인터페이스 및 모바일 레이아웃 개선 | [API·스키마](https://github.com/parksuejin1026/UniMate/commit/bc29e3d51e), [채팅 UI](https://github.com/parksuejin1026/UniMate/commit/08243be812) |
| UI/UX | UniMate 리브랜딩, 테마·모바일 화면, 입력창·스켈레톤·빈 화면과 스플래시 개선 | [리브랜딩](https://github.com/parksuejin1026/UniMate/commit/0f469afdea), [UI 개선](https://github.com/parksuejin1026/UniMate/commit/cf63f2617a), [스플래시](https://github.com/parksuejin1026/UniMate/commit/73ab725588) |
| 문서화 | PRD 정리, 아키텍처·API 명세·사용자 가이드·배포 문서 작성 | [산출물 문서화](https://github.com/parksuejin1026/UniMate/commit/50159be244) |

## 기술 구성

| 구분 | 기술 |
| --- | --- |
| 웹 | Next.js 14, React, TypeScript |
| UI | Tailwind CSS, sonner |
| 데이터 | MongoDB / Mongoose, Google Sheets API |
| 챗봇 | OpenAI API, Vercel AI SDK |
| 인증 관련 | bcryptjs, nodemailer |
| 배포 | Vercel |

## 실행

Node.js 18.17 이상과 npm이 필요합니다.

```sh
git clone https://github.com/parksuejin1026/UniMate.git
cd UniMate
npm ci
```

[배포·환경 설정 문서](docs/DEPLOYMENT.md)에 따라 `.env.local`을 설정한 뒤 실행합니다. MongoDB, 학교별 Google Sheets 데이터와 챗봇 API 설정이 필요합니다.

```sh
npm run dev
```

개발 서버: `http://localhost:3000`

## 구조와 문서

| 경로 | 내용 |
| --- | --- |
| [app](app) | 서비스 페이지와 API |
| [components](components) | 채팅·탭 바·모달 등 UI 컴포넌트 |
| [context](context) | 테마 등 공통 상태 |
| [lib](lib) | DB, Google Sheets 및 외부 서비스 연동 |
| [public](public) | 이미지·아이콘 |
| [아키텍처](docs/ARCHITECTURE.md) | 시스템 구성과 데이터 흐름 |
| [API 명세](docs/API_REFERENCE.md) | 주요 API |
| [사용자 가이드](docs/USER_GUIDE.md) | 서비스 이용 방법 |
| [배포 가이드](docs/DEPLOYMENT.md) | 설치·환경 설정과 배포 |
