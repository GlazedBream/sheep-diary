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

### 프론트엔드
- Flutter (모바일 앱)

### 백엔드
- Django (RESTful API)
- MySQL 데이터베이스
- 사용자 인증 및 권한 관리 (JWT)

### API 문서
API 문서는 [SwaggerHub](https://virtserver.swaggerhub.com/lgu3_sheepdiary/diary-service/1.0.0)에서 확인할 수 있습니다.

## 프로젝트 구조
```
sheep-diary/
├── README.md                      # 프로젝트 소개, 설치 방법, 기여 가이드
├── .gitignore                     # Git 무시 파일 목록
├── frontend/                      # Flutter 프로젝트
│   ├── pubspec.yaml               # Flutter 패키지 의존성
│   ├── android/                   # 안드로이드 설정
│   ├── ios/                       # iOS 설정
│   ├── web/                       # (선택) 웹 지원 시 필요
│   ├── lib/
│   │   ├── main.dart              # 앱 진입점
│   │   ├── models/                # 데이터 모델
│   │   ├── screens/               # UI 화면
│   │   ├── widgets/               # 재사용 가능한 위젯
│   │   ├── services/              # API 통신 서비스
│   │   └── utils/                 # 유틸리티 함수
│   └── test/                      # 테스트 코드
├── backend/                       # Django API 서버
│   ├── manage.py                  # Django 관리 스크립트
│   ├── requirements.txt           # Python 의존성
│   ├── sheep_diary_api/           # Django 프로젝트 설정
│   │   ├── settings.py            # 설정 파일
│   │   ├── urls.py                # URL 라우팅
│   │   └── wsgi.py                # WSGI 설정
│   ├── diary/                     # 주요 앱 모듈
│   │   ├── models.py              # 데이터 모델
│   │   ├── views.py               # API 뷰
│   │   ├── serializers.py         # DRF 시리얼라이저
│   │   ├── urls.py                # API 엔드포인트
│   │   └── tests.py               # 앱 테스트
│   └── utils/                     # 유틸리티 모듈
├── db/
│   ├── schema/
│   │   ├── init_schema.sql        # 테이블 생성 SQL
│   │   └── migrations/            # 스키마 변경 스크립트
│   ├── seed/
│   │   ├── insert_dummy_data.sql  # 더미 데이터
│   │   └── test_data.sql          # 테스트용 데이터
│   └── ERD.png                    # 데이터 모델링 다이어그램
├── docs/                          # 문서
│   ├── api_spec.md                # API 명세
│   ├── ui_mockup/                 # UI 목업 이미지
│   ├── user_scenarios.md          # 사용자 시나리오
│   └── dev_guide.md               # 개발자 가이드
├── deploy/                        # 배포 설정
│   ├── docker-compose.yml         # 도커 컴포즈 설정
│   ├── backend.dockerfile         # 백엔드 도커 설정
│   ├── frontend.dockerfile        # 프론트엔드 도커 설정
│   └── nginx/                     # Nginx 설정 (필요시)
└── .github/                       # GitHub 설정
    ├── workflows/                 # GitHub Actions CI/CD
    │   ├── backend_ci.yml
    │   └── frontend_ci.yml
    └── ISSUE_TEMPLATE/            # 이슈 템플릿
```

## 개발 환경 설정

### 요구사항
- Flutter SDK
- Python 3.8 이상
- MySQL 또는 MariaDB

### 설치 및 실행
```bash
# 레포지토리 클론
git clone https://github.com/GlazedBream/sheep-diary.git
cd sheep-diary

# 백엔드 설정
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

# 프론트엔드 설정
cd ../frontend
flutter pub get
flutter run
```

## 기여 방법

1. 이 레포지토리를 포크합니다.
2. 새로운 브랜치를 생성합니다. (`git checkout -b feature/amazing-feature`)
3. 변경사항을 커밋합니다. (`git commit -m 'Add some amazing feature'`)
4. 브랜치에 푸시합니다. (`git push origin feature/amazing-feature`)
5. Pull Request를 생성합니다.

## 라이센스

이 프로젝트는 MIT 라이센스 하에 배포됩니다.
