---
name: step-by-step-codework
description: "spring BE 코드를 구현할 때의 지침. 사용자가 직접 명시적으로 이 스킬을 사용하라고 할 경우에만 사용한다. spring-backend-change-procedure 스킬과 함께 사용할 때는 spring-backend-change-procedure 지침을 우선으로 삼는다."
---

계획서에 작성된 내용을 토대로 작고 조각난 단계별(small baby steps)로 나눠서 AI는 단계별로 진행한다. 이 때, 구현을 할 때마다 조각난 스텝에서 단 하나의 스텝만 하나씩 수행하도록 제어한다. 이 때, 각 스텝별 작업이 완료되면 그 작업에 대한 커밋메시지 예시를 작성해 사용자에게 제공한다. 커밋메시지 형식은 레포의 CLAUDE.md·최근 커밋 형식을 따른다.

small baby steps란
실패했을 때 원인을 즉시 파악할 수 있고, 언제든 롤백(Undo) 가능한 최소 단위의 변화이다. small baby steps는 다음과 같은 특징을 갖는다. 아래의 특징을 갖는다면 단계로 쪼갠다.

- 피드백 루프가 1~2분 이내인 단위
- 구조적 변경 혹은 행동적 변경
- 관찰 가능한 한 가지의 변화
- 언제든 지워버릴 수 있는 단위
