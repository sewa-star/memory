# 3월23일 월(유튜브)- [Connect AI LAB] AI 수익형 앱 개발 마스터 클래스: 실전편

---

이 교재는 최신 인공지능인 Gemini 3.1, AI STUDIO 을 활용하여 복잡한 로직을 한 번에 구현하는 기술을 다룹니다. 인공지능에게는 한국어보다 영어로 구체적인 프롬프트를 줄 때 성능이 극대화되므로, 본 프롬프트는 영문으로 작성되었습니다.

---

### 프로젝트 1: Sky Conquest (3D 멀티플레이어 비행 슈팅)

1. 이론 및 학습 포인트
- Three.js 기반의 고성능 그래픽 구현 및 클라이언트 사이드 물리 연산
- Firebase Realtime Database를 이용한 초저지연 멀티플레이어 상태 동기화
- PayPal SDK를 통한 인게임 상점 및 실제 결제 데이터 처리 로직
1. 구글 AI 스튜디오 활용법
- 모델 설정에서 Gemini 3.1을 선택합니다.
- 하단의 복합 프롬프트를 그대로 복사하여 입력창에 넣으세요.
- 생성된 코드를 index.html로 저장하고 Firebase API 키를 연결합니다.
1. Gemini 3.1 전용 풀 프롬프트 (Copy & Paste)

> Create a high-performance 3D multiplayer airplane arcade game titled Sky Conquest: Connect AI LAB Edition using Three.js and Firebase.
> 
> 1. Branding and UI:
> - Display a glassmorphism header with Connect AI LAB in neon cyan.
> - Include an Open in New Tab button and a Shop button for payments.
> - Ensure UI layers do not block 3D canvas pointer events.
> 1. Core Mechanics:
> - 3rd-person chase camera with dynamic FOV during speed boosts.
> - Physics-based flight using WASD/Arrow keys and Spacebar to fire.
> - Collectible Data Cores with varying point values spawned randomly.
> 1. Multiplayer (Firebase):
> - Real-time state synchronization of player position, rotation, and score using Firebase Realtime Database.
> - Global live leaderboard showing top 10 players.
> - Drop-in/drop-out system with automatic cleanup of inactive players.
> 1. Monetization (PayPal):
> - Fully integrate PayPal JavaScript SDK.
> - Create a purchase flow for Premium Fuel or Skins.
> - On payment approval, update the credits field in the user's Firebase document and trigger a gold particle explosion.
> 1. Visuals:
> - Cyber-arcade aesthetic with neon light trails, bloom effects, and volumetric clouds.
> - Provide the complete boilerplate including Firebase/PayPal config placeholders.

---

### 프로젝트 2: Chef AI LAB (AI 지능형 레시피 관리 SaaS)

1. 이론 및 학습 포인트
- LLM을 활용한 비정형 텍스트(레시피)의 JSON 구조화 기술(Parsing)
- Firestore 기반의 계층적 데이터 모델링 및 다중 사용자 권한(RBAC) 설계
- SaaS 모델을 위한 구독 기반 결제 시스템 구축
1. 구글 AI 스튜디오 활용법
- Gemini 3.1 모델을 선택하고 시스템 인스트럭션에 아래 프롬프트를 입력합니다.
- AI가 출력하는 데이터 스키마와 프론트엔드 코드를 확인하세요.
1. Gemini 3.1 전용 풀 프롬프트 (Copy & Paste)

> Build a centralized AI-assisted recipe organizer called Chef AI LAB with intelligent parsing and household sync.
> 
> 1. Interface and Branding:
> - Sleek Dark Mode UI with Connect AI LAB branding and glassmorphism cards.
> - 3D Interactive Pantry view using Three.js where ingredients are displayed on a virtual shelf.
> 1. AI Logic (Gemini Engine):
> - Create a module that takes raw recipe text or image URLs and parses them into structured JSON (ingredients, steps, macros).
> - Implement an AI Suggest button that generates custom recipes based on existing pantry items in Firebase.
> 1. Household Management (Firebase):
> - Multi-user sync with Household ID grouping.
> - Role-Based Access Control: Admin (Billing), Editor (Add/Edit), Viewer (Read only).
> - Real-time shopping list that updates instantly across all devices in the household.
> 1. Payment Gateway (PayPal):
> - Integrate PayPal SDK for a Pro Subscription plan.
> - Unlocking features: Unlimited AI parsing and advanced nutritional analytics.
> - Update subscription_status in Firestore upon successful transaction.
> 1. Technical Stack:
> - Provide a React-based structure integrating Firebase Firestore, Auth, and the PayPal SDK.

---

###