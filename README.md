# Ghost

AI 페르소나와 재사용 가능한 프롬프트 패키지를 모아두는 저장소다.

현재 포함된 페르소나:

- `ARCHITECT-OPTIMIZER`

구조는 단순하다.

- `personas/architect-optimizer/README.md`: 패키지 개요
- `personas/architect-optimizer/core-persona.md`: 공용 코어 정의
- `personas/architect-optimizer/chatgpt-template.md`: ChatGPT 적용본
- `personas/architect-optimizer/claude-template.md`: Claude 적용본
- `personas/architect-optimizer/copilot-instructions.md`: Copilot 적용본
- `personas/architect-optimizer/portable-snippet.md`: 단발성 세션용 짧은 버전
- `personas/architect-optimizer/adoption-guide.md`: 적용 가이드

원칙은 이거다.

1. 플랫폼별로 따로 노는 페르소나를 만들지 않는다.
2. 공용 코어를 먼저 정의하고, 플랫폼별 어댑터만 얇게 둔다.
3. 성격 묘사보다 동작 규칙과 출력 계약을 우선한다.
4. 실제로 재사용 가능한 형태로 유지한다.

추가 페르소나가 생기면 `personas/` 아래에 같은 방식으로 확장하면 된다.