# qaunt-privica

# Privica — 퀀트 투자, 누구나 쉽게

**privicalab.com**

## 소개

Privica는 코딩 없이 나만의 퀀트 투자 공식을 만들고 백테스팅할 수 있는 웹 서비스입니다.
PER, PBR, ROE 같은 팩터를 선택하고 가중치를 조정하면, 미국(S&P500)과 한국(KOSPI/KOSDAQ) 시장에서 과거 성과를 즉시 확인할 수 있습니다.

## 주요 기능

- **공식 빌더** — 팩터 선택 + 가중치 조정으로 나만의 투자 공식 생성
- **백테스팅** — 실제 주가 데이터 기반 과거 수익률, MDD, 샤프지수 계산
- **AI 분석** — Claude AI가 백테스팅 결과를 해설하고 개선 방향 제안
- **뉴스 감성분석** — 종목별 최근 뉴스 감성 점수 제공
- **미국 + 한국 시장** — S&P500 및 KOSPI/KOSDAQ 전 종목 지원

## 기술 스택

**프론트엔드**
- Next.js 14 (App Router)
- TypeScript
- Tailwind CSS
- Recharts

**백엔드**
- FastAPI (Python)
- yfinance
- DART OpenAPI
- Anthropic Claude API

**인프라**
- Vercel (프론트엔드)
- Railway (백엔드)
- Supabase (DB + Auth)

## 로컬 실행

**프론트엔드**
```bash
cd quant-app
npm install
npm run dev
```

**백엔드**
```bash
cd quant-backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
```

## 환경변수

**프론트엔드 (.env.local)**

NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
NEXT_PUBLIC_BACKTEST_API_URL=


**백엔드 (.env)**

SUPABASE_URL=
SUPABASE_KEY=
DART_API_KEY=
anthropic_api_key=


