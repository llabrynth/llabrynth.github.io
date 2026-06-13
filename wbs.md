---
layout: default
title: RTwP RPG — WBS
permalink: /wbs/
---

# RTwP RPG — WBS (Work Breakdown Structure)
<!-- 이 파일은 CLAUDE.md 지침에 따라 작업 완료 시 자동 갱신됩니다 -->
> 최종 업데이트: 2026-06-14 (스킬 애니메이션 개선 + 스프라이트 피벗 보정)

범례: ✅ 완료 | ⬜ 진행 예정

---

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| **1** | **Stage 0: 프로젝트 기반** | ✅ | 04-05 |
| 1.1 | RTwP 시간 제어 시스템 | ✅ | 04-05 |
| 1.1.1 | TimeFlowManager | ✅ | 04-05 |
| 1.1.2 | InitiativeQueue | ✅ | 04-05 |
| 1.2 | 기본 전투 구조 | ✅ | 04-05 |
| 1.2.1 | 파티 & 적 시스템 골격 | ✅ | 04-05 |
| 1.2.2 | 스테이지 / 웨이브 구조 | ✅ | 04-05 |
| **2** | **Stage 1: 전투 기반** | ✅ | 04-09 |
| 2.1 | 데이터 아키텍처 | ✅ | 04-09 |
| 2.1.1 | StatModifier 파이프라인 | ✅ | 04-09 |
| 2.1.2 | SkillData ScriptableObject | ✅ | 04-09 |
| 2.1.3 | EquipmentData ScriptableObject | ✅ | 04-09 |
| 2.2 | 전투 판정 시스템 | ✅ | 04-09 |
| 2.2.1 | PositioningCalculator (배후/측면 보너스) | ✅ | 04-09 |
| 2.2.2 | CombatCalculator (커버 방어 보정) | ✅ | 04-09 |
| 2.3 | 상태이상 시스템 | ✅ | 04-09 |
| 2.3.1 | UnitStatusHandler (6종 스택/갱신 혼합) | ✅ | 04-09 |
| 2.4 | 적 AI 시스템 | ✅ | 04-09 |
| 2.4.1 | EnemyAI FSM (Idle/Chase/Attack/Retreat) | ✅ | 04-09 |
| 2.5 | 비주얼 피드백 | ✅ | 04-09 |
| 2.5.1 | SpriteCharacterView 애니메이션 컨트롤러 | ✅ | 04-09 |
| 2.5.2 | DamagePopupManager | ✅ | 04-09 |
| **3** | **Stage 2: 캐릭터 심화** | ✅ | 04-11 |
| 3.1 | 캐릭터 성장 시스템 | ✅ | 04-11 |
| 3.1.1 | ClassData & 전직 시스템 | ✅ | 04-11 |
| 3.1.2 | SkillTreeComponent | ✅ | 04-11 |
| 3.1.3 | InventoryComponent | ✅ | 04-11 |
| 3.2 | 전투 심화 메커니즘 | ✅ | 04-11 |
| 3.2.1 | APRecoveryHandler | ✅ | 04-11 |
| 3.2.2 | Dodge / Parry 판정 | ✅ | 04-11 |
| 3.3 | 전투 전 UI | ✅ | 04-11 |
| 3.3.1 | PreBattleScreen | ✅ | 04-11 |
| 3.3.2 | SkillDeckUI (A/B 토글) | ✅ | 04-11 |
| 3.3.3 | InventoryUI | ✅ | 04-11 |
| **4** | **Stage 3: 월드 & 콘텐츠 확장** | ✅ | 04-12 |
| 4.1 | 지형 시스템 | ✅ | 04-12 |
| 4.1.1 | TerrainTileData & GridManager | ✅ | 04-12 |
| 4.1.2 | AStarPathfinder (이동 비용 + Obstacle) | ✅ | 04-12 |
| 4.2 | 보스 & 적 AI 확장 | ✅ | 04-12 |
| 4.2.1 | BossController (페이즈 전환) | ✅ | 04-12 |
| 4.2.2 | EnemyAI Archetype (MeleeRush/Sniper/AoE/Healer) | ✅ | 04-12 |
| 4.3 | 거점 방어 시스템 | ✅ | 04-12 |
| 4.3.1 | DefendPointController | ✅ | 04-12 |
| 4.3.2 | 승패 조건 7종 | ✅ | 04-12 |
| 4.4 | 허브 & 진행 시스템 | ✅ | 04-12 |
| 4.4.1 | LootManager & DropTable | ✅ | 04-12 |
| 4.4.2 | DifficultyScaler & ChapterProgressData | ✅ | 04-12 |
| 4.4.3 | ChapterHubScreen | ✅ | 04-12 |
| **5** | **Stage 4: 스토리 & 진행 시스템** | ✅ | 04-16 |
| 5.1 | 데이터 저장 시스템 | ✅ | 04-16 |
| 5.1.1 | SaveData & SaveLoadService | ✅ | 04-16 |
| 5.1.2 | GameManager (씬 전환 & 챕터 진행) | ✅ | 04-16 |
| 5.2 | 스토리 시스템 | ✅ | 04-16 |
| 5.2.1 | DialogueData & DialoguePlayer | ✅ | 04-16 |
| 5.2.2 | ChapterData & MissionConfig SO | ✅ | 04-16 |
| 5.3 | 경제 시스템 | ✅ | 04-16 |
| 5.3.1 | ShopData & ShopScreen | ✅ | 04-16 |
| 5.4 | 결과 & 설정 UI | ✅ | 04-16 |
| 5.4.1 | BattleResultScreen | ✅ | 04-16 |
| 5.4.2 | EndingResultScreen | ✅ | 04-16 |
| 5.4.3 | SaveSlotPanel & SettingsPanel | ✅ | 04-16 |
| **6** | **Stage 5: 폴리싱** | ✅ | 05-16 |
| 6.1 | UI/UX 품질 시스템 | ✅ | 04-24 |
| 6.1.1 | TooltipSystem & ITooltipProvider | ✅ | 04-24 |
| 6.1.2 | ScreenFader (씬 전환 페이드) | ✅ | 04-24 |
| 6.1.3 | CursorManager (컨텍스트 커서) | ✅ | 04-24 |
| 6.2 | 사운드 시스템 | ✅ | 04-25 |
| 6.2.1 | AudioManager (BGM 크로스페이드 + SFX 풀) | ✅ | 04-25 |
| 6.2.2 | AudioConfig 에셋 (19종 클립 매핑) | ✅ | 04-25 |
| 6.3 | VFX 시스템 | ✅ | 04-25 |
| 6.3.1 | VFXManager (파티클 풀) | ✅ | 04-25 |
| 6.3.2 | VFX 파티클 프리팹 5종 | ✅ | 04-25 |
| 6.4 | 상태이상 비주얼 | ✅ | 04-25 |
| 6.4.1 | UnitStatusView | ✅ | 04-25 |
| 6.4.2 | PartyMemberHUD 상태이상 패널 | ✅ | 04-25 |
| 6.5 | 환경 연출 시스템 | ✅ | 04-25 |
| 6.5.1 | EnvironmentManager (Rain/Fog/Fire) | ✅ | 04-25 |
| 6.6 | 튜토리얼 시스템 | ✅ | 05-14 |
| 6.6.1 | TutorialManager (4단계 시퀀서) | ✅ | 04-29 |
| 6.6.2 | TutorialOverlay (스포트라이트 + 말풍선) | ✅ | 04-29 |
| 6.6.3 | Tutorial.unity 씬 | ✅ | 05-14 |
| 6.7 | 리플레이 시스템 | ✅ | 05-14 |
| 6.7.1 | BattleRecorder & ReplayPlayer | ✅ | 05-14 |
| 6.7.2 | Replay.unity 씬 | ✅ | 05-14 |
| 6.8 | 한글 폰트 & 성능 | ✅ | 05-15 |
| 6.8.1 | NanumGothic TMP Dynamic Asset | ✅ | 05-15 |
| 6.8.2 | DamagePopupManager 오브젝트 풀 | ✅ | 05-15 |
| 6.9 | 전투 UI | ✅ | 05-16 |
| 6.9.1 | SkillPanel (이동/대기/스킬 버튼) | ✅ | 05-16 |
| 6.9.2 | SelectionRing | ✅ | 05-16 |
| 6.9.3 | TargetIndicator | ✅ | 05-16 |
| **7** | **마무리: 코드 수정 & 빌드 검증** | ✅ | 05-22 |
| 7.1 | 코드 품질 버그 패치 (20건, H-1~H-20) | ✅ | 05-20 |
| 7.2 | 고정 틱 시뮬레이션 마이그레이션 | ✅ | 05-20 |
| 7.2.1 | 기반 파일 (ActionPhase / UnitSimState / CommandQueue / BattleSimulation) | ✅ | 05-20 |
| 7.2.2 | UnitController 확장 + UnitCombatAction 상태머신 | ✅ | 05-20 |
| 7.2.3 | 의존 시스템 Tick 전환 + TimeFlowManager Facade + BattleRecorder | ✅ | 05-20 |
| 7.2.4 | 전투 씬 회귀 테스트 결과 | ✅ | 05-22 |
| 7.3 | 최종 검증 산출물 | ✅ | 05-22 |
| 7.3.1 | 씬 플로우 테스트 결과 | ✅ | 05-22 |
| 7.3.2 | Windows Standalone 빌드 | ✅ | 05-22 |
| 7.4 | 고심각도 버그 패치 (H-5~H-11) | ✅ | 05-22 |
| 7.4.1 | StageRunner SpawnEnemy EnemyAI 중복 AddComponent 방지 (H-5) | ✅ | 05-22 |
| 7.4.2 | BattleSimulation accumulator unscaledDeltaTime 전환 (H-6) | ✅ | 05-22 |
| 7.4.3 | Sustained 스킬 PendingTimeCost 불일치 패치 (H-7) | ✅ | 05-22 |
| 7.4.4 | TryExecutePendingSkill 실패 시 _pendingSkill 유지 + RefreshButtons 갱신 (H-9, H-10) | ✅ | 05-22 |
| 7.4.5 | CommandQueue 이중 소비 제거 — Update 단일 경로 통합 (H-11) | ✅ | 05-22 |
| 7.5 | 중간 심각도 버그 패치 (12건, M-1~M-12) | ✅ | 05-22 |
| 7.6 | 낮은 심각도 버그 패치 (7건, L-A2/A4/B1/B4/C1~C4) | ✅ | 05-22 |
| 7.7 | 타겟팅·색상 버그 근본 패치 | ✅ | 05-27 |
| 7.7.1 | BattleInputHandler 스킬/이동 발행 후 Deselect 제거 → 적 재타겟팅 가능 | ✅ | 05-27 |
| 7.7.2 | UnitCombatAction.IsBusy — CommandQueue HasCommandFor 포함 | ✅ | 05-27 |
| 7.7.3 | UnitCombatAction.StartAction 진입 시 SetHighlight(true) | ✅ | 05-27 |
| 7.7.4 | PartyManager.SelectUnit IsBusy 체크 — 행동 중 노랑 덮어쓰기 방지 | ✅ | 05-27 |
| 7.7.5 | SkillPanel.RefreshButtons 이동/대기 버튼 interactable 갱신 | ✅ | 05-27 |
| 7.8 | KillEnemy 튜토리얼 스텝 | ✅ | 05-27 |
| 7.8.1 | EnemyHPBar WorldSpace Canvas 컴포넌트 | ✅ | 05-27 |
| 7.8.2 | TutorialManager KillEnemy 스텝 + ChapterHub 이동 | ✅ | 05-27 |
| 7.8.3 | GameManager.NewGame() tutorialDone 분기 | ✅ | 05-27 |
| 7.8.4 | Step_KillEnemy SO + Enemy_Basic HPBarCanvas 프리팹 + Tutorial 씬 연결 | ✅ | 05-27 |
| 7.9 | 튜토리얼 플레이어빌리티 패치 | ✅ | 05-29 |
| 7.9.1 | Char_TutorialEnemy maxHP 50→200 (원샷 방지) | ✅ | 05-29 |
| 7.9.2 | SpriteCharacterView OnUnitDied 구독 — 사망 시 회색+페이드 | ✅ | 05-29 |
| 7.9.3 | EnemyHPBar fillAmount→anchorMax.x 방식 전환 | ✅ | 05-29 |
| 7.9.4 | Enemy_Basic HPBarCanvas sizeDelta (80,8)→(200,16) | ✅ | 05-29 |
| 7.9.5 | TutorialManager GameManager null 시 SceneManager fallback | ✅ | 05-29 |
| 7.9.6 | ChapterHubController — 씬 전환 시 ChapterHubScreen.Open() 자동 호출 | ✅ | 05-29 |
| **8.0** | **콘텐츠: 맵·허브 UI** | ✅ | 05-30 |
| 8.0.1 | Tutorial 씬 맵 — 10×8 잔디+돌 테두리, 나무·덤불 장식 | ✅ | 05-30 |
| 8.0.2 | ChapterHub UI — 헤더·임무목록·상세패널·출격버튼 + MissionSlot 프리팹 | ✅ | 05-30 |
| 8.0.3 | Battle 씬 맵 — 10×8 잔디+돌 테두리, 나무·덤불 장식 | ✅ | 05-30 |
| **8.1** | **GameManager·PartyManager 연동** | ✅ | 05-30 |
| 8.1.1 | GameManager.InitDefaultParty() — 새 게임 시 partyMembers 초기화 | ✅ | 05-30 |
| 8.1.2 | GameManager.FindCharacter(id) — GameAssets 캐릭터 검색 공개 접근자 | ✅ | 05-30 |
| 8.1.3 | PartyManager.SpawnParty() SaveData 기반 스폰 + Inspector fallback | ✅ | 05-30 |
| 8.1.4 | UnitStats.SetCurrentHP(int) — 저장된 HP 복원 세터 | ✅ | 05-30 |
| **8.2** | **콘텐츠 연결 작업** | ✅ | 05-30 |
| 8.2.1 | GameAssets.allCharacters 스킬 연결 (Vanguard/Midguard/Rearguard) | ✅ | 05-30 |
| 8.2.2 | Ending 씬 UI | ✅ | 05-30 |
| 8.2.3 | 캐릭터 스프라이트/애니메이터 연결 (Unit_Animator + TX Player portrait) | ✅ | 05-30 |
| 8.2.4 | 장비 6종 SO + DropTable Ch1 연결 + GameAssets 등록 | ✅ | 05-30 |
| 8.2.5 | ShopScreen + SaveSlotPanel UI + ShopData_Ch1 에셋 | ✅ | 05-30 |
| **9.0** | **엔드-투-엔드 플레이어빌리티 패치 1차** | ✅ | 05-30 |
| 9.0.1 | StageRunner LootManager 적 사망 훅 — 골드·장비 드롭 활성화 | ✅ | 05-30 |
| 9.0.2 | GameManager.OnBattleWon 파티 HP 저장 — 씬 전환 후 HP 유지 | ✅ | 05-30 |
| 9.0.3 | BalanceConfig.startingGold + InitDefaultParty 초기 골드 | ✅ | 05-30 |
| 9.0.4 | ChapterHubController.CheckChapterFailed — 소프트락 방지 | ✅ | 05-30 |
| 9.0.5 | ChapterHubScreen txtGold UI — 골드 표시 | ✅ | 05-30 |
| 9.0.6 | BattleResultScreen UI 재구성 — 전투 결과 화면 | ✅ | 05-30 |
| **10.0** | **코드 리뷰 반영 패치** | ✅ | 05-31 |
| 10.0.1 | EventBus._snapshot 풀 기반 재진입 안전 구조 | ✅ | 05-31 |
| 10.0.2 | BattleManager.cs 삭제 + Stage_01 씬 정리 | ✅ | 05-31 |
| 10.0.3 | GameManager.FadeAndLoad EventBus.Clear — 씬 전환 리스너 정리 | ✅ | 05-31 |
| 10.0.4 | SaveLoadService 세이브 파일 삭제 전 LogError | ✅ | 05-31 |
| 10.0.5 | GameManager.NewGame clueGaugePerChapter 동적 결정 | ✅ | 05-31 |
| 10.0.6 | BattleResultScreen 주석 정정 | ✅ | 05-31 |
| 10.0.7 | StageRunner.SpawnEnemy Resources.Load Dictionary 캐시 | ✅ | 05-31 |
| 10.0.8 | TimeFlowManager.ActiveActionCount 제거 + TimeFlowHUD 정리 | ✅ | 05-31 |
| **11.0** | **허브-전투 씬 연동 구조** | ✅ | 05-31 |
| 11.0.1 | StageRunner.OnMissionSelectedFromHub GameManager.GetCurrentChapter() 우선 사용 | ✅ | 05-31 |
| 11.0.2 | DifficultyScaler.GenerateSpawns chapter null 방어 | ✅ | 05-31 |
| 11.0.3 | StageRunner.OnMissionSelectedFromHub EliminateAll + PartyWipe 승패 조건 | ✅ | 05-31 |
| 11.0.4 | Battle.unity PartyManager.partyMemberPrefab 연결 | ✅ | 05-31 |
| 11.0.5 | Battle.unity StageRunner.chapterData 연결 (ChapterData_Ch1) | ✅ | 05-31 |
| **12.0** | **StageConfig 웨이브 스테이지 시스템** | ✅ | 05-31 |
| 12.0.1 | StageConfig SO (stageId/waves/WaveConfig/SpawnEntry/WinConditionType/WaveTrigger) | ✅ | 05-31 |
| 12.0.2 | WaveRunner MonoBehaviour + WaveRunnerClearCondition | ✅ | 05-31 |
| 12.0.3 | ChapterData.stages StageConfig[] (MissionConfig[] 하위 호환 유지) | ✅ | 05-31 |
| 12.0.4 | ChapterProgressData StageConfig 오버로드 | ✅ | 05-31 |
| 12.0.5 | StageRunner PendingStage 경로 + OnStageSelectedFromHub + SpawnEntryFromStage | ✅ | 05-31 |
| 12.0.6 | GameManager PendingStage + LoadBattle(StageConfig) + OnBattleWon(StageConfig) | ✅ | 05-31 |
| 12.0.7 | ChapterHubScreen StageConfig 슬롯 표시 | ✅ | 05-31 |
| 12.0.8 | Stage_Ch1_M1_Patrol / M2_Ambush / M3_Investigate 에셋 + ChapterData 등록 | ✅ | 05-31 |
| 12.0.9 | 스테이지 제작 가이드 (docs/guides/stage-creation-guide.md) | ✅ | 05-31 |
| **13.0** | **전투 결과 화면** | ✅ | 05-31 |
| 13.0.1 | StageRunner.Update() 승패 폴링 — BattleSimulation 일시정지 무관 | ✅ | 05-31 |
| 13.0.2 | BattleResultScreen GO 비활성 유지 + ShowResult 정적 메서드 + FindObjectOfType 폴백 | ✅ | 05-31 |
| 13.0.3 | BattleResultScreen 카드 UI — txtTitle/btnReplay + 네이비 카드+골드 아웃라인 | ✅ | 05-31 |
| 13.0.4 | GameManager.OnBattleWonCore CurrentSave null 폴백 | ✅ | 05-31 |
| **14.0** | **허브 UI 리디자인** | ✅ | 05-31 |
| 14.0.1 | ChapterHub 헤더 — IbarraRealNova-SemiBold 챕터 제목, Jost-SemiBold 스탯, 아이콘 버튼 | ✅ | 05-31 |
| 14.0.2 | ChapterHub 패널 — Outline 컴포넌트, 임무목록/출격정보 라벨 스타일 | ✅ | 05-31 |
| 14.0.3 | 상점/저장 버튼 DarkBackground 아이콘 스프라이트 | ✅ | 05-31 |
| 14.0.4 | 출격 버튼 레드-오렌지 강조색 + Outline | ✅ | 05-31 |
| 14.0.5 | MissionSlot 프리팹 다크 스타일 통일 | ✅ | 05-31 |
| **15.0** | **ADR 문서화 & 아키텍처 정비** | ✅ | 05-31 |
| 15.0.1 | ADR-0006: StageConfig + WaveRunner 시스템 | ✅ | 05-31 |
| 15.0.2 | ADR-0007: ChapterHub 별도 씬 구조 | ✅ | 05-31 |
| 15.0.3 | ADR-0008: StageRunner.Update() 승패 폴링 | ✅ | 05-31 |
| 15.0.4 | ADR-0009: Modern GDR + Cainos UI 아트 방향 | ✅ | 05-31 |
| 15.0.5 | ADR-0010: 코루틴 → 20 TPS 고정 틱 시뮬레이션 전환 | ✅ | 05-31 |
| 15.0.6 | CLAUDE.md ADR 지침 강화 | ✅ | 05-31 |
| **16.0** | **플레이어빌리티 버그 패치 2차** | ✅ | 05-31 |
| 16.0.1 | StageRunner EventBus OnUnitDied → LootManager.OnEnemyDefeated 연결 | ✅ | 05-31 |
| 16.0.2 | GameManager.OnBattleWonCore 전투 후 파티 HP SaveData 동기화 | ✅ | 05-31 |
| 16.0.3 | GameManager.InitDefaultParty BalanceConfig.startingGold 초기 골드 | ✅ | 05-31 |
| 16.0.4 | ChapterHubController.Start CheckChapterFailed() — 소프트락 방지 | ✅ | 05-31 |
| 16.0.5 | ChapterHubScreen txtGold + RefreshHeader() 골드 표시 | ✅ | 05-31 |
| **17.0** | **플레이어빌리티 버그 패치 3차** | ✅ | 06-01 |
| 17.0.1 | EliminateAllEnemiesCondition _hadEnemies 플래그 패치 | ✅ | 06-01 |
| 17.0.2 | AudioManager 씬별 BGM 미매핑 StopBgm() 패치 | ✅ | 06-01 |
| 17.0.3 | AudioManager SceneManager.sceneLoaded 재구독 패치 | ✅ | 06-01 |
| 17.0.4 | ChapterHubController StopAll() 허브 진입 오디오 즉시 정지 처리 | ✅ | 06-01 |
| 17.0.5 | DifficultyScaler 적 스폰 안전 구역 — 맵 상단 절반 | ✅ | 06-01 |
| 17.0.6 | StageRunner.SpawnEntryFromStage 맵 경계 클램핑 | ✅ | 06-01 |
| 17.0.7 | IsometricYSort sortingOrder 오프셋 1000 패치 | ✅ | 06-01 |
| 17.0.8 | Stage_Ch1 아처 스폰 엔트리 삭제 | ✅ | 06-01 |
| 17.0.9 | ChapterData_Ch1 챕터명 "테스트" | ✅ | 06-01 |
| 17.0.10 | SpriteCharacterView DeathFade 후 GameObject Destroy 패치 | ✅ | 06-01 |
| **17.1** | **ADR 소급 문서화** | ✅ | 06-01 |
| 17.1.1 | ADR-0011: EventBus.Clear() DontDestroyOnLoad 싱글턴 재구독 패턴 | ✅ | 06-01 |
| 17.1.2 | ADR-0012: EliminateAllEnemiesCondition _hadEnemies 플래그 설계 | ✅ | 06-01 |
| 17.1.3 | ADR-0001 파생결정 링크 정정 | ✅ | 06-01 |

---

## 위험 관리

> 실제 개발 중 발생했거나 재발 가능한 위험 목록. 경험 기반으로 작성.

| # | 카테고리 | 위험 | 실제 발생 | 대응 |
|---|---------|------|----------|------|
| R-1 | 기술 | Inspector 직렬화 누락 — 빌드에서만 나타나는 null 참조 버그 | ✅ 발생 (SpriteCharacterView._spriteRenderer {fileID:0}, TutorialOverlay NextButton) | Awake()에서 GetComponentInChildren fallback 추가. 빌드 후 즉시 Console 확인 |
| R-2 | 기술 | EventBus.Clear() 사이드이펙트 — DontDestroyOnLoad 싱글턴 이벤트 수신 단절 | ✅ 발생 (AudioManager 씬 전환 후 BGM/SFX 무반응) | SceneManager.sceneLoaded에서 Off→On 재구독 패턴 적용 (ADR-0011) |
| R-3 | 기술 | 적 스폰 위치 오류 — 카메라 밖 또는 아군 구역 스폰 | ✅ 발생 (DifficultyScaler y=0~2 아군 구역, Stage 에셋 y=6 화면 밖) | 스폰 좌표 맵 상단 절반 클램핑. 스테이지 에셋 검수 절차 추가 |
| R-4 | 기술 | 조건 판정 타이밍 — IsPaused 상태에서 클리어 조건 미체크 | ✅ 발생 (EliminateAllEnemiesCondition Count==0 가드 버그 반복) | Update() 폴링으로 BattleSimulation과 독립 (ADR-0008). _hadEnemies 플래그 도입 (ADR-0012) |
| R-5 | 기술 | 에셋 스프라이트 슬라이싱 오류 — 투명 셀 참조로 유닛 불가시 | ✅ 발생 (Cainos banditCrossbowM2 스프라이트 95% 투명) | 신규 에셋 임포트 시 스프라이트 opaque pixel 비율 확인. 대체 표현(UnitCircle) 준비 |
| R-6 | 일정 | 특정 시스템 마이그레이션 공수 과소 추정 | ✅ 발생 (코루틴→고정 틱 전환 약 1주 소요) | 마이그레이션 전 ADR 작성 + Phase 분리 계획 필수 (ADR-0010) |

---

## 18.0 Directional 스킬 시스템 구현

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| **18** | **Directional 스킬 클라이언트 구현** | ✅ | 06-02 |
| 18.1 | SkillData targetingMode 필드 추가 (Positional/Directional enum) | ✅ | 06-01 |
| 18.2 | UnitCombatAction.TryUseSkillDirectional() 메서드 | ✅ | 06-01 |
| 18.3 | SkillPanel.TryExecutePendingSkillDirectional() 메서드 | ✅ | 06-02 |
| 18.4 | BattleInputHandler Directional 클릭 방향 입력 처리 | ✅ | 06-02 |

---

## 19.0 적 AI 고도화 + 스킬 장판 시각화

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| **19** | **적 AI 고도화 + 스킬 장판 시각화** | ✅ | 06-02 |
| 19.1 | SkillData IndicatorShape/SkillUsage enum + 필드 추가 | ✅ | 06-02 |
| 19.2 | SkillIndicator 장판 시각화 컴포넌트 (scale 0→1 보간) | ✅ | 06-02 |
| 19.3 | UnitCombatAction 장판 연동 + Directional 다중 타겟 지원 | ✅ | 06-02 |
| 19.4 | EnemyAI SelectBestSkill() — SkillUsage/AoE/힐 우선순위 선택 | ✅ | 06-02 |
| 19.5 | EnemyGroupCoordinator — 포커스 파이어/힐러 후방/산개/협공 | ✅ | 06-02 |
| 19.6 | SkillIndicator 프리팹 생성 + Battle 씬 EnemyGroupCoordinator 배치 | ✅ | 06-02 |

---

## 20.0 전투 UX 개선 — 스킬 슬롯·장판 아웃라인·파티 HUD

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| **20** | **전투 UX 개선** | ✅ | 06-03 |
| 20.1 | 스킬 슬롯 4개 제한 + QWER/A 단축키 (SkillPanel, SkillButton, BattleInputHandler) | ✅ | 06-03 |
| 20.2 | SkillIndicator 아웃라인 링/테두리 추가 — Circle/Rect/Cone 각 Outline SpriteRenderer | ✅ | 06-03 |
| 20.3 | 찌르기 스킬 Directional Rectangle — 방향 오프셋·fill 보간·선딜 0.5s 수정 | ✅ | 06-03 |
| 20.4 | EnemyAI lazy init 버그 수정 + SpawnEnemy AddComponent 순서 수정 | ✅ | 06-03 |
| 20.5 | StageRunner defaultStage — Battle 씬 직접 플레이 지원 | ✅ | 06-03 |
| 20.6 | BattleInputHandler 자동 유닛 선택 (OnUnitActed 이벤트 연동) | ✅ | 06-03 |
| 20.7 | BattleUIBuilder 파티 HP/AP HUD — 이름·수치·슬라이더 3슬롯 (Battle 씬 배치) | ✅ | 06-03 |

---

## 21.0 투사체 시스템 + 스킬 장판 개선

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| **21** | **투사체 시스템 + 스킬 장판 개선** | ✅ | 06-05 |
| 21.1 | 적 행동 시 노란색 하이라이트 제거 — IsEnemy 체크로 아군만 표시 | ✅ | 06-05 |
| 21.2 | 강타 스킬 Directional Cone 변경 — 90° 원뿔, range=2m | ✅ | 06-05 |
| 21.3 | SkillIndicator fill 틱 기반 보간 — SetProgress(t) + _preDelayTotal | ✅ | 06-05 |
| 21.4 | Projectile 클래스 — TickMove(dt) 틱 기반 투사체 이동 | ✅ | 06-05 |
| 21.5 | SkillData isProjectile + projectileSpeed 필드 | ✅ | 06-05 |
| 21.6 | 사격 스킬 (Skill_Shot) — Directional Single Rectangle, 투사체, 사거리 5m | ✅ | 06-05 |
| 21.7 | 중위 (Char_Midguard) 사격 스킬 슬롯 추가 | ✅ | 06-05 |
| 21.8 | Projectile_Arrow 프리팹 + Arrow 스프라이트 | ✅ | 06-05 |
| 21.9 | 장판 스프라이트 SmoothStep 안티앨리어싱 + Circle/Rect/Cone/Ring 256×256 재생성 | ✅ | 06-05 |
| 21.10 | Cone 스프라이트 BottomCenter pivot — 뿔 끝을 캐스터 위치에 고정 | ✅ | 06-05 |
| 21.11 | ADR-0013 투사체 틱 기반 시뮬레이션 | ✅ | 06-05 |
| 21.12 | ChapterHubScreen txtGold Inspector 연결 (B5 완료) | ✅ | 06-05 |

---

## 22.0 적 AI 전투 활성화 + RTwP 타이머 UI

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| **22** | **적 AI 전투 활성화 + RTwP 타이머 UI** | ✅ | 06-05 |
| 22.1 | Projectile 틱 보간 — _prevPos/_currentPos + Interpolate(alpha) | ✅ | 06-05 |
| 22.2 | UnitCombatAction.InterpolateProjectile — 유닛 Interpolate 체인 연결 | ✅ | 06-05 |
| 22.3 | EnemyArchetype.attackRange 필드 + SetArchetype() 런타임 적용 | ✅ | 06-05 |
| 22.4 | EnemyArchetype_Soldier — skills [Slash, HeavyBlow], attackRange=2.5 | ✅ | 06-05 |
| 22.5 | EnemyArchetype_Archer — skills [Shot], attackRange=5.0 | ✅ | 06-05 |
| 22.6 | BattleSimTimer — SimTime 틱 기반 MM:SS.cc 타이머, 일시정지 ⏸/▶ 표시 | ✅ | 06-05 |
| 22.7 | Battle.unity SimTimer GameObject — BattleHUD 상단 중앙 배치 | ✅ | 06-05 |

---

## 23.0 전투 버그 수정 — 맵 밖 스폰 / 원뿔 장판 불일치

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| **23** | **전투 버그 수정 배치** | ✅ | 06-06 |
| 23.1 | EnemyAI.ChaseKeepDistance IsInBounds 체크 — RangedSniper 맵 밖 탈출 버그 수정 | ✅ | 06-06 |
| 23.2 | SkillIndicator_ConeRing.png 재생성 — SmoothStep 엣지 안티앨리어싱 (경계 텍스처) | ✅ | 06-06 |
| 23.3 | SkillIndicator_Cone.png fill 재생성 — 잘못된 tan=1 기하학 + 원형 클립 버그 수정 | ✅ | 06-06 |
| 23.4 | UnitCombatAction OnUnitDied 구독 — 사망 시 스킬 장판 잔상 제거 | ✅ | 06-06 |
| 23.5 | 원뿔 장판 부채꼴(sector) 형태 — Fill + ConeRing 텍스처 재생성 (삼각형→원호 클립) | ✅ | 06-06 |

---

## 24.0 전투 메커니즘 — AP 회복 상향 + 패링/회피 스킬

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| **24** | **AP 회복 + 패링/회피 스킬** | ✅ | 06-06 |
| 24.1 | AP 회복 기본값 10→20/sec (ClassData, CharacterData) | ✅ | 06-06 |
| 24.2 | SkillData isInstantSelf + dodgeParryData 필드 — 자체 발동 스킬 지원 | ✅ | 06-06 |
| 24.3 | DodgeParryData apRecoveryOnDodge 필드 — 회피 성공 AP 회복량 | ✅ | 06-06 |
| 24.4 | 패링 성공 시 공격자 1타일 Knockback + "패링!" 팝업 | ✅ | 06-06 |
| 24.5 | 회피 성공 시 방어자 AP 회복 + "회피!" 팝업 | ✅ | 06-06 |
| 24.6 | DamagePopup/Manager ShowText(string) — 임팩트 텍스트 팝업 | ✅ | 06-06 |
| 24.7 | SkillPanel 자체 발동 스킬 즉시 실행 + 회피 방향 자동 결정 | ✅ | 06-06 |
| 24.8 | Skill_Parry.asset + Skill_Dodge.asset 생성 | ✅ | 06-06 |
| 24.9 | 전위/중위 → 패링 스킬, 후위 → 회피 스킬 CharacterData 등록 | ✅ | 06-06 |
| 24.10 | SkillIndicator.ShowParryTimer() — 금색 원 활성 시간 타이머 | ✅ | 06-06 |
| 24.11 | SkillPanel.IsDodgeMode — 회피 목적지 클릭 모드 (범위 원 표시 + 방향 스냅) | ✅ | 06-06 |
| 24.12 | BattleInputHandler 회피 모드 클릭 처리 + 예측선 | ✅ | 06-06 |
| 24.13 | 패링 넉백 보간 잔상 제거 + EnemyAI 즉시 재공격 방지 스태거 | ✅ | 06-06 |
| 24.14 | Sorting Layer 계층 정리 — Layer 1 단일 레이어 order 구간 확정 (ADR-0014) | ✅ | 06-06 |
| 24.15 | "패링!" 팝업 미표시 버그 수정 — DamagePopupManager 씬 미배치 + 한글 폰트 누락 | ✅ | 06-07 |
| 24.16 | 회피 유예 타이머 — DodgeGraceTimer 0.5초, 이동 완료 후 원래 자리 공격 회피 판정 | ✅ | 06-07 |
| 24.17 | 회피 IsDodgeActive 타이밍 버그 — StartDodge에서 즉시 활성화 (패링 구조 통일) | ✅ | 06-07 |
| 25.0 | 시작화면 배경 맵 — 숲+폐허 Tilemap + Perlin 드리프트 카메라 | ✅ | 06-07 |
| 25.1 | MainMenuCameraDrift.cs — Perlin noise 카메라 드리프트 스크립트 | ✅ | 06-07 |
| 25.2 | MainMenu 씬 Grid + 4-layer Tilemap 구조 세팅 | ✅ | 06-07 |
| 25.3 | Ground 레이어 잔디/돌 바이옴 Perlin noise 경계 페인팅 | ✅ | 06-07 |
| 25.4 | Transition 레이어 바이옴 경계 엣지 타일 처리 | ✅ | 06-07 |
| 25.5 | 오브젝트 배치 — 나무 클러스터·우물·성벽 잔해·제단·묘비 | ✅ | 06-07 |
| 25.6 | UI Layout C — 타이틀 상단 + 하단 반투명 버튼 바 | ✅ | 06-07 |
| 25.7 | 배경 맵 오브젝트 밀도 개선 — 숲·폐허·전환 구역 오브젝트 200개 추가 | ✅ | 06-07 |
| 25.8 | 배경 맵 벽/절벽 지형 17개 구조물 추가 — Wall/Cliff 타일 조합 | ✅ | 06-07 |

---

## 26.0 스킬 트리 UI & 성장 시스템

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| **26** | **스킬 트리 UI & 성장 시스템** | ⬜ | — |
| 26.0.0 | ADR-0015: 스킬 트리 레이아웃 & 성장 방식 결정 | ✅ | 06-09 |
| **26.A** | **Phase A — 데이터·레벨링** | ✅ | 06-11 |
| 26.A.1 | SerializedPartyMember — unlockedSkillIds[], skillPoints, activeSlotIds[], passiveSlotIds[] | ✅ | 06-11 |
| 26.A.2 | BalanceConfig — xpPerLevel 필드 추가 | ✅ | 06-11 |
| 26.A.3 | GameManager.OnBattleWon — XP 집계 + 레벨업 처리 | ✅ | 06-11 |
| 26.A.4 | SkillTreeComponent.RestoreFromSave() — 저장된 언락 목록 복원 | ✅ | 06-11 |
| **26.B** | **Phase B — UI 핵심** | ✅ | 06-11 |
| 26.B.1 | SkillTreeNode — 아이콘·잠금 오버레이·클릭 이벤트 | ✅ | 06-11 |
| 26.B.2 | SkillTreePanel — 캐릭터 탭 3개, Tier 세로 배치, 연결선, 포인트 표시 | ✅ | 06-11 |
| 26.B.3 | ChapterHubScreen "성장" 버튼 → SkillTreePanel 호출 | ✅ | 06-11 |
| 26.B.4 | ChapterHubUIBuilder — SkillTreeNode 프리팹 + SkillTreePanel GO 자동 생성 | ✅ | 06-11 |
| **26.C** | **Phase C — 콘텐츠 스킬 에셋** | ✅ | 06-11 |
| 26.C.1 | Vanguard Tier1 스킬 3개 + Tier2 스킬 2개 SO | ✅ | 06-11 |
| 26.C.2 | Midguard Tier1 스킬 3개 + Tier2 스킬 2개 SO | ✅ | 06-11 |
| 26.C.3 | Rearguard Tier1 스킬 3개 + Tier2 스킬 2개 SO | ✅ | 06-11 |
| 26.C.4 | StatusEffect SO 5개 (기절/출혈/중독/약화/화상) + ClassData SO 3개 생성 | ✅ | 06-11 |
| **26** | **스킬 트리 UI & 성장 시스템** | ✅ | 06-11 |

---

## 27.0 캐릭터 스프라이트 에셋 적용 — Olberic(전위) + Tressa(후위)

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| **27** | **캐릭터 스프라이트 에셋 적용** | ✅ | 06-13 |
| 27.1 | Olberic Animator(Olberic_Animator) Char_Vanguard 연결 + SetFacing flipX 방향 전환 | ✅ | 06-13 |
| 27.2 | UnitController PartyColor 파란 tint 제거 → Color.white | ✅ | 06-13 |
| 27.3 | SpriteCharacterView IsWalking Bool 기반 Walk 전환 — _walkParamChecked 캐시로 깜박임 해소 | ✅ | 06-13 |
| 27.4 | Olberic Idle/Attack/Skill 투명 프레임 제거 (idle 9→8, atk 12→11, magic_atk 6→4) | ✅ | 06-13 |
| 27.5 | UnitCombatAction 스킬 애니 재생 선딜→효과 처리 시점으로 이동 | ✅ | 06-13 |
| 27.6 | SpriteCharacterView.OnDeath() Hit 포즈 0.15s 프리즈 후 원본 색상 알파 페이드 아웃 | ✅ | 06-13 |
| 27.7 | SkillData.DamageType(Physical/Magical) 추가 → Physical=Attack, Magical=Skill 애니 분기 | ✅ | 06-13 |
| 27.8 | OlbericSpritePivotFixer.cs — atk/magic_atk/standby full-cell 재슬라이싱 Editor Script | ✅ | 06-13 |
| 27.9 | TressaAnimationBuilder.cs — idle/atk(3×6, 17프레임)/magic_atk/move/dying/dead + Tressa_Animator 생성 | ✅ | 06-13 |
| 27.10 | TherionAnimationBuilder.cs — idle(8f)/atk(10f)/magic_atk(4f)/move/dying/dead + Therion_Animator 생성 + Char_Midguard 연결 | ✅ | 06-13 |
| 27.11 | SkillData.DamageType.Support 추가 + AddSupportAnimation Editor Script — 3캐릭터 magic_standby 4f 클립+상태 추가 | ✅ | 06-13 |
| 27.12 | UnitCombatAction 연속 사격(3발) — _activeProjectiles 리스트, 발사 간격, 중간 타격 처리 | ✅ | 06-13 |
| 27.13 | SkillData 투사체 필드 추가 (isProjectile/Speed/Count/Interval) + Skill_Shot 연속 사격 3발 | ✅ | 06-13 |
| 27.14 | 치료 스킬 damageType Physical → Support (Heal/EmpoweredHeal/MassHeal) | ✅ | 06-13 |
| 27.15 | TickSpriteAnimator — AnimatorUpdateMode.Manual 제거, SampleAnimation 틱 기반 방식으로 재작성 | ✅ | 06-13 |

---

## 28.0 코드 리뷰 반영

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| 28.1 | DeathFade _baseColor.rgb 알파 페이드 (적 흰색 플래시 버그) | ✅ | 06-13 |
| 28.2 | ApplyDirectionalEffect PositioningCalculator + 커버 보정 추가 | ✅ | 06-13 |
| 28.3 | TickSpriteAnimator ApplyFrame 제거 → ForcePlay 원샷 메서드 추가 | ✅ | 06-13 |
| 28.4 | UnitActionEvent.skillId — skill.name 기반 안정 해시 + skillName 기록 | ✅ | 06-13 |
| 28.5 | 주석/문서 정정 (노란색→회색, SimTick 레이블, architecture.md 색상 테이블) | ✅ | 06-13 |
| 28.6 | SoundId.SkillHeal + AudioConfig 연결 — 치료 스킬 전용 마법 효과음 | ✅ | 06-13 |

---

## 29.0 이펙트 스프라이트 레이어 분리

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| 29.1 | ADR-0016 — 이펙트 레이어 분리 설계 결정 | ✅ | 06-13 |
| 29.2 | OlbericEffectSeparator — atk/magic_atk PNG 분리 Editor 스크립트 | ✅ | 06-13 |
| 29.3 | TickSpriteAnimator SetLinked/StopAndClear — 보조 애니메이터 동기화 | ✅ | 06-13 |
| 29.4 | SpriteCharacterView — EffectLayer 자동 탐지 및 SetFacing/SetVisible/DeathFade 연동 | ✅ | 06-13 |
| 29.5 | OlbericAnimationBuilder — _char.png 폴백 + 이펙트 컨트롤러 생성 | ✅ | 06-13 |
| 29.6 | Unity Editor: EffectLayer 자식 오브젝트 생성 및 메뉴 실행 | ✅ | 06-13 |
| 29.7 | 치료 스킬 이중 효과음 버그 수정 — ApplySkillEffect 순수 힐 early return | ✅ | 06-13 |

---

## 30.0 스킬 애니메이션 개선 + 스프라이트 피벗 보정

| ID | 산출물 | 상태 | 완료일 |
|----|--------|------|--------|
| 30.1 | 스테이지 클리어/실패 효과음 제거 — AudioManager BattleVictory/BattleDefeat 구독 제거 | ✅ | 06-13 |
| 30.2 | 스킬 PostDelay 공격 모션 유지 — OnActingComplete UseSkill Idle 생략, OnPostDelayComplete Idle 전환 | ✅ | 06-13 |
| 30.3 | 스킬 PreDelay 1프레임 고정 준비 자세 — TickSpriteAnimator.FreezeAtFirstFrame + UnitController 위임 | ✅ | 06-13 |
| 30.4 | 스킬 Acting 진입 시 2번째 프레임부터 재생 — TickSpriteAnimator.PlayFromFrame + UnitCombatAction 연결 | ✅ | 06-14 |
| 30.5 | Tressa 스프라이트 피벗 보정 — idle 기준 픽셀 측정, 전 애니메이션 pivot 계산, 전환 점프 제거 | ✅ | 06-14 |
| 30.6 | Olberic 스프라이트 피벗 보정 — OlbericSpritePivotFixer atk_char/magic_atk_char/standby/move/dying/dead | ✅ | 06-14 |

