# 4월10일 금(유튜브)- 토큰값 0원! 구글 Gemma 4로 나만의 AI 코딩 에이전트 육성하기 EP.2 (안티그래비티 바이브 + Gemma 4)

[https://youtu.be/ZtVTeLQDyHQ](https://youtu.be/ZtVTeLQDyHQ)

---

### 

**[💻 맥(Mac) & 윈도우(Windows) 완벽 호환 가이드]**

**1. 로컬 1인기업 서버 띄우기 (터미널/CMD 에 입력)**

- 🍎 **Mac 유저:**

```bash
OLLAMA_HOST=0.0.0.0:11434 ollama serve
```

- 🪟 **Windows 유저 (일반 CMD 기준):**

```bash
set OLLAMA_HOST=0.0.0.0:11434
ollama serve
```

**2. 에이전트 소통 테스트 (새 터미널 열고 입력)**

- 🍎 **Mac 유저:**

```bash
curl <http://localhost:11434/api/generate> -d '{
  "model": "gemma4:e2b",
  "prompt": "ai멘토 제이는 누구야?",
  "stream": false
}'
```

- 🪟 **Windows 유저 (일반 CMD 기준, 윈도우는 따옴표 규칙이 다릅니다!):**

```bash
curl <http://localhost:11434/api/generate> -d "{\\"model\\": \\"gemma4:e2b\\", \\"prompt\\": \\"ai멘토 제이는 누구야?\\", \\"stream\\": false}"
```

---

antigravity.config.json

```jsx
{
  "models": {
    "local": {
      "provider": "openai-compatible",
      "baseUrl": "http://localhost:11434/v1",
      "model": "gemma4:e2b",
      "apiKey": "ollama",
      "temperature": 0.1,
      "maxTokens": 4096,
      "contextWindow": 128000
    }
  },
  "defaultModel": "local",
  "fallback": {
    "enabled": true,
    "model": "claude-opus-4-6",
    "trigger": "context_exceeded"
  }
}
```