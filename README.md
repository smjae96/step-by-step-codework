# step-by-step-codework

> 구현 계획을 아주 작은 단계(small baby steps)로 나눠, Claude가 한 번에 한 단계만 구현하고 단계마다 커밋 메시지 예시를 주게 하는 Claude 스킬

## 왜 만들었나
AI에게 구현 계획을 넘기면 여러 파일을 한 번에 크게 바꾸는 경우가 많았다.
그러면 중간에 문제가 생겼을 때 어느 변경이 원인인지 찾기 어렵고, 일부만 되돌리기도 힘들었다.
실패하면 바로 원인을 알 수 있고 언제든 지울 수 있는 단위로만 진행하도록 만들었다.

## 언제 쓰나
명시적으로 요청할 때만 쓰는 스킬이다.
- "step-by-step-codework 스킬로 이 계획 구현해줘"
- "이 플랜 baby step으로 쪼개서 하나씩 진행해줘"
- "한 단계씩만 구현하고 커밋 메시지도 같이 줘"

## 무엇을 하나
- 계획서 내용을 small baby steps로 쪼갠다
- 한 번에 단 하나의 단계만 구현한다
- 단계가 끝날 때마다 그 작업의 커밋 메시지 예시를 준다(레포의 CLAUDE.md·최근 커밋 형식에 맞춤)
- 단계를 나누는 기준: 피드백 루프가 1~2분 이내 / 구조적 변경 혹은 행동적 변경 중 하나 / 관찰 가능한 한 가지 변화 / 언제든 지워버릴 수 있는 크기

## 설치
Claude Code
```bash
mkdir -p ~/.claude/skills/step-by-step-codework
curl -L https://raw.githubusercontent.com/smjae96/step-by-step-codework/main/SKILL.md -o ~/.claude/skills/step-by-step-codework/SKILL.md
```

Claude 앱(claude.ai): 이 레포 폴더를 zip으로 묶어 설정 > 기능 > 스킬에서 업로드

## 함께 쓰면 좋은 스킬
모음 레포: https://github.com/smjae96/claude-skills
- [spring-backend-change-procedure](https://github.com/smjae96/spring-backend-change-procedure) — Spring 백엔드 코드 변경 표준 절차. 함께 쓸 때는 이 스킬의 지침이 우선한다

## License
MIT
