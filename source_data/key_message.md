## 논문의 취지
- Our goal is not to offer a definitive solution, but to provide a conceptual scaffold with structured vocabulary to catalyze a community-wide dialogue, pushing the SE community to think beyond its classic, human-centric tenets toward a disciplined, scalable, and trustworthy agentic future.

## 현재 트렌드의 문제
- As the industry forges ahead, a Cambrian explosion of ad-hoc practitioner techniques is emerging. However, these grassroots innovations highlight a vacuum of robust, validated approaches. Current methods, relying heavily on informal, conversational prompting, are inadequate for developing trustworthy large-scale long-lived software. This informality fails to establish the robust processes that are needed for reproducibility, the auditable artifacts required for ensuring trust, or a durable mechanism for human-agent collaboration. It keeps the paradigm locked in the realm of 1-to-1 "agentic coding," rather than unlocking the potential of N-to-N "agentic software engineering" where teams of humans and agents collaborate at scale. Early attempts to impose order, like the Plan-Do-Assess-Review (PDAR) loop, are a crucial shift but do not constitute a complete engineering methodology. This new reality demands more than incremental adjustments; it compels us to fundamentally reconsider the pillars upon which the SE field is built: the Actors, the Processes they follow, the Tools they use, and the Artifacts they shape.

## 소프트웨어 개발을 더 체계적인 "공학적 규율"로 전환
> 에이전틱 소프트웨어 엔지니어링(Agentic SE)이 개발 생산성과 협업 방식, 그리고 지식/프로세스 관리 방식을 근본적으로 변경할 필요가 있다.
>
> 100x/1000x 개발자는 보편적, 정량적 실증치라기보다 관찰/비전 성격이 강하다. 슬라이드에서는 "상징적 표현"으로 다루고, "어떤 실천이 생산성을 좌우하는가(브리핑, 컨텍스트, 검증)"로 논점을 이동하는 것이 안전하다.

- The core purpose of the SE field has always been to ensure solutions are trustworthy and delivered economically, and much of the SE field exists because we cannot assume that every team is composed of "super developers." The industry has long acknowledged the phenomenon of the "10x developers," a small fraction of developers whose impact far exceeds the median. A significant portion of SE, from structured processes like Agile to sophisticated tools like IDEs, is designed to give non-super developers the scaffolding and opportunity to perform at a 10x level. Agentic SE radically reshapes this landscape, moving the conversation beyond 10x to the realm of 100x and even 1,000x productivity while also redefining the characteristics of such top-tier developers, away from raw coding prowess and toward effective collaboration with fleets of agents (aka AI Teammates).
- This ensures that they are living documents that always reflect the complete and current shared understanding of tasks, processes, and a team's collective wisdom and tribal agreements, transforming agentic SE from a craft into a true engineering discipline.

## (외부 데이터 소스) RPI 루프
- 출처: [https://www.youtube.com/watch?v=rmvDxxNubIg](https://www.youtube.com/watch?v=rmvDxxNubIg)
- 조사, 계획, 구현 RPI(Research, Plan, Implement) 루프

### RPI 기본 정의
- Research (조사): 시스템의 작동 방식을 객관적으로 파악하고 문제 해결에 필요한 관련 파일과 라인 번호를 식별합니다. 단순히 모든 코드를 읽는 것이 아니라, 필요한 정보만 골라내어 "압축된 진실" 스냅샷을 만드는 과정입니다.
- Plan (계획): 조사 결과를 바탕으로 수정할 파일, 구체적인 코드 스니펫, 수정 후 테스트 방법 등을 상세히 나열한 계획 파일을 생성합니다. 이 단계는 **"개발자(인간)의 검토"**가 이루어지는 가장 중요한 지점으로, 구현 전에 AI와 인간의 의도를 정렬(Mental Alignment)합니다.
- Implement (구현): 승인된 계획을 바탕으로 실제 코드를 수정합니다. 이미 상세한 계획이 수립되어 있으므로, 에이전트는 낮은 컨텍스트를 유지하면서도 정확하게 작업을 완수할 수 있습니다.

### RPI 워크플로우 (Research -> Plan -> Implement)
- 🔁 Frequent Intentional Compaction

### 핵심 철학
> "항상 smart zone 안에 머물러라"

### 1. Research (진실 압축)
- 목표
  - 코드베이스의 "실제 구조" 이해
  - 관련 파일/라인 정확히 찾기
  - 추측 금지
- 산출물
  - 문제와 관련된 파일 목록
  - 코드 흐름 요약
  - 정확한 참조 위치
- 핵심 메시지: 우리는 "문서"가 아니라 코드 기반 진실을 압축한다.

### 2. Plan (의도 압축)
- 목표
  - 변경 단계 명시
  - 파일명 + 코드 스니펫 포함
  - 테스트 전략 포함
- 중요: 계획이 애매하면 실행은 망한다.
- 좋은 Plan 특징
  - 구체적
  - 실행 가능
  - 검증 단계 포함
  - 변경 전/후 명확

### 3. Implement (저컨텍스트 실행)
- Plan을 그대로 실행
- 중간에 맥락 누적 금지
- 필요 시 다시 compaction
