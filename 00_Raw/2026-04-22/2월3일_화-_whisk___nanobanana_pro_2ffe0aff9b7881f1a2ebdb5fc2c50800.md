# 2월3일 화- whisk + nanobanana pro

### 이미지 한 장으로 시작하는 하이엔드 테크 영상 제작

이 교재는 정적인 제품 사진을 생성하고, 이를 정교한 분해(Exploded) 영상으로 전환하는 **Whisk(영상 변환) + Nanobanan(고품질 프롬프트)** 워크플로우를 다룹니다.

## 1교시: 완벽한 제품 사진 생성 (The Hero Shot)

가장 먼저 영상의 시작점이 될 '완성된 제품' 이미지를 생성합니다. 애플 광고처럼 고급스러운 분위기를 연출하는 것이 핵심입니다.

### 📝 프롬프트 분석 (Nanobanan Style)

이 프롬프트는 **조명**과 **질감**에 집중하여 럭셔리한 느낌을 줍니다.

> **Prompt Input:** Deep black background with subtle gradient falloff, soft rim lighting outlining the ear cups and headband, controlled reflections on smooth metal and leather textures. Cinematic lighting, high contrast, luxury tech aesthetic, sharp focus, shallow depth of field. No clutter, no text, no logos emphasized. Shot with a professional DSLR, 85mm lens, f/1.8, ultra-high resolution, photorealistic, Apple-level product shoot, dramatic mood, modern and elegant.
> 

### ✅ 핵심 포인트

- **조명 (Rim Lighting):** 제품의 테두리를 강조하여 배경과 분리시킵니다.
- **카메라 설정 (85mm, f/1.8):** 인물/제품 사진에 가장 적합한 렌즈를 사용하여 왜곡을 줄이고 심도(Depth)를 표현합니다.
- **질감 (Metal and Leather):** AI에게 재질을 명확히 알려주어 사실감을 높입니다.

---

## 2교시: 내부 구조 분해 이미지 생성 (The Exploded View)

제품이 공중에서 분해된 모습을 생성합니다. 1교시에서 만든 이미지와 **동일한 조명과 구도**를 유지하는 것이 가장 중요합니다.

### 📝 프롬프트 분석 (Explosion Logic)

1교시 프롬프트를 베이스로 하되, **'Exploded technical diagram(분해 기술 도면)'** 키워드를 추가합니다.

> **Prompt Input:** Exploded technical diagram view of the same matte black over-ear headphones, every component precisely separated and floating in perfect alignment, suspended in mid-air against a deep black studio background. Visible internal structure including copper wiring, drivers, magnets, circuit boards, padding layers, and metal frame. Hyper-realistic product visualization, ultra-sharp focus, studio rim lighting identical to the hero shot, soft highlights tracing each component, controlled reflections on matte and metal surfaces. Cinematic lighting, high contrast, luxury engineering aesthetic, no labels, no annotations, no text. Photorealistic, ultra-high resolution, Apple-style industrial design render, dramatic and clean.
> 

### ✅ 핵심 포인트

- **부품 나열 (Internal Structure):** 구리선, 드라이버, 자석 등 내부 부품을 구체적으로 명시해야 디테일이 살아납니다.
- **정렬 (Perfect Alignment):** 부품들이 무작위로 흩어지는 것이 아니라, 조립되는 라인 그대로 떠 있어야 합니다.
- **일관성 (Identical to hero shot):** 조명이 1교시 이미지와 똑같아야 영상 변환 시 자연스럽습니다.

---

## 3교시: 영상화 및 트랜지션 (Whisk - Video Gen)

두 이미지를 연결하여, 제품이 완성된 상태에서 부품별로 분해되는 영상을 만듭니다. (Image-to-Video 툴 사용: Runway, Kling, Luma 등)

### 🎬 영상 지시 프롬프트 (Motion Prompt)

> **Prompt Input:** Smoothly transition from the assembled product to the exploded view, slow motion Professional internal tech showcase, Apple style animation, high quality professional 3D explosion Slow with professional disassembly of the parts before showing exploded view.
> 

### ✅ 제작 테크닉

1. **Start Frame:** 1교시의 '완성된 헤드폰' 이미지를 넣습니다.
2. **End Frame:** 2교시의 '분해된 헤드폰' 이미지를 넣습니다.
3. **Prompt:** 위의 영상 지시 프롬프트를 입력합니다.
4. **팁:** "Apple style animation"은 부드러운 가속/감속(Easing)을 유도하여 고급스러운 움직임을 만듭니다.

---

## 💡 Pro Tip: 완성도를 높이는 비결

- **배경의 통일성:** 두 이미지 모두 `Deep black background`를 사용했습니다. 배경이 흔들리지 않아야 시선이 제품에 집중됩니다.
- **부정 프롬프트 (Negative Prompt) 활용:** 이미지 생성 시 `text, logo, watermark, messy, blurry` 등을 넣어 불필요한 요소를 제거하세요.
- **시드(Seed) 고정:** 가능하다면 1교시와 2교시 생성 시 같은 시드 번호를 사용하여 제품의 디자인 일관성을 유지하는 것이 좋습니다.

### 오늘 만든 이미지들 링크

![Gemini_Generated_Image_i595k8i595k8i595.jpg](Gemini_Generated_Image_i595k8i595k8i595.jpg)

![Gemini_Generated_Image_xbz9vtxbz9vtxbz9.jpg](Gemini_Generated_Image_xbz9vtxbz9vtxbz9.jpg)

![Whisk_d65d051389b7b9c8cc24fade26628cd1eg.png](Whisk_d65d051389b7b9c8cc24fade26628cd1eg.png)

![Whisk_e8d9e6d8b22825db65a4746915f28f4aeg.png](Whisk_e8d9e6d8b22825db65a4746915f28f4aeg.png)

![Whisk_fefec51181637889b8e4acced2969b85eg.png](Whisk_fefec51181637889b8e4acced2969b85eg.png)

위의 프롬프트를 사용해서 다른 제품을 만들고 나노바나나 프로 + 위스크 + veo 3.1을 사용해보세요 :)

### 구글 OPAL 링크

[https://opal.google/app/1nCKp8cRTwAaHkb5Vxrj-4WQjS_tYwOqj?shared](https://opal.google/app/1nCKp8cRTwAaHkb5Vxrj-4WQjS_tYwOqj?shared)

### 숙제

---

1. 구글 OPAL 사용해서 여러가지 영상 한번에 만드는 워크플로우 만들기 
2. 첫번째 프레임, 끝 프레임 정해서 영상 만드는 연습하기