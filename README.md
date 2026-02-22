# Apple Price Prediction & Communication Platform
> **기상 데이터 기반 사과 가격 예측 AI 및 PHP 기반 커뮤니티 관리 시스템**

본 프로젝트는 데이터 분석 기반의 가격 예측 서비스와 사용자 간 소통을 위한 커뮤니티 플랫폼이라는 두 가지 핵심 모듈로 구성

---

## 1. 사과 가격 예측 서비스 (Apple Price Predictor)
기상청 기상 데이터와 Kamis(농수산유통정보) 오픈 API를 활용하여 사과 가격의 변동 추이를 분석하고 예측

### Tech Stacks
- **Language:** `Python 3.x` (Jupyter Notebook)
- **Library:** `Pandas`, `Scikit-learn`, `Flask`
- **Model:** 경사 하강법(Gradient Descent), MSE(Mean Squared Error)
- **Tools:** VS Code, Anaconda

### Key Features & Improvements
- **데이터 전처리:** `StandardScaler`를 활용한 기상 데이터(기온, 강수량) 정규화
- **성능 최적화:** - 손실 함수(Loss) 값을 초기 **57만**에서 **17~18만**으로 약 68% 감소 성공
  - 최적화 알고리즘을 SGD에서 **Adam**으로 변경하여 수렴 속도 및 정확도 향상
- **웹 서비스화:** Flask 프레임워크를 이용해 학습된 모델을 웹 템플릿과 연동하여 실시간 예측 UI 제공


---

## 2. 커뮤니케이션 및 관리 시스템
XAMPP 환경에서 PHP와 MySQL을 활용하여 구축한 회원 관리 및 게시판 통합 솔루션

### 스택
- **Backend:** `PHP`
- **Database:** `MySQL`(SQLyog)
- **Server:** `XAMPP`(Apache)
- **Frontend:** HTML5, CSS3, JavaScript

### Core Functions
- **회원 관리:** - 비밀번호 **단방향 암호화** 저장 및 아이디/메일 중복 체크
  - 우편번호 API 연동 및 프로필 이미지 미리보기
- **어드민 패널:** - 회원 권한 관리, 목록 **페이지네이션**, 데이터 **Excel 저장** 기능
  - 동적 게시판 생성 및 삭제 관리 로직
- **커뮤니티 게시판:** - 파일 첨부(용량 제한 핸들링), 댓글 시스템, 게시물 검색 및 조회수 중복 방지

---

## Installation & Execution

### AI 예측 서버 실행
```bash
cd ./apple-predict-web
python app.py
```

![APP](https://github.com/user-attachments/assets/f12b9cf1-7d1b-48f7-a2ce-2d2311a947d1)
![Board](https://github.com/user-attachments/assets/b4b7e7fb-5ad5-4959-be27-ae428b0030c5)


