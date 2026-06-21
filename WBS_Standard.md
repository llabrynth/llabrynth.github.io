# RTwP RPG — WBS (표준 구성)
<!-- 범위(Scope) 기반 계층 분류 — 2026-06-21 -->
<!-- 시간 순서가 아닌 "무엇을 만드는가" 중심으로 재편 -->

> **프로젝트명:** RTwP RPG
> **완료 기준:** 산출물이 동작하고 통합 테스트를 통과한 상태
> **일정:** `docs/meta/WBS_Narrative.md` 참조

범례: ✅ 완료 | ⬜ 미완료

---

## 1.0 전투 엔진

### 1.1 시뮬레이션 코어

| ID | 산출물 | 상태 |
|----|--------|------|
| 1.1.1 | 20 TPS 고정 틱 루프 (BattleSimulation — accumulator 방식) | ✅ |
| 1.1.2 | RTwP 자동 정지 판정 (CheckAutoFreeze — IsBusy 기반) | ✅ |
| 1.1.3 | 명령 큐 (CommandQueue — 데드락 방지 Update 단일 경로) | ✅ |
| 1.1.4 | 유닛 심 상태 (UnitSimState — CurrentPosition / PrevPosition / IsBusy) | ✅ |
| 1.1.5 | 렌더 보간 (Interpolate — 매 프레임 Lerp) | ✅ |

### 1.2 전투 판정

| ID | 산출물 | 상태 |
|----|--------|------|
| 1.2.1 | 데미지 계산기 (CombatCalculator — 커버 방어 보정 포함) | ✅ |
| 1.2.2 | 포지셔닝 보너스 (PositioningCalculator — 배후 +30%, 측면 +15%) | ✅ |
| 1.2.3 | 패링 판정 & 반격 (공격자 1타일 Knockback + "패링!" 팝업) | ✅ |
| 1.2.4 | 회피 판정 (DodgeGraceTimer 0.5초 유예 + AP 회복) | ✅ |

### 1.3 행동 상태머신

| ID | 산출물 | 상태 |
|----|--------|------|
| 1.3.1 | 행동 페이즈 머신 (UnitCombatAction — PreDelay → Acting → PostDelay) | ✅ |
| 1.3.2 | Positional 스킬 처리 | ✅ |
| 1.3.3 | Directional 스킬 처리 (방향 입력 + 다중 타겟) | ✅ |
| 1.3.4 | 자체 발동 스킬 (isInstantSelf — 패링/회피) | ✅ |
| 1.3.5 | 연속 투사체 (3발 사격 — _activeProjectiles 리스트) | ✅ |

### 1.4 이동 & 지형

| ID | 산출물 | 상태 |
|----|--------|------|
| 1.4.1 | 이소메트릭 그리드 변환 (IsometricGrid — GridToWorld) | ✅ |
| 1.4.2 | A* 경로탐색 (AStarPathfinder — 이동 비용 + Obstacle) | ✅ |
| 1.4.3 | 지형 타일 데이터 (TerrainTileData & GridManager) | ✅ |

### 1.5 투사체 시스템

| ID | 산출물 | 상태 |
|----|--------|------|
| 1.5.1 | 틱 기반 투사체 이동 (Projectile — TickMove + Interpolate) | ✅ |
| 1.5.2 | 투사체 프리팹 (Projectile_Arrow) | ✅ |

---

## 2.0 캐릭터 시스템

### 2.1 스탯 & 성장

| ID | 산출물 | 상태 |
|----|--------|------|
| 2.1.1 | 스탯 파이프라인 (UnitStats + StatModifier) | ✅ |
| 2.1.2 | 클래스 & 전직 데이터 (ClassData SO) | ✅ |
| 2.1.3 | AP 회복 시스템 (APRecoveryHandler — 20/sec 기본값) | ✅ |
| 2.1.4 | XP 집계 & 레벨업 (GameManager.OnBattleWon — xpPerLevel) | ✅ |
| 2.1.5 | 레벨업 스탯 증가 (ClassData.levelUpStatGains — 레벨당 증가량 정의) | ⬜ |
| 2.1.6 | 레벨업 UI 피드백 (레벨업 팝업 — "+레벨!" + 스탯 목록) | ⬜ |
| 2.1.7 | SaveData 레벨/XP 저장·복원 | ⬜ |

### 2.2 스킬 시스템

| ID | 산출물 | 상태 |
|----|--------|------|
| 2.2.1 | 스킬 데이터 SO (SkillData — DamageType / IndicatorShape / SkillUsage) | ✅ |
| 2.2.2 | 스킬 트리 컴포넌트 (SkillTreeComponent + RestoreFromSave) | ✅ |
| 2.2.3 | 스킬 덱 관리 (A/B 토글, 슬롯 4개) | ✅ |
| 2.2.4 | 스킬 콘텐츠 — Vanguard (Tier1×3 + Tier2×2) | ✅ |
| 2.2.5 | 스킬 콘텐츠 — Midguard (Tier1×3 + Tier2×2) | ✅ |
| 2.2.6 | 스킬 콘텐츠 — Rearguard (Tier1×3 + Tier2×2) | ✅ |
| 2.2.7 | 패링 스킬 SO (Skill_Parry) | ✅ |
| 2.2.8 | 회피 스킬 SO (Skill_Dodge) | ✅ |
| 2.2.9 | 스킬 효과 타입 (SkillData.effectType — Damage/AoE/Buff/Debuff/Heal/Knockback) | ⬜ |
| 2.2.10 | AoE 범위 피해 적용 (ApplySkillEffect — 범위 내 타겟 순회) | ⬜ |
| 2.2.11 | 상태이상 스킬 적용 (Debuff 분기 — UnitStatusHandler 연결) | ⬜ |
| 2.2.12 | 힐 스킬 실제 HP 회복 구현 | ⬜ |

### 2.3 상태이상 시스템

| ID | 산출물 | 상태 |
|----|--------|------|
| 2.3.1 | 상태이상 핸들러 (UnitStatusHandler — 6종 스택/갱신 혼합) | ✅ |
| 2.3.2 | 상태이상 데이터 SO (기절/출혈/중독/약화/화상) | ✅ |
| 2.3.3 | 상태이상 비주얼 (UnitStatusView + PartyMemberHUD 패널) | ✅ |

### 2.4 장비 시스템

| ID | 산출물 | 상태 |
|----|--------|------|
| 2.4.1 | 장비 데이터 SO (EquipmentData — 6종) | ✅ |
| 2.4.2 | 인벤토리 컴포넌트 (InventoryComponent + InventoryUI) | ✅ |

---

## 3.0 적 AI 시스템

### 3.1 개체 AI

| ID | 산출물 | 상태 |
|----|--------|------|
| 3.1.1 | AI 유한 상태머신 (EnemyAI FSM — Idle/Chase/Attack/Retreat) | ✅ |
| 3.1.2 | 아케타입 시스템 (EnemyArchetype — Soldier/Archer + attackRange) | ✅ |
| 3.1.3 | 스킬 선택 알고리즘 (SelectBestSkill — SkillUsage/AoE/힐 우선순위) | ✅ |
| 3.1.4 | 사거리 유지 이동 (ChaseKeepDistance — IsInBounds 경계 체크) | ✅ |

### 3.2 집단 AI

| ID | 산출물 | 상태 |
|----|--------|------|
| 3.2.1 | 그룹 코디네이터 (EnemyGroupCoordinator — 포커스 파이어/힐러 후방/산개/협공) | ✅ |
| 3.2.2 | 보스 컨트롤러 (BossController — 페이즈 전환) | ✅ |
| 3.2.3 | 보스 페이즈 전환 패턴 구현 (HP 50% 이하 Phase 2 전환 로직) | ⬜ |
| 3.2.4 | 보스 전용 스킬 SO 3종 (강타/광역/특수) | ⬜ |

---

## 4.0 스테이지 & 월드

### 4.1 스테이지 시스템

| ID | 산출물 | 상태 |
|----|--------|------|
| 4.1.1 | 스테이지 구성 SO (StageConfig — waves/WaveConfig/SpawnEntry) | ✅ |
| 4.1.2 | 웨이브 런너 (WaveRunner — WaveTrigger/WaveRunnerClearCondition) | ✅ |
| 4.1.3 | 승패 조건 7종 (IWinCondition/ILoseCondition — _hadEnemies 플래그) | ✅ |
| 4.1.4 | 스테이지 러너 (StageRunner — 스폰 + 승패 폴링) | ✅ |
| 4.1.5 | 스테이지 에셋 (Ch1_M1_Patrol / M2_Ambush / M3_Investigate) | ✅ |

### 4.2 맵 & 지형

| ID | 산출물 | 상태 |
|----|--------|------|
| 4.2.1 | Tutorial 씬 맵 (10×8 잔디+돌 테두리 + 장식물) | ✅ |
| 4.2.2 | Battle 씬 맵 (10×8 잔디+돌 테두리 + 장식물) | ✅ |
| 4.2.3 | MainMenu 배경 맵 (4-layer Tilemap + Perlin 바이옴 + 구조물 200개+) | ✅ |
| 4.2.4 | 거점 방어 컨트롤러 (DefendPointController) | ✅ |

### 4.3 챕터 구성

| ID | 산출물 | 상태 |
|----|--------|------|
| 4.3.1 | 챕터 데이터 SO (ChapterData_Ch1) | ✅ |
| 4.3.2 | 난이도 스케일러 (DifficultyScaler — 안전 구역 스폰) | ✅ |
| 4.3.3 | 드롭 테이블 (LootManager + DropTable_Ch1) | ✅ |
| 4.3.4 | 챕터 진행 데이터 (ChapterProgressData) | ✅ |
| 4.3.5 | 챕터 1 스테이지 밸런싱 (M1/M2/M3 적 구성 + 1 Run 완주 검증) | ⬜ |
| 4.3.6 | 보스 스테이지 SO (Stage_Ch1_Boss — 페이즈 2 전환 포함) | ⬜ |
| 4.3.7 | 미션 목표 텍스트 한글화 (MissionConfig 설명 1~3) | ⬜ |
| 4.3.8 | 챕터 완주 루프 (M1→M2→M3→보스→엔딩 씬 흐름 연결) | ⬜ |

---

## 5.0 진행 & 저장 시스템

### 5.1 저장/로드

| ID | 산출물 | 상태 |
|----|--------|------|
| 5.1.1 | 세이브 데이터 구조 (SaveData — 3슬롯) | ✅ |
| 5.1.2 | 저장 서비스 (SaveLoadService — Newtonsoft JSON) | ✅ |
| 5.1.3 | HP 복원 세터 (UnitStats.SetCurrentHP) | ✅ |
| 5.1.4 | 씬 전환 HP 동기화 (GameManager.OnBattleWonCore) | ✅ |

### 5.2 게임 진행

| ID | 산출물 | 상태 |
|----|--------|------|
| 5.2.1 | 게임 매니저 (GameManager — 씬 전환 / 챕터 진행 / NewGame) | ✅ |
| 5.2.2 | 씬 전환 페이더 (ScreenFader + FadeAndLoad + EventBus.Clear) | ✅ |
| 5.2.3 | 초기 파티 구성 (InitDefaultParty — startingGold 포함) | ✅ |
| 5.2.4 | 소프트락 방지 (CheckChapterFailed) | ✅ |

### 5.3 경제 시스템

| ID | 산출물 | 상태 |
|----|--------|------|
| 5.3.1 | 상점 데이터 SO (ShopData_Ch1) | ✅ |
| 5.3.2 | 상점 화면 (ShopScreen) | ✅ |
| 5.3.3 | 골드 표시 (ChapterHubScreen.txtGold + RefreshHeader) | ✅ |

### 5.4 스킬 트리 진행

| ID | 산출물 | 상태 |
|----|--------|------|
| 5.4.1 | 언락 저장 구조 (SerializedPartyMember — unlockedSkillIds / skillPoints) | ✅ |
| 5.4.2 | 저장 복원 (SkillTreeComponent.RestoreFromSave) | ✅ |

---

## 6.0 비주얼 & 오디오

### 6.1 스프라이트 애니메이션

| ID | 산출물 | 상태 |
|----|--------|------|
| 6.1.1 | 틱 기반 스프라이트 샘플러 (TickSpriteAnimator — SampleAnimation 직접 호출) | ✅ |
| 6.1.2 | 캐릭터 뷰 컨트롤러 (SpriteCharacterView — SetFacing / PlayAnimation / DeathFade) | ✅ |
| 6.1.3 | Olberic 스프라이트 에셋 + Animator (6종 클립, 투명 프레임 제거) | ✅ |
| 6.1.4 | Tressa 스프라이트 에셋 + Animator (6종 클립) | ✅ |
| 6.1.5 | Therion 스프라이트 에셋 + Animator (6종 클립) | ✅ |
| 6.1.6 | Standby 애니메이션 (Olberic/Therion — 패링 대기 자세) | ✅ |
| 6.1.7 | Support 애니메이션 (3캐릭터 magic_standby — 치료 스킬 자세) | ✅ |

### 6.2 스킬 장판 시각화

| ID | 산출물 | 상태 |
|----|--------|------|
| 6.2.1 | 장판 컴포넌트 (SkillIndicator — Circle/Rect/Cone, fill 보간) | ✅ |
| 6.2.2 | 장판 스프라이트 4종 (SmoothStep 안티앨리어싱, 256×256) | ✅ |
| 6.2.3 | 패링 타이머 시각화 (ShowParryTimer — 금색 원) | ✅ |

### 6.3 VFX 시스템

| ID | 산출물 | 상태 |
|----|--------|------|
| 6.3.1 | VFX 매니저 (VFXManager — 파티클 풀) | ✅ |
| 6.3.2 | VFX 파티클 프리팹 5종 | ✅ |
| 6.3.3 | 환경 연출 (EnvironmentManager — Rain/Fog/Fire) | ✅ |

### 6.4 피드백 비주얼

| ID | 산출물 | 상태 |
|----|--------|------|
| 6.4.1 | 데미지 팝업 (DamagePopupManager — 오브젝트 풀) | ✅ |
| 6.4.2 | 임팩트 텍스트 팝업 ("패링!" / "회피!" — ShowText) | ✅ |
| 6.4.3 | 선택 링 (SelectionRing) | ✅ |
| 6.4.4 | 타겟 인디케이터 (TargetIndicator) | ✅ |
| 6.4.5 | 적 HP 바 (EnemyHPBar — WorldSpace Canvas) | ✅ |
| 6.4.6 | 보스 HP 바 (EnemyHPBar 보스 전용 색상 / 대형 사이즈) | ⬜ |

### 6.5 오디오 시스템

| ID | 산출물 | 상태 |
|----|--------|------|
| 6.5.1 | 오디오 매니저 (AudioManager — BGM 크로스페이드 + SFX 풀 + sceneLoaded 재구독) | ✅ |
| 6.5.2 | 오디오 설정 (AudioConfig — 19종 클립 매핑) | ✅ |

---

## 7.0 UI 시스템

### 7.1 공통 디자인 시스템 (OT2 스타일)

| ID | 산출물 | 상태 |
|----|--------|------|
| 7.1.1 | 색상 토큰 (UIColors.cs — 테마A/B/C + HUD + 스킬 패널 + 팝업) | ✅ |
| 7.1.2 | UI 빌더 유틸 (UIBuilderUtils — MkPopup/MkBar/MkCornerDecor/MkSectionLabel) | ✅ |
| 7.1.3 | 툴팁 시스템 (TooltipSystem + ITooltipProvider) | ✅ |
| 7.1.4 | 커서 매니저 (CursorManager — 컨텍스트 커서) | ✅ |
| 7.1.5 | 한글 폰트 (NanumGothic TMP Dynamic Asset) | ✅ |

### 7.2 전투 HUD

| ID | 산출물 | 상태 |
|----|--------|------|
| 7.2.1 | 스킬 패널 (SkillPanel — QWER/A 단축키, 높이 84px, 앵커 우측) | ✅ |
| 7.2.2 | 스킬 버튼 (SkillButton.Build — border/아이콘/단축키/스킬명/AP비용) | ✅ |
| 7.2.3 | 파티 HUD (BattleUIBuilder — HP/AP 바 + 이름 3슬롯, 테마A/B/C) | ✅ |
| 7.2.4 | 전투 타이머 (BattleSimTimer — MM:SS.cc, 일시정지 표시) | ✅ |
| 7.2.5 | 전투 일시정지 메뉴 (BattlePauseMenu — ESC 감지, StopFlow/StartFlow) | ✅ |

### 7.3 챕터 허브 UI

| ID | 산출물 | 상태 |
|----|--------|------|
| 7.3.1 | 챕터 허브 화면 (ChapterHubScreen — 출격/골드/성장 버튼) | ✅ |
| 7.3.2 | 월드맵 뷰 (WorldMapView — uvRect 줌/팬 + 비콘 링 펄스) | ✅ |
| 7.3.3 | 임무 슬롯 UI (MissionSlotUI — 호버 이벤트 + 3D 핀 마커 + L자 코너 장식) | ✅ |
| 7.3.4 | 스킬 트리 패널 (SkillTreePanel — 캐릭터 탭 3개 + Tier 세로 배치 + 연결선) | ✅ |
| 7.3.5 | 허브 ESC 메뉴 (HubEscMenu) | ✅ |

### 7.4 결과 & 설정 화면

| ID | 산출물 | 상태 |
|----|--------|------|
| 7.4.1 | 전투 결과 화면 (BattleResultScreen — BuildUI 자동 생성, L자 코너 장식) | ✅ |
| 7.4.2 | 엔딩 결과 화면 (EndingResultScreen) | ✅ |
| 7.4.3 | 저장 슬롯 패널 (SaveSlotPanel) | ✅ |
| 7.4.4 | 설정 패널 (SettingsPanel) | ✅ |

---

## 8.0 씬 & 게임 흐름

### 8.1 씬 구성

| ID | 산출물 | 상태 |
|----|--------|------|
| 8.1.1 | MainMenu 씬 (배경 맵 Tilemap + Perlin 드리프트 카메라 + 하단 버튼 바) | ✅ |
| 8.1.2 | Tutorial 씬 (10×8 맵 + TutorialManager 연결) | ✅ |
| 8.1.3 | Battle 씬 (10×8 맵 + HUD + StageRunner + BattlePauseMenu) | ✅ |
| 8.1.4 | ChapterHub 씬 (월드맵 UI + HubEscMenu) | ✅ |
| 8.1.5 | Replay 씬 (유닛 고스트 보간 재생) | ✅ |
| 8.1.6 | Ending 씬 (EndingResultScreen) | ✅ |

### 8.2 씬 흐름 제어

| ID | 산출물 | 상태 |
|----|--------|------|
| 8.2.1 | 씬 전환 & 챕터 진행 (GameManager.FadeAndLoad + LoadBattle + LoadMainMenu) | ✅ |
| 8.2.2 | 소프트락 방지 (ChapterHubController.CheckChapterFailed) | ✅ |
| 8.2.3 | 새 게임 분기 (tutorialDone 플래그) | ✅ |

### 8.3 튜토리얼 시스템

| ID | 산출물 | 상태 |
|----|--------|------|
| 8.3.1 | 튜토리얼 매니저 (TutorialManager — 4단계 시퀀서) | ✅ |
| 8.3.2 | 튜토리얼 오버레이 (TutorialOverlay — 스포트라이트 + 말풍선) | ✅ |
| 8.3.3 | KillEnemy 스텝 (Step_KillEnemy SO + GameManager.NewGame 연결) | ✅ |

### 8.4 리플레이 시스템

| ID | 산출물 | 상태 |
|----|--------|------|
| 8.4.1 | 전투 레코더 (BattleRecorder — EventBus 구독 + 스냅샷) | ✅ |
| 8.4.2 | 리플레이 플레이어 (ReplayPlayer — 유닛 고스트 보간) | ✅ |
| 8.4.3 | 씬 간 데이터 전달 (ReplayDataBridge — DontDestroyOnLoad) | ✅ |

---

## 9.0 코어 인프라

### 9.1 이벤트 시스템

| ID | 산출물 | 상태 |
|----|--------|------|
| 9.1.1 | 이벤트 버스 (EventBus — 풀 기반 스냅샷, 재진입 안전) | ✅ |
| 9.1.2 | 게임 이벤트 정의 (GameEvents — OnUnitDied / OnTimeFlowChanged 등) | ✅ |
| 9.1.3 | 씬 전환 리스너 정리 (FadeAndLoad → EventBus.Clear → sceneLoaded 재구독) | ✅ |

### 9.2 데이터 레이어

| ID | 산출물 | 상태 |
|----|--------|------|
| 9.2.1 | ScriptableObject 레지스트리 (GameAssets 싱글턴) | ✅ |
| 9.2.2 | 스탯 수정자 파이프라인 (StatModifier — 합산/곱산/오버라이드) | ✅ |
| 9.2.3 | 밸런스 설정 (BalanceConfig — startingGold / xpPerLevel) | ✅ |

### 9.3 성능 최적화

| ID | 산출물 | 상태 |
|----|--------|------|
| 9.3.1 | 오브젝트 풀 (Queue<T> — DamagePopup / VFX / EventBus 스냅샷) | ✅ |
| 9.3.2 | 이니셔티브 큐 캐시 (_dirty 플래그 — 순서 변화 시에만 재정렬) | ✅ |
| 9.3.3 | 스폰 리소스 캐시 (StageRunner.SpawnEnemy — Resources.Load Dictionary) | ✅ |

### 9.4 렌더링 인프라

| ID | 산출물 | 상태 |
|----|--------|------|
| 9.4.1 | 소팅 레이어 계층 (Layer 1 단일 레이어 order 구간 — ADR-0014) | ✅ |
| 9.4.2 | 이소메트릭 Y 정렬 (IsometricYSort — sortingOrder 오프셋 1000) | ✅ |
| 9.4.3 | 파티원 프리팹 (PartyMember_Prefab — 10개 컴포넌트 구성) | ✅ |

---

## 10.0 품질 보증

### 10.1 단위 테스트

| ID | 산출물 | 상태 |
|----|--------|------|
| 10.1.1 | CombatCalculator 피해 계산 검증 | ✅ |
| 10.1.2 | PositioningCalculator 배후/측면 보너스 검증 | ✅ |
| 10.1.3 | InitiativeQueue 순서 정렬 검증 | ✅ |
| 10.1.4 | SaveLoadService JSON 직렬화/역직렬화 검증 | ✅ |

### 10.2 통합 테스트

| ID | 산출물 | 상태 |
|----|--------|------|
| 10.2.1 | 전투 시나리오 (파티 1명 vs 적 1명 → 사망 → OnUnitDied → LootManager) | ✅ |
| 10.2.2 | RTwP 정지 테스트 (IsBusy=false → IsPaused=true → 명령 → IsBusy=true → 재개) | ✅ |
| 10.2.3 | 씬 전환 테스트 (Battle → ChapterHub → 저장 데이터 유지) | ✅ |

### 10.3 빌드 검증

| ID | 산출물 | 상태 |
|----|--------|------|
| 10.3.1 | 씬 플로우 테스트 결과 | ✅ |
| 10.3.2 | Windows Standalone 빌드 (.exe) | ✅ |

### 10.4 설계 문서

| ID | 산출물 | 상태 |
|----|--------|------|
| 10.4.1 | ADR 17개 (모든 중요 설계 결정 사전 문서화) | ✅ |
| 10.4.2 | WBS 갱신 체계 (작업 완료 시 자동 업데이트) | ✅ |
| 10.4.3 | 주간 보고서 (docs/weekly/ — 주차별 진행 기록) | ✅ |
| 10.4.4 | 스테이지 제작 가이드 (docs/guides/stage-creation-guide.md) | ✅ |
| 10.4.5 | UI 디자인 가이드 (docs/guides/ui-design-guide.md) | ✅ |

---

## 위험 관리

| # | 위험 | 발생 여부 | 대응 |
|---|------|----------|------|
| R-1 | Inspector 직렬화 누락 — 빌드 null 참조 | ✅ 발생 | Awake() GetComponent fallback |
| R-2 | EventBus.Clear() — DontDestroyOnLoad 이벤트 단절 | ✅ 발생 | sceneLoaded 재구독 패턴 (ADR-0011) |
| R-3 | 적 스폰 위치 오류 — 카메라 밖/아군 구역 | ✅ 발생 | 맵 상단 절반 클램핑 |
| R-4 | IsPaused 상태 클리어 조건 미체크 | ✅ 발생 | Update() 폴링 독립 (ADR-0008) |
| R-5 | 투명 스프라이트 — 루프마다 깜박임 | ✅ 발생 | 픽셀 투명도 검사 + 프레임 제외 |
| R-6 | 마이그레이션 공수 과소 추정 | ✅ 발생 | ADR 선작성 + Phase 분리 (ADR-0010) |
