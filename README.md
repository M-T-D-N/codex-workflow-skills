# Codex Workflow Skills

실제 작업에서 반복되는 판단·실행 문제를 다루는 **9개의 선택 설치형 스킬**입니다. 요청과 기존 기능을 먼저 맞추고, 반복 오류를 근거로 진단하고, 검증된 상태에서 작업을 이어가도록 돕습니다.

Nine focused, independently installable skills for grounded changes, evidence-driven debugging, lean execution, bounded delegation, critical review, task handoff, and visual prompt reconstruction.

각 폴더의 `SKILL.md`가 핵심 지침입니다. 필요한 스킬만 설치할 수 있습니다. 원문은 한국어와 영어가 혼합되어 있으며, 이미지 프롬프트 복원 스킬은 기본적으로 한국어·영어 프롬프트를 모두 제공합니다.

개발 안내: 이 스킬 모음은 AI가 생성하고 사용자 요구와 사용 피드백으로 개선했습니다. [전체 고지](#ai-개발-고지)를 확인하세요.

## 스킬 선택

| 스킬 | 해결하는 문제 | 요청 예시 |
|---|---|---|
| [request-grounding](skills/request-grounding/SKILL.md) | 기존 기능과 실제 요구를 확인하기 전에 구현부터 시작함 | “기능 추가 전에 이미 가능한지, 어느 계층을 바꿔야 하는지 확인해줘.” |
| [evidence-driven-debugging](skills/evidence-driven-debugging/SKILL.md) | 첫 수정 후 재발하거나 여러 원인이 혼재함 | “수정 후에도 재발했어. 원인을 판별할 근거를 먼저 찾아줘.” |
| [execute-leanly](skills/execute-leanly/SKILL.md) | 파일 읽기·계획·상태 조회·검증을 반복함 | “검증된 지점부터 남은 작업만 이어서 처리해줘.” |
| [swarm](skills/swarm/SKILL.md) | 위임할 수 있는 구현·근거 수집을 메인이 모두 수행함 | “범위가 명확한 구현과 근거 수집을 적합한 작업자에게 맡기고 결과를 검증해줘.” |
| [adversarial-review](skills/adversarial-review/SKILL.md) | 취합한 결론의 숨은 전제와 중요한 반례를 놓침 | “이 계획을 적대적으로 검토하고 유지할지 판단해줘.” |
| [codex-why](skills/codex-why/SKILL.md) | 관행·추론·과거 결정을 필수 규칙처럼 설명함 | “그 승인이 필수라는 판단은 어떤 현재 규칙에서 나왔어?” |
| [pink-elephant-guard](skills/pink-elephant-guard/SKILL.md) | 폐기된 문구나 구조가 최종 결과에 다시 등장함 | “확정된 방향만으로 바로 사용할 최종 소개문을 작성해줘.” |
| [prepare-codex-handoff](skills/prepare-codex-handoff/SKILL.md) | 새 대화에서 중요한 결정과 검증 상태가 유실됨 | “새 Codex 대화에서 이어갈 인계 프롬프트 하나를 만들어줘.” |
| [visual-prompt-reconstructor](skills/visual-prompt-reconstructor/SKILL.md) | 이미지를 피상적인 스타일 키워드로만 설명함 | “이 참고 이미지를 재현할 한국어·영어 프롬프트를 만들어줘.” |

## 설치

### Codex에 요청

`skill-installer`를 사용할 수 있는 환경에서는 원하는 폴더의 GitHub 주소를 지정합니다.

```text
$skill-installer https://github.com/M-T-D-N/codex-workflow-skills/tree/main/skills/adversarial-review
```

다른 스킬을 설치하려면 마지막 폴더 이름을 바꾸세요. 기존에 같은 이름의 스킬이 있으면 내용을 비교하고 유지·교체할 대상을 먼저 결정하세요.

### 직접 복사

1. 이 저장소의 **Code → Download ZIP**으로 다운로드하고 압축을 풉니다.
2. `skills/` 안에서 필요한 스킬 폴더를 통째로 복사합니다. `references/`와 `agents/`가 있다면 포함합니다.
3. 개인 전체 작업에 쓰려면 사용자 홈의 `.agents/skills/` 아래에, 특정 저장소에서만 쓰려면 해당 저장소의 `.agents/skills/` 아래에 넣습니다.
4. Codex에서 스킬을 확인합니다. 바로 나타나지 않으면 Codex를 다시 시작합니다.

설치 결과 예시:

```text
.agents/skills/
└── adversarial-review/
    └── SKILL.md
```

공식 설치 위치와 동작: [OpenAI — Build skills](https://learn.chatgpt.com/docs/build-skills). 이 저장소는 개별 폴더 설치용 배포판이며 플러그인 마켓 등록은 포함하지 않습니다.

## 사용

스킬을 명시적으로 지정하려면 요청에 `$스킬이름`을 넣습니다.

```text
$adversarial-review 이 설계의 핵심 전제와 실제 반례를 검토해줘.
$prepare-codex-handoff 현재 작업을 새 대화에서 이어갈 프롬프트로 정리해줘.
$visual-prompt-reconstructor 첨부 이미지를 재현할 한국어·영어 프롬프트를 만들어줘.
```

스킬 설명과 요청이 맞으면 호스트가 자동 선택할 수도 있습니다. `adversarial-review`는 내용상 명시적인 적대적 검토 요청에만 적용합니다. 설명·진단·검토 요청만으로 파일 수정이나 외부 게시를 시작하지 않습니다.

## 의존성과 적용 범위

- **일반 워크플로 스킬:** 별도의 기억 서버나 전용 실행 서비스가 필요하지 않습니다. 다른 스킬 이름은 선택적 연계 안내입니다. 필요한 도구가 없으면 미확인 사항을 표시하며 결과를 꾸며내지 않습니다.
- **swarm:** 범위와 결과 확인 방법이 명확한 구현·근거 수집을 적합한 작업자에게 맡깁니다. 검증된 좁은 작업에는 Local Qwen을, 그 밖의 준비된 작업에는 호스트가 지원하는 `gpt-5.6-luna`의 `max` 설정을 기본으로 선택합니다. Luna는 한 번에 한 작업만 수행하며, 완료된 뒤 다음 작업에 순차 재사용할 수 있습니다. 단순 경과 시간·침묵·대기 도구의 시간 초과만으로 실패를 판정하지 않고, 사용자·호스트의 제한과 실제 실행 상태를 따릅니다. 실패한 목표의 연쇄 재위임은 금지합니다. 이 배포판은 모델이나 실행기를 제공하지 않으며, 필요한 모델·도구·권한이 없으면 메인이 수행합니다. [설정 계약](skills/swarm/references/worker-setup.md)과 [Luna 실행·가격 근거](skills/swarm/references/luna-lane.md)를 참고하세요. 가격표는 날짜가 명시된 API 비교 자료이며 실제 Codex 요금·절감액을 뜻하지 않습니다.
- **visual-prompt-reconstructor:** 이미지를 읽을 수 있는 호스트와 실제 참고 이미지가 필요합니다. 생성 도구는 프롬프트 작성만 할 때는 필요하지 않습니다.
- **Codex 전용 동작:** `agents/openai.yaml`, task 관리, 도구·승인 방식은 호스트에 따라 다릅니다. 다른 에이전트에서의 동일 동작은 검증하지 않았습니다.

스킬은 현재 사용자 요청과 적용되는 상위 지침을 따릅니다. 프로젝트의 보안·승인·데이터 경계를 바꾸지 않습니다. 모든 스킬을 연쇄 적용할 필요는 없습니다. 예를 들어 반복 오류 진단이 필요한 경우에는 해당 진단 스킬이 작업을 맡고, 원인과 수정이 확정된 뒤 실행 스킬로 이어갈 수 있습니다.

## 배포판과 유지 관리

개인 작업용 스킬을 바탕으로 Codex의 도움을 받아 배포용으로 편집했습니다. 개인 절대 경로와 전용 기억 서비스 참조를 일반화했고, `swarm`은 특정 모델·스크립트가 없어도 메인이 작업을 수행할 수 있는 형태로 조정했습니다. 개인 환경의 실행 로그, 원시 대화, 인증 정보와 로컬 런타임은 포함하지 않습니다.

이 저장소는 OpenAI 공식 배포물이 아닙니다. 최초 공개판은 YAML/frontmatter, 내부 참조, 배포 파일 구성을 확인했습니다. 모든 수신자 환경에서의 동작이나 작업 품질을 보증하는 종단 간 실행 검증을 의미하지는 않습니다.

문제를 보고할 때는 스킬 이름, 기대한 적용 범위, 실제 동작과 민감정보를 제거한 짧은 재현 요청을 알려주세요. 개정은 재현 가능한 문제에 필요한 범위로 제한합니다.

## AI 개발 고지

스킬 지침과 배포판 변경 대부분은 사용자가 제공한 요구사항과 반복적인 수용 요청에 따라 OpenAI Codex가 작성·수정했습니다. 저장소 소유자는 소스 내용을 직접 읽거나 검토하지 않았습니다. 개인 설치본의 개선은 소유자의 Codex 환경에서의 사용 피드백을 바탕으로 했으며, 이번 배포판의 검증은 자동화된 형식·참조·파일 구성 점검과 Codex의 내용 검토를 근거로 합니다. 독립적인 제3자 코드 검토나 보안 감사는 수행되지 않았습니다.

**요약:** AI가 생성하고 사용자의 사용 피드백으로 개선했으며, 수동 소스 리뷰를 거치지 않았습니다. 배포판 전체에 대한 별도 사용자 기능 시험은 수행하지 않았습니다.

## 라이선스

Copyright 2026 M-T-D-N. 이 스킬 모음은 [Apache License 2.0](LICENSE)으로 제공합니다. 스킬을 개별 설치할 때도 라이선스를 함께 가져갈 수 있도록 각 스킬 폴더에 `LICENSE.txt`를 포함했습니다.
