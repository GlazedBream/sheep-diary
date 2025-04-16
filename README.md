# 쉽다이어리 (Sheep Diary)

간편하게 일상을 기록하는 다이어리 앱 서비스

## 프로젝트 소개

쉽다이어리는 사용자가 쉽고 간편하게 일기를 작성하고 관리할 수 있는 웹/앱 서비스입니다. 직관적인 인터페이스와 깔끔한 디자인으로 일상 기록을 더욱 즐겁게 만들어 드립니다.

## 주요 기능

- 사용자 계정 관리 (회원가입, 로그인)
- 일기 작성, 조회, 수정, 삭제
- 날짜별 일기 검색 및 정렬
- 심플하고 직관적인 UI/UX

## 기술 스택

### 백엔드
- RESTful API (OpenAPI 3.0.3 명세)
- 사용자 인증 및 권한 관리 (JWT)

### API 문서

API 문서는 [SwaggerHub](https://virtserver.swaggerhub.com/lgu3_sheepdiary/diary-service/1.0.0)에서 확인할 수 있습니다.

## 개발 환경 설정

### 요구사항
- Node.js 또는 적절한 백엔드 환경
- 데이터베이스 (PostgreSQL, MySQL 등)

### 설치 및 실행
```bash
# 레포지토리 클론
git clone https://github.com/GlazedBream/sheep-diary.git
cd sheep-diary

# 의존성 설치
npm install

# 개발 서버 실행
npm run dev
```

## 기여 방법

1. 이 레포지토리를 포크합니다.
2. 새로운 브랜치를 생성합니다. (`git checkout -b feature/amazing-feature`)
3. 변경사항을 커밋합니다. (`git commit -m 'Add some amazing feature'`)
4. 브랜치에 푸시합니다. (`git push origin feature/amazing-feature`)
5. Pull Request를 생성합니다.

## 라이센스

이 프로젝트는 MIT 라이센스 하에 배포됩니다.
