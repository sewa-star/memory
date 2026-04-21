# 2월4일 수- 
📘 차세대 AI 에이전트 자동화: OPAL, MCP, Antigravity

### 오늘의 연구

**📘 차세대 AI 에이전트 자동화: OPAL, MCP, Antigravity**

Google OPAL의 자동화, MCP의 표준화된 연결성, 그리고 Antigravity의 워크플로우 실행력을 결합한 차세대 자동화 시스템을 설계하고, 이를 통해 멀티미디어(이미지) 생성 자동화를 구현하는 방법을 다룹니다.

**중요 : 오늘 라이브는 아래의 영상을 꼭 시청하시고 참여해주시면 더욱 깊은 이해가 됩니다.** 

[https://youtu.be/Iiyy80_x6oo?si=VAdiH1vm1_4KV_v0](https://youtu.be/Iiyy80_x6oo?si=VAdiH1vm1_4KV_v0)

### 논의 : Google OPAL X MCP X Antigravity 를 연결하면 어떻게 될까?

현재 제이가 개발중..

![스크린샷 2026-02-04 오후 7.07.25.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-02-04_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.07.25.png)

### Part 1. 이론 및 아키텍처 설계

**1. The Trinity: OPAL x MCP x Antigravity 연결 가설**

- **MCP (Model Context Protocol - The Connector):**
    - **역활:** AI 모델과 외부 데이터/툴 간의 표준 인터페이스.
    - **기여:** OPAL이 Antigravity의 툴을 호출하거나, 외부 DB를 참조할 때 '통역사' 역할을 하여 복잡한 API 연동 없이 플러그인 형태로 기능을 확장하게 합니다.
- **Antigravity (The Engine):**
    - **역활:** 워크플로우 오케스트레이션 및 실제 액션 수행.
    - **기여:** OPAL의 판단을 받아 실제 `generate image`같은 과업을 수행하고 결과를 다시 MCP를 통해 모델로 반환합니다.

## 제2장. 핵심 로직: "한 번에 여러 개 만들기" (Batch & Parallel)

사용자가 "트럼프, 머스크, 잡스 3명을 그려줘"라고 한 번만 말해도, 알아서 3장의 이미지가 나오는 원리를 배웁니다.

```jsx
A cute, highly stylized 3D caricature of 트럼프, featuring a slightly oversized head, big glossy eyes, and soft rounded facial features. Rendered in a clean Pixar-inspired style with smooth textures and gentle ambient lighting. Subtle shadows and a simple pastel background keep the focus entirely on the character’s charm.
이거 비슷하게 다른 캐릭터 3개로 만들어줘
```

### 1. Fan-out & Fan-in (부채 펼치기 & 접기)

이것이 **Google OPAL 워크플로우**

1. **명령 수신:** "3명 그려줘"
2. **Fan-out (확산):** OPAL이 이 명령을 3개의 작업지시서로 쪼갭니다. (부채를 펼치듯 작업이 늘어납니다.)
    - 작업 1: 트럼프 그리기
    - 작업 2: 머스크 그리기
    - 작업 3: 잡스 그리기

### OPAL VS Antigravity or connection?

### 질문 : OPAL과 Antigravity는 같은가?

### 생각 : Antigravity 또한 마찬가지. 다만 워크플로우를 감춘다.

### 질문 : 그렇다면 Parallel Execution (병렬 실행) 인가?

제이의 생각 : 아니다, 하지만 이미지 생성 오류를 Self healing 가능할것 같다.

Antigravity의 generate image 기능을 이용한 이미지 생성 자동화 

### Antigravity에서의 연구

다운로드 받기 : https://antigravity.google/

### 실험 1 : 명령어 하나에 여러개 이미지 생성을 해보자

![스크린샷 2026-02-04 오후 7.10.03.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-02-04_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.10.03.png)

![스크린샷 2026-02-04 오후 7.10.20.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-02-04_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.10.20.png)

![스크린샷 2026-02-04 오후 7.10.44.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-02-04_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.10.44.png)

# 같이 연구해봅시다!

### 실험 2 : 구글 OPAL에서 어려웠던 누가 제일 잘생겼어? 를 빠르게 할수 있는지 테스트하자.

프롬프트 : 

```jsx
첨부한 이미지를 아래의 프롬프트를 사용해서 이미지 생성

A cute, highly stylized 3D caricature of 첨부 이미지, featuring a slightly oversized head, big glossy eyes, and soft rounded facial features. Rendered in a clean Pixar-inspired style with smooth textures and gentle ambient lighting. Subtle shadows and a simple pastel background keep the focus entirely on the character’s charm. 
```

### 실험 3 : 그리고 웹사이트까지 바로 만들수 있는지 테스트하자

![스크린샷 2026-02-04 오후 9.01.06.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-02-04_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_9.01.06.png)