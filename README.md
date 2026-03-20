# LinkedIn Writer Agent (Share)

Claude Code 서브에이전트 기반 링크드인 글쓰기 자동화 시스템.

주제를 입력하면 **브랜드 평가 → 기획 → 초안 → 편집**까지 AI가 자동으로 처리합니다.

---

## 특징

- Python 불필요, API 키 불필요, 텔레그램 봇 불필요
- **Claude Code만 있으면 작동**
- `brand_config.md` 파일 하나만 수정하면 누구든 자기 브랜드에 맞게 사용 가능
- 전문 에이전트 5개가 파이프라인으로 협업

---

## 에이전트 구성

| 에이전트 | 역할 |
|---|---|
| `linkedin-writer` | 전체 파이프라인 조율 (오케스트레이터) |
| `brand-strategist` | 주제의 브랜드 적합성 평가 |
| `content-planner` | 기획서 + 훅 3안 생성 |
| `writer` | 1인칭 초안 작성 |
| `editor` | 편집 + 품질 점수 산출 |

---

## 시작하기

### 1. 이 레포지토리 클론 또는 다운로드

```bash
git clone https://github.com/teo-hash/linkedin-writer-agent-share
```

### 2. brand_config.md 작성

`brand_config.md` 파일을 열어서 내 정보로 채웁니다.

```
- 이름 / 직책 / 회사
- 브랜드 포지셔닝 (어떤 사람으로 기억되고 싶은가)
- 핵심 독자
- 콘텐츠 기둥 (주로 다룰 주제)
- 전문 배경 및 레퍼런스
- 글쓰기 톤
- 하지 않을 것
```

> 이 파일만 수정하면 됩니다. 나머지는 건드리지 않아도 됩니다.

### 3. Claude Code로 이 폴더 열기

```bash
cd linkedin-writer-agent-share
claude
```

### 4. 사용

```
링크드인 글 써줘. 주제는 [주제]야.
```

---

## 폴더 구조

```
Linkedin_writer_agent_Share/
├── .claude/
│   └── agents/
│       ├── linkedin-writer.md    ← 메인 오케스트레이터
│       ├── brand-strategist.md
│       ├── content-planner.md
│       ├── writer.md
│       └── editor.md
├── brand_config.md               ← 여기만 수정
├── 사용가이드.md
└── README.md
```

---

## 자세한 사용 방법

[사용가이드.md](사용가이드.md) 참고

---

## 문의

멍멍AI (비개발자의 AI 스터디) https://t.me/ai_together_korea
