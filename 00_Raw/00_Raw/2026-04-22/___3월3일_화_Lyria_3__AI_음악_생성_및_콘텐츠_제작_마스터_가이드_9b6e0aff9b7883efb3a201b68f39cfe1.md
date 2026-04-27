# 📘 3월3일 화[Lyria 3] AI 음악 생성 및 콘텐츠 제작 마스터 가이드

---

## 제 1장: Lyria 3 핵심 이론 (The Theory)

![스크린샷 2026-03-03 오후 7.47.28.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-03-03_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.47.28.png)

![스크린샷 2026-03-03 오후 7.36.52.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-03-03_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.36.52.png)

Lyria 3는 단순한 텍스트-투-오디오 모델을 넘어, 음악의 구조적 이해를 바탕으로 하는 **멀티모달 음악 생성 AI**입니다.

1. **구조화된 프롬프팅 (Structured Prompting):** 단순 키워드가 아닌 템포(BPM), 다이내믹(강약), 악기 구성을 계층적으로 이해합니다.
2. **보컬 프로파일링 (Vocal Profiling):** 성별, 음역대(Soprano/Baritone), 질감(Breathy/Gravelly)을 분리하여 설정 가능합니다.
3. **이미지-투-뮤직 (Image-to-Music):** 시각적 데이터를 분석하여 분위기(Mood)와 질감(Texture)을 음악으로 치환합니다.

---

## 제 2장: 유튜브 인트로 제작 프로세스 (K-AI Lab 스타일)

채널의 첫인상을 결정하는 10~15초 인트로 제작 공식입니다.

### [실전 프롬프트 템플릿]

> **Prompt:** "A 10-second high-tech **K-Electronic** intro for an AI lab. 128 BPM. Features a **sharp digital glitch** opening, followed by a **driving synthwave melody**. Professional studio mix, high-fidelity. **Instrumental only.** Ends with a clean resolution."
> 
- **Tip:** 인트로에서 '글리치(Glitch)' 소리는 시청자의 주의를 환기하는 효과가 있습니다.
- **Antigravity 활용:** 채널 로고 이미지를 업로드하고 위 프롬프트를 함께 넣으면 로고 분위기에 맞는 사운드가 생성됩니다.

---

## 제 3장: 보컬 및 한글 가사 구현 (Vocal & Lyrics)

Lyria 3는 다국어 지원이 강력하여 한글 가사 생성이 가능합니다.

### 1. 한글 가사 입력 방법

가사를 넣을 때는 **[Lyrics]** 태그를 사용하거나 문장으로 명시하는 것이 좋습니다.

> **Prompt:** "A soulful K-pop ballad with a **clear soprano female vocal**. The lyrics are in **Korean**.
> 
> 
> **[Lyrics]** > 새로운 연결, 인공지능의 미래, 우리와 함께 시작해요.
> 
> Create a warm and emotional atmosphere with acoustic piano."
> 

### 2. 보컬 스타일 세부 제어

- **K-Pop 아이돌 느낌:** "Polished K-pop idol vocal style, upbeat and energetic."
- **감성적인 느낌:** "Breathy, emotional Korean indie-style vocals."
- **신뢰감 있는 나레이션풍:** "Calm and steady male baritone, rhythmic talking style."

---

## 제 4장: 실전 실험용 프롬프트 라이브러리 (Copy & Paste)

![스크린샷 2026-03-03 오후 7.37.16.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-03-03_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.37.16.png)

![스크린샷 2026-03-03 오후 7.37.29.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-03-03_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.37.29.png)

| **목적** | **영문 실전 프롬프트 (Lyria 입력용)** | **기대 효과** |
| --- | --- | --- |
| **미래적 배경음** | "Futuristic ambient techno, minimalist pulse, 110 BPM. No vocals. Perfect for AI tutorial background." | 설명 영상에 최적화된 깔끔한 BGM |
| **K-퓨전 테크** | "Fusion of traditional Gayageum and modern Trap beats. High-energy, heavy bass. High-tech Korea vibe." | 한국적이고 독창적인 AI 채널 정체성 |
| **감성 브이로그** | "Chill Korean City-pop, 95 BPM. Funky electric guitar, nostalgic synth pads. Instrumental only." | 편안하고 세련된 일상 영상 배경 |
| **전환 효과음** | "5-second rapid percussion build-up ending with a digital chime. High dynamics." | 장면 전환 시 임팩트 부여 |

---

## 제 5장: 전문가용 조절 키워드 (The Toolkit)

![스크린샷 2026-03-03 오후 7.37.46.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-03-03_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.37.46.png)

프롬프트 끝에 붙여 퀄리티를 높이는 단어들입니다.

- **`Royalty-free style`**: 유튜브 저작권 시스템에 최적화된 전형적인 구성 요청.
- **`Seamless loop`**: 배경음악으로 무한 반복 사용 가능한 구조.
- **`SynthID integrated`**: 구글의 AI 워터마크 기술을 고려한 정밀 생성.
- **`Mastered for YouTube`**: 유튜브 오디오 표준에 맞춘 마스터링 품질.

---

![스크린샷 2026-03-03 오후 7.38.09.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-03-03_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.38.09.png)

![스크린샷 2026-03-03 오후 7.38.28.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-03-03_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.38.28.png)

![스크린샷 2026-03-03 오후 7.40.41.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-03-03_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.40.41.png)

![스크린샷 2026-03-03 오후 7.40.53.png](%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2026-03-03_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.40.53.png)

[Neon_Bloom.mp4](Neon_Bloom.mp4)

[https://youtube.com/shorts/-PiPYFIDSdY?si=LBFQonoF5mxyc4lm](https://youtube.com/shorts/-PiPYFIDSdY?si=LBFQonoF5mxyc4lm)

오늘 제출할것, 자신만의 음악을 만들어서 위와같이 어떤 프롬프트를 썼는지( 이미지, 영상, 텍스트를 넣다며 함께 캡쳐)해서 결과물을 jay@connexionai.kr로 보내주세요