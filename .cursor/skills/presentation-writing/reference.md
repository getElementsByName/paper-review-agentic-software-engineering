# Presentation Writing Guide — Reference

Detailed tables, examples, and extended checklist for the presentation-writing skill. See [SKILL.md](SKILL.md) for the main instructions.

---

## Source and confidence (출처·신뢰 구분) — Full table

| 구분(Class) | 의미(Meaning) |
|-------------|----------------|
| 원문 근거(Direct Evidence) | 원문(논문·영상·자료 등)에서 직접 확인되는 내용 |
| 발표 해석(Interpretation) | 원문을 기반으로 실무 적용을 위해 확장한 내용 |
| 탐색 가이드(Exploration Guide) | 발표 후 추가 탐색을 돕기 위해 정리한 키워드/읽기 경로 |

Use these labels so that "무엇이 사실인지" and "무엇을 선택할지" can be separated in discussion.

**Placement:** Put each source line at the **end of the slide** (right before `<!-- 발표 스크립트`), with the **"참고:"** prefix (e.g. `참고: 출처(원문): §4`). This keeps references visible but low-prominence.

---

## Notation examples (표기 예시)

- **Acronyms**: First use: **한글(Full Name in English, ACRONYM)**.
- **Bilingual**: Use only for **발표 키워드**, **전문용어**, or **헷갈리거나 낯선 경우**—not for every English term. Format: **한글(English)** or **English (한글)**; keep 한글-first order where used.

Examples (keywords / technical or unfamiliar terms; replace with your talk’s terms as needed):

- 대규모 언어 모델(Large Language Model, LLM)
- 인간 피드백 기반 강화학습(Reinforcement Learning from Human Feedback, RLHF)
- 모델 컨텍스트 프로토콜(Model Context Protocol, MCP)
- 구조화된 에이전틱 소프트웨어 엔지니어링(Structured Agentic Software Engineering, SASE)
- 연속 통합/연속 배포(Continuous Integration/Continuous Delivery, CI/CD)

---

## Speaker script block examples

Script content will vary by talk; the structure (one block per slide, context + transition) stays the same.

**Example 1 — After a slide on “논문의 취지” (or similar intro slide)**

```html
<!--
발표 스크립트
이 논문은 "우리가 완성된 해답을 만들었다"고 주장하지 않습니다.
대신, 앞으로 에이전틱 소프트웨어 엔지니어링을 논의할 때 필요한 공통 좌표계를 제시합니다.
이 태도는 매우 중요합니다.
왜냐하면 지금 이 분야는 도구가 너무 빠르게 변하고 있어서, 고정된 정답 프레임이 금방 낡기 때문입니다.
따라서 논문은 기술 스택 고정안이 아니라, 사고 구조와 용어 체계를 제안합니다.
발표 전체도 이 취지를 따라, 특정 벤더 중심이 아니라 구조 중심으로 설명하겠습니다.
-->
```

**Example 2 — After “발표 이야기 지도” (or similar flow slide)**

```html
<!--
발표 스크립트
흐름을 먼저 제시하는 이유는, 오늘 내용이 단일 도구 소개가 아니라 시스템 설계 이야기이기 때문입니다.
초반에는 문제의 성격을 정의하고, 중반에는 구조적 해법을 설명합니다.
후반에는 발표 이후 추가로 찾아볼 수 있는 탐색 경로와 쟁점 언어를 다룹니다.
즉 "문제 인식 → 구조 이해 → 탐색 확장"의 순서입니다.
이 순서를 유지해야 발표가 자연스럽게 이어지고, 각 슬라이드의 의미가 분명해집니다.
-->
```

Scripts add context and transition; they do not repeat the slide bullets verbatim.

---

## Key message per slide (페이지별 핵심 메시지) — Examples

**나쁜 예**: 제목이 "RPI 루프 소개"만 있으면, 슬라이드가 "무엇을 기억해야 하는지" 한 문장으로 드러나지 않는다.

**좋은 예**: 제목이나 첫 문장이 메시지를 담는다. 예: "RPI는 조사–계획–구현의 반복으로 의도를 압축한다" 또는 첫 불릿에 "Research 단계의 핵심: 문서가 아니라 코드 기반 진실을 압축한다"처럼 한 문장으로 정리한다. 청중이 "이 슬라이드에서 꼭 기억할 것"을 말할 수 있으면 된다.

---

## Extended checklist (확장 체크리스트)

When adding or revising slides, use this in addition to the short checklist in SKILL.md:

- [ ] **Story step**: If the project defines a story flow or slide structure (e.g. five steps such as Why Now → Signal → Core → Exploration → Discussion), the slide belongs to one of those steps and is in the right place in the deck.
- [ ] **Key message**: The slide has a single clear key message, stated in the title or the first line/bullet (or in a KeyMessage/similar component if the project uses one).
- [ ] **Source labels**: Every claim from a paper or external talk has a source line at the **bottom of the slide** with `참고: 출처(원문): §n` or `참고: 보강 해석(Interpretation):` (or Exploration Guide) so the class is clear.
- [ ] **Acronyms**: Every new acronym in the deck has its first use in the form 한글(Full Name, ACRONYM). Later slides may use the acronym only.
- [ ] **Bilingual terms**: Presentation keywords, technical terms, or ambiguous/unfamiliar terms have 한글 병기 (or the reverse); do not require bilingual for every term.
- [ ] **Single script block**: Each slide has at most one `<!-- 발표 스크립트 ... -->` block, placed right after the slide content and before `---`.
- [ ] **Script content**: The script explains why this slide matters, what to stress, or how to transition to the next slide—not a line-by-line read of the bullets.
- [ ] **Slide separator**: Slide boundaries use `---` (and optional layout/class as per Slidev). No duplicate or stray `---` inside a slide.
