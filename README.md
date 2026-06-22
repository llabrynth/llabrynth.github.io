# RTwP RPG

**2D 탑다운 Real-Time with Pause 전술 RPG**

유닛이 행동을 마치고 명령을 기다리는 순간, 게임이 스스로 멈춥니다.
플레이어는 그 틈에 다음 전략을 결정합니다. 생각하는 속도로 진행되는 전투입니다.

---

## 목차

- [게임 소개](#게임-소개)
- [요구사항](#요구사항)
- [설치 및 실행](#설치-및-실행)
- [빌드](#빌드)
- [프로젝트 구조](#프로젝트-구조)
- [핵심 시스템](#핵심-시스템)
- [테스트](#테스트)
- [문서](#문서)

---

## 게임 소개

| 항목 | 내용 |
|------|------|
| 장르 | 2D 탑다운 전술 RTwP RPG |
| 파티 구성 | 3인 (전위 / 중위 / 후위) |
| 전투 방식 | Real-Time with Pause — 파티원 명령 대기 시 자동 정지 |
| 핵심 재미 | 선딜·후딜 타이밍 계산, 포지셔닝(배후 +40% / 측면 +20%) |
| 씬 구성 | MainMenu → Tutorial → ChapterHub → Battle → Ending |
| 특수 시스템 | 패배 시 전투 자동 리플레이, 스킬 트리 성장, 웨이브 스테이지 |

---

## 요구사항

| 항목 | 버전 |
|------|------|
| Unity | 6 (6000.0.x) |
| 렌더 파이프라인 | URP 17.3.0 (패키지 자동 설치) |
| OS | Windows 10 / 11 (64-bit) |
| IDE | Visual Studio 2022 또는 JetBrains Rider |
| Git | 최신 버전 |

---

## 설치 및 실행

### 1. 저장소 클론

```bash
git clone https://github.com/llabrynth/RTwP_RPG.git
cd RTwP_RPG
```

### 2. Unity Hub에서 프로젝트 열기

```
Unity Hub → Projects → Add project from disk → RTwP_RPG 폴더 선택
```

Unity가 패키지를 자동으로 설치합니다 (첫 실행 시 수 분 소요).

### 3. 씬 열기

```
Project 창 → Assets/Scenes/MainMenu.unity 더블클릭
```

### 4. 실행

```
상단 Play (▶) 버튼 클릭
```

---

## 빌드

### Windows Standalone 빌드

```
File → Build Settings
  Platform : PC, Mac & Linux Standalone
  Target   : Windows (x86_64)
  Scenes   : MainMenu, Tutorial, ChapterHub, Battle, Replay, Ending (순서대로)

→ Build 클릭
→ RTwP_RPG.exe 생성
```

### 빌드 결과물 실행

```
RTwP_RPG.exe 더블클릭 (추가 설치 불필요)
```

---

## 프로젝트 구조

```
RTwP_RPG/
├── Assets/
│   ├── Scenes/          MainMenu, Tutorial, ChapterHub, Battle, Replay, Ending
│   ├── Scripts/
│   │   ├── Core/        GameManager, EventBus, SaveLoadService
│   │   ├── Data/        ScriptableObject 정의 (SkillData, StageConfig, CharacterData ...)
│   │   ├── Battle/      전투 로직
│   │   │   └── Tick/   BattleSimulation (20 TPS 고정 틱 엔진)
│   │   ├── UI/          화면·HUD·패널
│   │   ├── Audio/       BGM 크로스페이드 + SFX 풀
│   │   ├── VFX/         파티클 풀, 상태이상 비주얼
│   │   ├── Replay/      전투 재생 시스템
│   │   └── Tutorial/    4단계 튜토리얼 시퀀서
│   └── Tests/
│       └── EditMode/    단위 테스트 24개 (NUnit)
├── docs/
│   ├── adr/             ADR-0001 ~ ADR-0017 (설계 결정 기록)
│   ├── meta/            WBS, Questions
│   ├── weekly/          주간 진행 보고서 (W11 ~ W25)
│   ├── guides/          UI 디자인 가이드, 스테이지 제작 가이드
│   └── architecture.md  기술 스택 & 시스템 설명
├── CLAUDE.md            AI 에이전트 작업 정책
├── AGENTS.md            AI 에이전트 공통 정책 (CLAUDE.md 동일 규칙)
└── README.md            이 파일
```

---

## 핵심 시스템

### RTwP 자동 정지

```
살아있는 파티원 중 IsBusy=false인 유닛이 한 명이라도 있으면
→ BattleSimulation.IsPaused = true (SimTick 루프 정지)

전원 Busy 또는 사망이면
→ IsPaused = false (20 TPS SimTick 재개)
```

`Time.timeScale`을 건드리지 않습니다. 렌더 프레임은 항상 `Interpolate(alpha)`로 부드럽게 유지됩니다.

### 기술 스택

| 분류 | 선택 |
|------|------|
| 엔진 | Unity 6 + URP 17.3.0 |
| 언어 | C# |
| 데이터 | ScriptableObject (ADR-0002) |
| 저장 | Newtonsoft JSON, 로컬 3슬롯 |
| 입력 | New Input System 1.18.0 |
| AI 내비 | Unity NavMesh 2.0.10 |
| 오브젝트 풀 | 수동 Queue\<T\> (ADR-0003) |
| 리플레이 | BattleRecorder + 별도 씬 (ADR-0004) |

---

## 테스트

### 단위 테스트 실행 (Unity Editor)

```
Window → General → Test Runner → EditMode → Run All
```

| 파일 | 케이스 수 | 대상 |
|------|---------|------|
| PositioningTests.cs | 6 | 포지션 판정, 데미지 배율 |
| CombatCalculatorTests.cs | 2 | 최종 데미지 수치 |
| Stage2LogicTests.cs | 9 | 전직, 스킬 해금, 상태이상 |
| Stage3LogicTests.cs | 7 | 난이도 스케일링, 단서 게이지 |
| **합계** | **24** | |

자세한 테스트 결과: [`docs/test-results.md`](docs/test-results.md)

---

## 문서

| 문서 | 경로 |
|------|------|
| 아키텍처 | [`docs/architecture.md`](docs/architecture.md) |
| WBS | [`docs/meta/WBS.md`](docs/meta/WBS.md) |
| ADR 목록 (17개) | [`docs/adr/`](docs/adr/) |
| UI 디자인 가이드 | [`docs/guides/ui-design-guide.md`](docs/guides/ui-design-guide.md) |
| 스테이지 제작 가이드 | [`docs/guides/stage-creation-guide.md`](docs/guides/stage-creation-guide.md) |
| 테스트 결과 | [`docs/test-results.md`](docs/test-results.md) |
| 발표 보고서 | [`docs/presentation-report.md`](docs/presentation-report.md) |
| 주간 보고서 | [`docs/weekly/`](docs/weekly/) |

---

## 라이선스

개인 포트폴리오 프로젝트입니다.
에셋: Cainos Pixel Art Top Down (에셋스토어), Modern GDR Free Icons Pack, NanumGothic (오픈폰트 라이선스)
