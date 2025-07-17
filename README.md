# 점심 메뉴 추천 API 🍽️

점심 메뉴를 추천해주는 RESTful API 서버입니다.

## 설치 및 실행

### 1의존성 설치
```bash
npm install
```

### 2서버 실행
```bash
# 개발 모드 (nodemon 사용)
npm run dev

# 프로덕션 모드
npm start
```

서버는 기본적으로 `http://localhost:3000`에서 실행됩니다.

## API 엔드포인트

### 1서버 정보
- **GET** `/`
- 서버 상태와 사용 가능한 엔드포인트 정보를 반환합니다.

### 2. 점심 메뉴 추천
- **GET** `/api/lunch/recommend`
- 오늘의 점심 메뉴를 추천합니다.

**응답 예시:**
```json
{
  success:true,data: [object Object]
  name": "김치찌개,
    category": "한식",
    description":매콤달콤한 김치찌개",
    price": "800원,
    rating:40.5   image: "https://example.com/kimchi-jjigae.jpg"
  },
  message":오늘의 점심 메뉴를 추천합니다!}
```

### 3. 전체 메뉴 목록
- **GET** `/api/lunch/menu`
- 전체 메뉴 목록을 반환합니다.

**응답 예시:**
```json
{
  success:true,
data:
   [object Object]  id": 1,
    name: ,
      category": 한식",
      price": "8000,
     rating: 4.5   }
  ],
  count":1
}
```

## 기술 스택

- **Node.js** - 런타임 환경
- **Express.js** - 웹 프레임워크
- **CORS** - Cross-Origin Resource Sharing
- **Helmet** - 보안 헤더
- **Morgan** - HTTP 요청 로깅

## 개발 가이드

### 내부 구현이 필요한 부분
1. **`/api/lunch/recommend`** - 실제 추천 알고리즘 구현
2**`/api/lunch/menu`** - 메뉴 데이터베이스 연동

각 엔드포인트의 TODO 주석 부분에 실제 비즈니스 로직을 구현하시면 됩니다.

## 환경 변수

- `PORT` - 서버 포트 (기본값: 3000) 