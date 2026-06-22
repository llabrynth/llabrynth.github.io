# RTwP RPG — AI 에이전트 작업 정책

> 이 파일은 Claude, Gemini, Copilot 등 모든 AI 에이전트에 적용되는 공통 정책입니다.
> Claude Code 사용자는 `CLAUDE.md`와 동일한 규칙이 적용됩니다.

---

## 핵심 경로 (작업 전 반드시 확인)

| 항목 | 경로 |
|------|------|
| WBS | `docs/meta/WBS.md` |
| ADR 폴더 | `docs/adr/` (현재 최신: ADR-0017) |
| 아키텍처 문서 | `docs/architecture.md` |
| UI 디자인 가이드 | `docs/guides/ui-design-guide.md` |
| 질문 목록 | `docs/meta/Questions.md` |
| 주간 보고서 | `docs/weekly/` |

---

## 규칙 1 — WBS 자동 최신화

**작업을 완료할 때마다 반드시 `docs/meta/WBS.md`를 갱신한다.**

### 갱신 절차

1. `docs/meta/WBS.md`를 읽어 `⬜` 미완료 행 목록 파악
2. 방금 완료한 작업과 매칭되는 행의 `⬜`를 `✅`로, `완료일`을 오늘 날짜로 변경
3. 새로 발견된 작업이 있으면 마지막 섹션에 새 행 추가
4. 파일 상단 `최종 업데이트` 날짜 갱신
5. 변경이 있으면 커밋:
   ```
   git add docs/meta/WBS.md
   git commit -m "docs(wbs): 진행률 X% — <완료 산출물 이름>"
   ```

### 매칭이 애매할 때

- 파일을 직접 읽어 완료 여부 확인
- Unity Editor 작업(Inspector 연결 등)은 사용자에게 직접 확인 후 체크

---

## 규칙 2 — 주간 보고서 자동 생성

**새 주의 첫 작업 시 `docs/weekly/`에 이번 주 파일이 없으면 생성한다.**

### 생성 절차

1. 오늘 날짜로 주차 계산 (예: 2026-05-18 → `2026-W21`)
2. `docs/weekly/2026-W21.md` 파일이 없으면 생성
3. `git log`로 이번 주 커밋 수집
4. 커밋을 `feat` / `fix` / `perf` / `docs` / `chore` 유형으로 분류해 테이블 작성
5. 다음 주 예정은 WBS `⬜` 항목 중 상위 항목만 (진행률·소요일 기재 금지)
6. 커밋: `docs(weekly): 2026-W<주차> 주간 보고서 생성`

---

## 규칙 3 — 질문 목록 자동 갱신

**아래 경우에 `docs/meta/Questions.md`에 항목을 추가한다.**

### 추가 조건

- 사용자가 코드 동작·설계에 대해 직접 질문할 때
- 코드 리뷰·분석 중 동작이 불명확하다고 판단될 때
- 버그가 반복되는 영역에서 근본 원인이 불분명할 때
- 세션에서 나눈 Q&A 중 기억해둘 가치가 있는 것

### 추가 규칙

- 기존 항목과 중복이면 추가하지 않음
- 해결된 질문은 `⬜` → `✅`로 변경하고 근거 컬럼에 해결 방법 한 줄 기록
- 변경 후 커밋: `docs(questions): 질문 N건 추가/해결`

---

## 규칙 4 — UI 디자인 규칙

**UI 씬·패널·컴포넌트를 새로 만들거나 수정할 때 반드시 `docs/guides/ui-design-guide.md`를 준수한다.**

### 필수 확인 항목

- 색상은 `UIColors.cs` 토큰만 사용 (`docs/guides/ui-design-guide.md` §3 참고)
- 패널 테두리: `#7a5c1e` (dim gold) / 강조: `#c8a028` (bright gold)
- 버튼에는 용도별 L자 코너 장식 추가 (가이드 §5-2 크기 테이블 참고)
- 오버레이 패널은 형제 노드 중 **마지막** 순서로 생성 (렌더 순서)
- 섹션 구분에는 `MkSectionLabel` 패턴 사용

### 금지 사항

- `UIColors.cs`에 없는 하드코딩 색상을 코드 본문에 직접 삽입하지 않는다
- 기존 패널의 색상·레이아웃을 근거 없이 임의로 변경하지 않는다

---

## 규칙 5 — ADR 자동 생성

**중대한 의사결정이 있을 때 반드시 코드 작성 전에 ADR을 작성한다.**

### ADR이 필요한 순간

| 트리거 | 예시 |
|--------|------|
| 기술·패턴·라이브러리 선택 | "A 방식 vs B 방식 중 무엇을 쓸까?" |
| 기존 설계 변경·폐기 | 씬 구조 변경, 컴포넌트 분리·통합 |
| 두 개 이상의 구현 방법이 경합 | 이벤트 vs 폴링 |
| 나중에 "왜 이렇게 했죠?" 질문이 올 결정 | 시스템 간 의존 방향 |

### ADR이 불필요한 경우

- 버그 수정 (근본 설계 변경이 없는 경우)
- 수치 조정 (볼륨, 타이밍, 좌표, 색상)
- 이름 변경·리팩터링 (동작 동일)
- 단순 기능 추가 (기존 패턴 그대로 따를 때)

### 파일 규칙

```
docs/adr/ADR-XXXX-짧은-제목.md
```

번호는 `docs/adr/` 폴더에서 가장 큰 번호 + 1. 현재 최신: **ADR-0017**.

### ADR 템플릿

```markdown
# ADR-XXXX: 결정 제목

- **날짜:** YYYY-MM-DD
- **상태:** 확정 | 검토 중 | 폐기

## 배경
이 결정이 필요했던 이유와 맥락.

## 결정
무엇을 선택했는가. 한 문장으로 요약.

## 대안

| 대안 | 검토 결과 |
|------|-----------|
| 대안 A | 왜 선택하지 않았는가 |

## 결과
- **장점:** 이 결정으로 얻은 것
- **단점:** 감수해야 하는 트레이드오프
- **파생 결정:** 이 결정으로 인해 새로 생긴 결정
```

커밋:
```
git add docs/adr/ADR-XXXX-제목.md
git commit -m "docs(adr): ADR-XXXX <결정 제목>"
```

---

## 프로젝트 컨텍스트 요약

### 핵심 아키텍처

- **데이터:** ScriptableObject (SkillData, CharacterData, StageConfig 등) — 런타임 변경 없음
- **상태:** MonoBehaviour (UnitController, UnitCombatAction, UnitStats)
- **통신:** EventBus 정적 클래스 (On / Emit / Off / Clear)
- **시뮬레이션:** BattleSimulation 20 TPS 고정 틱, `unscaledDeltaTime` accumulator

### RTwP 시간 제어 핵심 규칙

```
Time.timeScale 절대 수정 금지.
BattleSimulation.IsPaused 플래그로 SimTick() 루프만 제어한다.
```

### 씬 구조

```
MainMenu → Tutorial → ChapterHub → Battle → ChapterHub (반복)
                                          ↘ Replay (패배 시)
                               (보스 클리어) → Ending
```

### 유닛 색상 규칙

| 상태 | 색상 |
|------|------|
| 파티원 기본 | `Color.white` |
| 적 기본 | `(1, 0.2, 0.2, 1)` 빨간색 |
| 행동 중(IsBusy) | `(0.6, 0.6, 0.6)` 회색 — 아군만 |
| 패링 활성 | `(1, 0.85, 0.1)` 금색 |
| 사망 | `_baseColor.rgb` 알파 2초 페이드아웃 |

### Sorting Layer 규칙 (ADR-0014)

모든 동적 오브젝트는 **Layer 1** 단일 레이어 사용. order 구간:

| 구간 | 역할 |
|------|------|
| 0–99 | 바닥 오버레이 (SelectionRing, MoveRange) |
| 100–999 | 유닛 (IsometricYSort: -y×100+1000) |
| 1000–1099 | 유닛 위 링 (TargetIndicator) |
| 1100–1299 | 스킬 장판 / 패링 타이머 |
| 1300–1399 | 유닛 부착 UI (EnemyHPBar) |
| 1400+ | 텍스트 팝업 (DamagePopup) |

---

## 커밋 컨벤션

```
feat(scope):  새 기능
fix(scope):   버그 수정
perf(scope):  성능 개선
docs(scope):  문서
chore(scope): 설정·정리
refactor:     동작 변경 없는 구조 개선
```

모든 커밋 끝에 Co-Authored-By 불필요. 간결하게 한 줄 요약.
