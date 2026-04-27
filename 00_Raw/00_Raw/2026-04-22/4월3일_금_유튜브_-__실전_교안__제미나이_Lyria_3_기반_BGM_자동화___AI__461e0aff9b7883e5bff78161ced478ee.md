# 4월3일 금(유튜브)- [실전 교안] 제미나이 Lyria 3 기반 BGM 자동화 & AI 1인 기업 파이프라인

> **"지속적으로 나가는 음원 저작권료, 이제 AI가 100% 무료 커스텀 BGM으로 만들어 드립니다."** 본 교재를 바탕으로 나만의 음악 채널 구축은 물론, 상업용 BGM 비즈니스를 바로 시작할 수 있습니다.
> 

---

## **🎹 1. 음악 생성 프롬프트: 5가지 핵심 기둥**

일반 텍스트 챗봇과 달리, 고품질 BGM을 뽑아내려면 아래 **5가지 프롬프트 변수**를 디테일하게 제어해야 합니다.

1. **장르 (Genre):** 로파이 힙합(Lo-Fi Hip Hop), 재즈 퓨전, 시네마틱 오케스트라, 신스웨이브 등 명확한 베이스 장르
2. **주요 악기 (Instruments):** 펜더 로즈 피아노(Fender Rhodes), TR-808 드럼, 카우벨, 콘트라베이스 등 (구체적일수록 원하는 사운드 도출)
3. **템포 (BPM):** 120 BPM(경쾌함), 70 BPM(느린 템포) 등 곡의 속도 지정
4. **분위기 (Mood):** 향수 어린, 공격적인, 새벽 감성의, 몽환적인, 집중하기 좋은 등
5. **질감/특징 (Texture):** 먼지 쌓인 바이닐(LP) 노이즈, 로파이 카세트테이프 공간감, 따뜻한 진공관 앰프 톤 등

---

## **🤖 2. 구글 제미나이 Lyria 3 모델의 2가지 무기**

구글 AI 스튜디오 및 API에서 제공하는 **Lyria 3**는 목적에 따라 두 가지 모델로 나뉩니다.

### **🎧 1) Lyria 3 Pro (`lyria-3-pro-preview`)**

- **특징:** 스튜디오 수준의 최고 품질 프리미엄 모델
- **길이:** 최대 3분 (전체 길이의 완곡 생성)
- **주 작업:** 곡의 구조(Intro, Verse, Bridge, Chorus 등)가 풀 세팅된 상업용 음원, 유튜브 공식 음원 플레이리스트 제작에 최적화

### **⏱️ 2) Lyria 3 Clip (`lyria-3-clip-preview`)**

- **특징:** 속도에 최적화된 고속 생성 모델
- **길이:** 30초
- **주 작업:** 숏폼(Reels, Shorts) 배경 음악, 타격감 있는 루프, 빠른 아이디어 프로토타이핑 검증용

---

## **📝 3. 무조건 터지는 음악 프롬프트 공식**

텍스트 프롬프트 창에 아래 공식을 뼈대로 살을 붙여보세요. **`[장르/시대] + [템포/무드] + [특정 악기] + [보컬 스타일] + [가사/주제]`**

> **💡 동네 카페 BGM 프롬프트 예시 (보컬 제외)** "1990년대 스타일의 로파이 힙합, 75 BPM의 새벽 감성 몽환적인 무드, 빈티지한 펜더 로즈 피아노와 무거운 어쿠스틱 드럼 루프, 먼지 쌓인 LP 노이즈 질감 추가, 보컬 없이 연주곡으로만."
> 

---

## **💻 4. 에이전트도구**

이제 웹 UI에서 타이핑하는 것을 넘어, 파이썬을 이용해 내 컴퓨터가 24시간 곡을 찍어내도록 **API 에이전트**를 구축합니다.

### 

### **🚀 실전 코드: 오디오 생성**

```
python

import os
from googleimport genai
from google.genaiimport types

# 1. 제미나이 API 클라이언트 연결 (환경 변수 GEMINI_API_KEY 설정 필요)
client = genai.Client()

# 2. Lyria 모델 호출 및 프롬프트 전송
response = client.models.generate_content(
    model="lyria-3-clip-preview",
    contents="Create a 30-second cheerful acoustic folk song with guitar and harmonica.",
    config=types.GenerateContentConfig(
        response_modalities=["AUDIO","TEXT"],# 오디오와 가사(텍스트) 동시 반환 요청
    ),
)

# 3. 반환받은 응답에서 오디오와 텍스트(가사) 분리 저장 준비
lyrics = []
audio_data =None

# 모든 파트를 반복하며 데이터 분리
for partin response.parts:
if part.textisnotNone:
        lyrics.append(part.text)
        print("📝 생성된 텍스트/가사:", part.text)
elif part.inline_dataisnotNone:
        audio_data = part.inline_data.data

# 4. mp3 파일로 하드디스크에 저장 (자동화의 완성)
if audio_data:
with open("clip.mp3","wb")as f:
        f.write(audio_data)
    print("✅ 성공! 'clip.mp3' 파일이 저장되었습니다.")
else:
    print("❌ 오디오 데이터를 받지 못했습니다.")
```

> 
>