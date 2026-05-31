# RTwP RPG — WBS (Work Breakdown Structure)
<!-- 이 파일은 CLAUDE.md 지침에 따라 작업 완료 시 자동 갱신됩니다 -->
> 최종 업데이트: 2026-05-31 (ADR 문서화 + 엔드-투-엔드 플레이어빌리티 수정)

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
| 6.9 | 전투 UI 개선 | ✅ | 05-16 |
| 6.9.1 | SkillPanel (이동/대기/스킬 버튼) | ✅ | 05-16 |
| 6.9.2 | SelectionRing | ✅ | 05-16 |
| 6.9.3 | TargetIndicator | ✅ | 05-16 |
| **7** | **마무리: 코드 수정 & 빌드 검증** | ✅ | 05-22 |
| 7.1 | 코드 품질 수정 | ✅ | 05-20 (2차) |
| 7.1.1 | SelectionRing GC 최적화 <!-- fix-gc-ring --> | ✅ | 05-20 |
| 7.1.2 | TargetIndicator GC 최적화 <!-- fix-gc-target --> | ✅ | 05-20 |
| 7.1.3 | SelectionRing Shader null 안전성 <!-- fix-shader-ring --> | ✅ | 05-20 |
| 7.1.4 | TargetIndicator Shader null 안전성 <!-- fix-shader-target --> | ✅ | 05-20 |
| 7.1.5 | MoveRangeVisualizer Shader null 안전성 | ✅ | 05-20 |
| 7.1.6 | SelectionRing / TargetIndicator DontDestroyOnLoad | ✅ | 05-20 |
| 7.1.7 | BossController TimeScale 무적 타이머 | ✅ | 05-20 |
| 7.1.8 | EnemyAI AttackAsHealer IsAlive 가드 | ✅ | 05-20 |
| 7.1.9 | StageRunner OnConfirmed 중복 구독 제거 | ✅ | 05-20 |
| 7.1.10 | StageRunner SpawnEnemy 반환값 직접 사용 | ✅ | 05-20 |
| 7.1.11 | UnitController NextId RuntimeInitialize 초기화 | ✅ | 05-20 |
| 7.1.12 | TutorialOverlay NextButton 필드 <!-- fix-tutorial-field --> | ✅ | 05-20 |
| 7.1.13 | TutorialOverlay Inspector 연결 <!-- fix-tutorial-inspector --> | ✅ | 05-20 |
| 7.1.14 | BattleSimulation 시간 미흐름 데드락 수정 (CommandQueue IsPaused 중 처리) | ✅ | 05-20 |
| 7.1.15 | BattleInputHandler LateUpdate 전환 (이동 버튼 클릭 → 월드 클릭 동일 프레임 충돌) | ✅ | 05-20 |
| 7.1.16 | SkillPanel SetMoveHighlight img.color 직접 변경 (normalColor×imgColor = 초록 버그) | ✅ | 05-20 |
| 7.1.17 | BattleInputHandler IsMoveMode 중 유닛 재선택 방지 (isActionPending 가드) | ✅ | 05-20 |
| 7.1.18 | TryUseSkill AP 사전 체크 (AP 부족 silent fail → IsPaused 데드락 방지) | ✅ | 05-20 |
| 7.1.19 | OnActingComplete GetPostDelay 호출 순서 수정 (ActiveSkill null 이전 호출) | ✅ | 05-20 |
| 7.1.20 | OnPostDelayComplete try-finally 보호 (예외 시 Phase 고착 → 유닛 먹통 방지) | ✅ | 05-20 |
| 7.2 | 틱 시스템 마이그레이션 | ✅ | 05-20 |
| 7.2.1 | Phase 1: 기반 파일 생성 (ActionPhase / UnitSimState / CommandQueue / BattleSimulation) | ✅ | 05-20 |
| 7.2.2 | Phase 2: UnitController 확장 + UnitCombatAction 상태머신 전환 | ✅ | 05-20 |
| 7.2.3 | Phase 3~5: 의존 시스템 Tick 전환 + TimeFlowManager Facade + BattleRecorder | ✅ | 05-20 |
| 7.2.4 | 전투 씬 회귀 테스트 결과 <!-- tick-test --> | ✅ | 05-22 |
| 7.3 | 최종 검증 | ✅ | 05-22 |
| 7.3.1 | 씬 플로우 테스트 결과 <!-- final-flow --> | ✅ | 05-22 |
| 7.3.2 | Windows Standalone 빌드 <!-- final-build --> | ✅ | 05-22 |
| 7.4 | 추가 버그 수정 | ✅ | 05-22 |
| 7.4.1 | StageRunner SpawnEnemy EnemyAI 중복 AddComponent 방지 (H-5) <!-- h-5-enemyai --> | ✅ | 05-22 |
| 7.4.2 | BattleSimulation accumulator unscaledDeltaTime 전환 (H-6) <!-- h-6-unscaled --> | ✅ | 05-22 |
| 7.4.3 | Sustained 스킬 PendingTimeCost 불일치 수정 (H-7) <!-- h-7-sustained --> | ✅ | 05-22 |
| 7.4.4 | TryExecutePendingSkill 실패 시 _pendingSkill 유지 (H-9) + RefreshButtons 자동 갱신 (H-10) | ✅ | 05-22 |
| 7.4.5 | CommandQueue 이중 소비 제거 (H-11) — Update 단일 경로로 통합 <!-- h-11-queue --> | ✅ | 05-22 |
| **7.5** | **중간 심각도 버그 수정 (M-1~M-12)** | ✅ | 05-22 |
| 7.5.1 | BattleResultScreen Continue → LoadChapterHub (M-1) | ✅ | 05-22 |
| 7.5.2 | APRecoveryHandler DoT 피해 시 AP 회복 방지 (M-2) | ✅ | 05-22 |
| 7.5.3 | UnitStatusHandler 동결 파괴 보너스 피해 isDot:true (M-3) | ✅ | 05-22 |
| 7.5.4 | CombatCalculator 패링 반격 피해 rawDamage 기반 (M-4) | ✅ | 05-22 |
| 7.5.5 | PositioningCalculator 동일 좌표 Front 처리 (M-5) | ✅ | 05-22 |
| 7.5.6 | EnemyAI MeleeRush detectRange 밖 타겟 제외 (M-6) | ✅ | 05-22 |
| 7.5.7 | GridManager GetReachableTiles IsWalkable 검사 (M-7) | ✅ | 05-22 |
| 7.5.8 | GridManager Move 점유 덮어쓰기 방지 (M-8) | ✅ | 05-22 |
| 7.5.9 | SaveLoadService 슬롯 범위 검증 (M-9) | ✅ | 05-22 |
| 7.5.10 | SaveLoadService 손상 JSON 예외처리 (M-10) | ✅ | 05-22 |
| 7.5.11 | UnitController TickAI EnemyAI 캐시 (M-11) | ✅ | 05-22 |
| 7.5.12 | InitiativeQueue GetOrderedUnits IReadOnlyList 반환 (M-12) | ✅ | 05-22 |
| **7.6** | **낮음 심각도 버그 수정 (L-A2, L-A4, L-B1, L-B4, L-C1~C4)** | ✅ | 05-22 |
| 7.6.1 | StageRunner OnDestroy 이벤트 구독 해제 (L-A2) | ✅ | 05-22 |
| 7.6.2 | BattleSimulation 매 틱 BossController GetComponent 캐시 (L-A4) | ✅ | 05-22 |
| 7.6.3 | BattleHUD DestroyImmediate → Destroy (L-B1) | ✅ | 05-22 |
| 7.6.4 | SkillButton onClick 리스너 중복 등록 방지 (L-B4) | ✅ | 05-22 |
| 7.6.5 | AudioManager SubscribeEvents Awake 이동 (L-C1) | ✅ | 05-22 |
| 7.6.6 | VFXManager BuildPool+이벤트 구독 Awake 이동 (L-C2) | ✅ | 05-22 |
| 7.6.7 | ReplayPlayer Play() 중복 코루틴 방지 + LoadRecord null 가드 (L-C3/C4) | ✅ | 05-22 |
| **7.7** | **타겟팅·색상 버그 근본 수정** | ✅ | 05-27 |
| 7.7.1 | BattleInputHandler 스킬/이동 발행 후 Deselect 제거 → 적 재타겟팅 가능 | ✅ | 05-27 |
| 7.7.2 | UnitCombatAction.IsBusy — CommandQueue HasCommandFor 포함 (1프레임 간격 해소) | ✅ | 05-27 |
| 7.7.3 | UnitCombatAction.StartAction 진입 시 SetHighlight(true) — 행동 중 노랑 표시 | ✅ | 05-27 |
| 7.7.4 | PartyManager.SelectUnit IsBusy 체크 — 행동 중 유닛 노랑 덮어쓰기 방지 | ✅ | 05-27 |
| 7.7.5 | SkillPanel.RefreshButtons 이동/대기 버튼 interactable 갱신 추가 | ✅ | 05-27 |
| **7.8** | **튜토리얼 KillEnemy 스텝 추가** | ✅ | 05-27 |
| 7.8.1 | EnemyHPBar WorldSpace Canvas 컴포넌트 | ✅ | 05-27 |
| 7.8.2 | TutorialManager KillEnemy 스텝 + ChapterHub 이동 | ✅ | 05-27 |
| 7.8.3 | GameManager.NewGame() tutorialDone 분기 | ✅ | 05-27 |
| 7.8.4 | Step_KillEnemy SO 생성 + Enemy_Basic HPBarCanvas 프리팹 + Tutorial 씬 연결 (MCP) | ✅ | 05-27 |
| **7.9** | **튜토리얼 플레이 버그 수정** | ✅ | 05-29 |
| 7.9.1 | Char_TutorialEnemy maxHP 50→200 (원샷 방지) + 테스트 업데이트 | ✅ | 05-29 |
| 7.9.2 | SpriteCharacterView OnUnitDied 구독 → 사망 시 회색+2초 페이드아웃 | ✅ | 05-29 |
| 7.9.3 | EnemyHPBar fillAmount→anchorMax.x 방식 전환 (WorldSpace HP 바 시각 반영) | ✅ | 05-29 |
| 7.9.4 | Enemy_Basic HPBarCanvas sizeDelta (80,8)→(200,16) 크기 확대 | ✅ | 05-29 |
| 7.9.5 | TutorialManager GameManager null 시 SceneManager.LoadScene fallback | ✅ | 05-29 |
| 7.9.6 | ChapterHubController 추가 — 씬 전환 시 ChapterHubScreen.Open() 자동 호출 | ✅ | 05-29 |
| **8.0** | **콘텐츠: 맵·허브 UI 구축** | ✅ | 05-30 |
| 8.0.1 | Tutorial 씬 맵 — 10×8 잔디+돌 테두리, 나무·덤불 장식 (Cainos 타일셋) | ✅ | 05-30 |
| 8.0.2 | ChapterHub UI — 헤더·임무목록·상세패널·출격버튼 + MissionSlot 프리팹 | ✅ | 05-30 |
| 8.0.3 | Battle 씬 맵 — 10×8 잔디+돌 테두리, 나무·덤불 장식 (Cainos 타일셋) | ✅ | 05-30 |
| **8.1** | **GameManager·PartyManager 연동** | ✅ | 05-30 |
| 8.1.1 | GameManager.InitDefaultParty() — 새 게임 시 partyMembers 초기화 | ✅ | 05-30 |
| 8.1.2 | GameManager.FindCharacter(id) — GameAssets 캐릭터 검색 공개 접근자 | ✅ | 05-30 |
| 8.1.3 | PartyManager.SpawnParty() SaveData 기반 스폰 + Inspector fallback | ✅ | 05-30 |
| 8.1.4 | UnitStats.SetCurrentHP(int) — 저장된 HP 복원용 세터 | ✅ | 05-30 |
| **8.2** | **다음 작업 예정** | ⬜ | — |
| 8.2.1 | GameAssets.allCharacters 스킬 연결 (Vanguard/Midguard/Rearguard) | ✅ | 05-30 |
| 8.2.2 | Ending 씬 UI 구축 (이미 완성 확인) | ✅ | 05-30 |
| 8.2.3 | 캐릭터 스프라이트/애니메이터 연결 (Unit_Animator + TX Player portrait) | ✅ | 05-30 |
| 8.2.4 | 장비 6종 SO 생성 + DropTable Ch1 연결 + GameAssets 등록 | ✅ | 05-30 |
| 8.2.5 | ShopScreen + SaveSlotPanel UI 구축 + ShopData_Ch1 에셋 생성 | ✅ | 05-30 |
| **9.0** | **엔드-투-엔드 플레이어빌리티 수정** | ✅ | 05-30 |
| 9.0.1 | StageRunner LootManager 적 사망 훅 (B1) — 골드·장비 드롭 활성화 | ✅ | 05-30 |
| 9.0.2 | GameManager.OnBattleWon 파티 HP 저장 (B2) — 체력 씬 전환 후 유지 | ✅ | 05-30 |
| 9.0.3 | BalanceConfig.startingGold + InitDefaultParty 초기 골드 (B3) | ✅ | 05-30 |
| 9.0.4 | ChapterHubController.CheckChapterFailed 호출 (B4) — 소프트락 방지 | ✅ | 05-30 |
| 9.0.5 | ChapterHubScreen 골드 표시 (B5) — txtGold UI 추가 | ✅ | 05-30 |
| 9.0.6 | BattleResultScreen UI 재구성 (B6) — 전투 결과 화면 표시 | ✅ | 05-30 |
| **10.0** | **코드 리뷰 수정** | ✅ | 05-31 |
| 10.0.1 | EventBus._snapshot → 풀 기반 재진입 안전 구조 | ✅ | 05-31 |
| 10.0.2 | BattleManager.cs 삭제 + Stage_01 씬에서 GameObject 제거 | ✅ | 05-31 |
| 10.0.3 | GameManager.FadeAndLoad EventBus.Clear 추가 (씬 전환 리스너 정리) | ✅ | 05-31 |
| 10.0.4 | SaveLoadService 세이브 파일 삭제 전 LogError 추가 | ✅ | 05-31 |
| 10.0.5 | GameManager.NewGame clueGaugePerChapter 크기를 챕터 수 기반으로 동적 결정 | ✅ | 05-31 |
| 10.0.6 | BattleResultScreen 주석 수정 (LoadReplay → LoadChapterHub) | ✅ | 05-31 |
| 10.0.7 | StageRunner.SpawnEnemy Resources.Load 결과 Dictionary 캐시 | ✅ | 05-31 |
| 10.0.8 | TimeFlowManager.ActiveActionCount 제거 + TimeFlowHUD 연동 정리 | ✅ | 05-31 |
| **11.0** | **허브→전투 씬 연결** | ✅ | 05-31 |
| 11.0.1 | StageRunner.OnMissionSelectedFromHub: GameManager.GetCurrentChapter() 우선 사용 (chapterData null 수정) | ✅ | 05-31 |
| 11.0.2 | DifficultyScaler.GenerateSpawns: chapter null 방어 체크 | ✅ | 05-31 |
| 11.0.3 | StageRunner.OnMissionSelectedFromHub: EliminateAll + PartyWipe 승패 조건 추가 | ✅ | 05-31 |
| 11.0.4 | Battle.unity: PartyManager.partyMemberPrefab 연결 (PartyMember_Prefab) | ✅ | 05-31 |
| 11.0.5 | Battle.unity: StageRunner.chapterData 연결 (ChapterData_Ch1) | ✅ | 05-31 |
| **12.0** | **StageConfig 웨이브 스테이지 시스템** | ✅ | 05-31 |
| 12.0.1 | StageConfig SO (stageId/waves/WaveConfig/SpawnEntry/WinConditionType/WaveTrigger) | ✅ | 05-31 |
| 12.0.2 | WaveRunner MonoBehaviour + WaveRunnerClearCondition (웨이브 순차 스폰) | ✅ | 05-31 |
| 12.0.3 | ChapterData.stages: StageConfig[] 추가 (MissionConfig[] 하위 호환 유지) | ✅ | 05-31 |
| 12.0.4 | ChapterProgressData StageConfig 오버로드 (RecordClear/IsCleared/IsUnlocked) | ✅ | 05-31 |
| 12.0.5 | StageRunner PendingStage 경로 + OnStageSelectedFromHub + SpawnEntryFromStage | ✅ | 05-31 |
| 12.0.6 | GameManager PendingStage + LoadBattle(StageConfig) + OnBattleWon(StageConfig) | ✅ | 05-31 |
| 12.0.7 | ChapterHubScreen StageConfig 슬롯 표시 (MissionConfig 슬롯과 공존) | ✅ | 05-31 |
| 12.0.8 | Stage_Ch1_M1_Patrol / M2_Ambush / M3_Investigate 에셋 생성 + ChapterData 등록 | ✅ | 05-31 |
| 12.0.9 | 스테이지 제작 가이드 (docs/guides/stage-creation-guide.md) | ✅ | 05-31 |
| **13.0** | **전투 결과 화면 개선** | ✅ | 05-31 |
| 13.0.1 | StageRunner.Update() 승패 폴링 — BattleSimulation 일시정지 무관 클리어 감지 | ✅ | 05-31 |
| 13.0.2 | BattleResultScreen 구조 개선 — GO 비활성 유지 + ShowResult 정적 메서드 + FindObjectOfType 폴백 | ✅ | 05-31 |
| 13.0.3 | BattleResultScreen 카드 UI — txtTitle/btnReplay 추가, 네이비 카드+골드 아웃라인 레이아웃 | ✅ | 05-31 |
| 13.0.4 | GameManager.OnBattleWonCore null 폴백 — CurrentSave null 시 ShowResult(0,null) | ✅ | 05-31 |
| **14.0** | **허브 UI 리디자인** | ✅ | 05-31 |
| 14.0.1 | ChapterHub 헤더 — IbarraRealNova-SemiBold 챕터 제목, Jost-SemiBold 스탯, 아이콘 버튼 | ✅ | 05-31 |
| 14.0.2 | ChapterHub 패널 — Outline 컴포넌트, 임무목록/출격정보 라벨 스타일 | ✅ | 05-31 |
| 14.0.3 | 상점/저장 버튼 — DarkBackground 아이콘 스프라이트 (Shop_DarkBG / Reload_DarkBG) | ✅ | 05-31 |
| 14.0.4 | 출격 버튼 — 레드-오렌지 강조색 + Outline, "출격" 중앙 텍스트 | ✅ | 05-31 |
| 14.0.5 | MissionSlot 프리팹 — 다크 스타일 + Outline 통일 | ✅ | 05-31 |
| **15.0** | **ADR 문서화 & 아키텍처 정비** | ✅ | 05-31 |
| 15.0.1 | ADR-0006: StageConfig + WaveRunner 신규 시스템 (레거시 StageData 공존) | ✅ | 05-31 |
| 15.0.2 | ADR-0007: ChapterHub 별도 씬 구조 + ChapterHubScreen active=true 타이밍 결정 | ✅ | 05-31 |
| 15.0.3 | ADR-0008: StageRunner.Update() 승패 폴링 (BattleSimulation 일시정지 무관) | ✅ | 05-31 |
| 15.0.4 | ADR-0009: Modern GDR + Cainos UI 아트 방향 — 폰트/컬러 팔레트 확정 | ✅ | 05-31 |
| 15.0.5 | ADR-0010: 코루틴 → 20 TPS 고정 틱 시뮬레이션 전환 | ✅ | 05-31 |
| 15.0.6 | CLAUDE.md ADR 지침 강화 — 코드 작성 전 ADR 의무화, docs/adr/ 경로 수정 | ✅ | 05-31 |
| **16.0** | **엔드-투-엔드 플레이어빌리티 버그 수정** | ✅ | 05-31 |
| 16.0.1 | StageRunner: EventBus OnUnitDied 구독 → LootManager.OnEnemyDefeated 연결 | ✅ | 05-31 |
| 16.0.2 | GameManager.OnBattleWonCore: 전투 후 파티 HP SaveData 동기화 | ✅ | 05-31 |
| 16.0.3 | GameManager.InitDefaultParty: BalanceConfig.startingGold 초기 골드 설정 | ✅ | 05-31 |
| 16.0.4 | ChapterHubController.Start: CheckChapterFailed() 호출 — 날짜 소진 소프트락 방지 | ✅ | 05-31 |
| 16.0.5 | ChapterHubScreen: txtGold 필드 + RefreshHeader() 골드 표시 | ✅ | 05-31 |
