---
name: presentation-writing
description: Guides creation and editing of Slidev presentation slides (e.g. slides.md) with consistent notation, source attribution, and speaker script format. Use when editing slide markdown, working on 발표 자료 (presentation materials), adding or revising slides, or when the user asks for presentation writing conventions, slide structure, or 발표 가이드.
---

# Presentation Writing Guide (발표 작성 가이드)

This skill defines how to create and edit Slidev-based presentation slides (typically `slides.md` or the project’s main slide file). Follow these rules whenever adding, revising, or restructuring slides or speaker scripts in the current presentation.

## 1. Purpose and scope

- **Applies to**: The presentation file you are editing (commonly `slides.md`) and any Slidev markdown used for talks in the current project.
- **Tasks**: Adding/editing slides, writing or updating speaker scripts, attributing sources, applying notation rules, and keeping story flow consistent.
- **Audience**: Content is for both the audience (slide body) and the speaker (script comments). Keep "원문 근거" and "발표 해석" clearly separated so the audience can tell fact from interpretation.

## 2. Story Map (슬라이드 구성 원칙)

If the project defines its own story flow or slide structure (e.g. in a README or convention doc), follow that first. Otherwise, the following five-step flow is a **recommended example** so the deck reads as "문제 인식 → 구조 이해 → 탐색 확장". Other projects may use fewer steps or different names.

1. **Why Now** – 왜 지금 이 주제가 구조적 필수인가
2. **Practice / Research Signal** – 현장 신호(Practice Signal)와 연구 신호(Research Signal)
3. **Core structure** – 주제의 핵심 구조
4. **Post-talk exploration** – 후속 탐색 가이드(Post-talk Exploration Guide): 키워드와 읽기 경로
5. **Discussion** – 토론 질문(Discussion Questions)과 쟁점 언어(Issue Vocabulary)

When inserting or moving slides, place them in the step that matches their role. If using this flow, do not put execution checklists or deep dives before the "Why Now" and signal slides.

## 3. 페이지별 핵심 메시지 (Key message per slide)

- **원칙**: 각 슬라이드는 **한 페이지당 하나의 핵심 메시지**를 갖는다. 청중이 "이 슬라이드에서 꼭 기억할 것"을 한 문장으로 말할 수 있어야 함.
- **표현 위치**: (1) 슬라이드 **제목**이 메시지를 담거나, (2) 제목 아래 **첫 문장/첫 불릿**이 메시지를 담음. 필요 시 슬라이드 하단에 `핵심 메시지: …` 한 줄을 두는 것도 허용(선택).
- **KeyMessage (or similar) component**: If the project provides a KeyMessage or similar component (e.g. `<KeyMessage message="한 문장 핵심 메시지" />`), place it immediately after the title so the audience can quickly see the slide’s main point. When adding slides, set the message to match the slide’s role and script emphasis. Cover, outline, and transition slides may omit it. **If the project does not use such a component**, state the key message in the title or in the first sentence/bullet.
- **Story/structure**: If the project uses a story map or defined steps, check that the key message reflects the slide’s role in that flow.
- **스크립트와의 관계**: 발표 스크립트는 이 핵심 메시지를 강조하고, 다음 슬라이드로 넘어가는 이유(전환)를 설명하는 데 쓴다. 스크립트가 메시지를 흐리게 하지 않도록 함.

슬라이드 구성 요소와 메시지 위치 (핵심 메시지 컴포넌트가 있을 때):

```
[슬라이드]
  제목
  <KeyMessage message="한 문장 핵심 메시지" />   ← 해당 컴포넌트가 있을 때
  본문 불릿
  참고: 출처 ...  (또는 <SourceNote text="..." /> 등 프로젝트에서 쓰는 방식)
  <!-- 발표 스크립트: 메시지 강조 + 전환 -->
```

## 4. Source and confidence (출처·신뢰 구분)

Use three classes for every claim that comes from literature or external material:

| Class | Meaning |
|-------|--------|
| **원문 근거 (Direct Evidence)** | Content directly verifiable in the cited paper or source. |
| **발표 해석 (Interpretation)** | Extension or application of the source for this talk/context. |
| **탐색 가이드 (Exploration Guide)** | Keywords, reading paths, or follow-up pointers for after the talk. |

**In-slide markup:**

- Place source lines at the **bottom of each slide** (immediately before the script block) with the **"참고:"** prefix to keep references low-prominence.
- For direct citations: `참고: 출처(원문): §n` or `참고: 출처(원문): Abstract, §1` (section as in the paper).
- For mixed or enhanced: `참고: 출처(원문 + 보강): ...`
- For your interpretation: `참고: 보강 해석(Interpretation): ...`

Never mix "원문 근거" and "발표 해석" without labeling so that "무엇이 사실인지" and "무엇을 선택할지" stay separable in discussion. For the full table and examples, see [reference.md](reference.md).

## 5. Notation (표기 규칙)

- **Acronyms (약어)**: On first use in the deck, write **한글(Full Name in English, ACronym)**. Example: 대규모 언어 모델(Large Language Model, LLM).
- **Bilingual (이중언어)**: Use **한글(English)** or **English (한글)** only for **발표 키워드(presentation keywords), 전문용어(technical terms), or terms that are 헷갈리는(ambiguous) or 낯선(unfamiliar)** to the audience. Do not bilingualize every English term.
- **Rationale**: Reduces misinterpretation where it matters; avoids clutter on common or obvious terms. Aligns with reducing implicit knowledge for terms that need it.

Examples (more in [reference.md](reference.md)):

- 대규모 언어 모델(Large Language Model, LLM)
- 인간 피드백 기반 강화학습(Reinforcement Learning from Human Feedback, RLHF)
- 모델 컨텍스트 프로토콜(Model Context Protocol, MCP)

## 6. Speaker script format (발표 스크립트 형식)

- **Place**: Immediately after the slide content, before the next `---`.
- **Format**: A single HTML comment block:
  ```html
  <!--
  발표 스크립트
  [1–3 short paragraphs: context, emphasis, transition to next slide. Do not simply read the slide bullets.]
  -->
  ```
- **Content**: Add context, stress one or two points, and bridge to the next slide. Do not duplicate the slide text verbatim. Scripts are for "맥락·전환 보강".

## 7. Checklist when editing slides

Before considering a slide or section done:

- [ ] **Title**: For keywords, technical terms, or unfamiliar terms, includes 한글–English (or English–한글) as appropriate.
- [ ] **핵심 메시지**: 해당 슬라이드의 핵심 메시지가 한 문장으로 명확하다. 프로젝트에서 KeyMessage(또는 유사) 컴포넌트를 쓰면 제목 직후에 넣었는지 확인하고, 쓰지 않으면 제목 또는 첫 문장에 담겨 있는지 확인한다.
- [ ] **Claims from papers/talks**: Marked at the bottom of the slide with `참고: 출처(원문):` or `참고: 보강 해석(Interpretation):` as appropriate (or with a project-specific component such as SourceNote if used).
- [ ] **New acronyms**: First occurrence has 풀네임(Full Name, ACRONYM) and 한글.
- [ ] **Script**: If the slide has a script block, it’s one `<!-- 발표 스크립트 ... -->` block and adds context/transition, not a copy of the bullets.
- [ ] **Story/structure**: If the project defines a story flow or slide structure, the slide’s position and role match it.

Extended checklist items are in [reference.md](reference.md).

## 8. Reference

- Detailed tables, more notation examples, and script examples: see [reference.md](reference.md).
- Projects may keep their own convention doc or slide file as the source for story flow and component usage.
