# 씬 흐름 (Scene Flow)

```mermaid
flowchart LR
    MM[MainMenu] -->|NewGame| TUT[Tutorial]
    MM -->|Continue| HUB[ChapterHub]
    TUT -->|적 처치| HUB
    HUB -->|출격| BAT[Battle]
    BAT -->|클리어| HUB
    BAT -->|패배| REP[Replay]
    REP --> HUB
    BAT -->|보스+최종 챕터| END[Ending]

    classDef menu fill:#2d3748,stroke:#4a5568,color:#fff
    classDef play fill:#742a2a,stroke:#c53030,color:#fff
    class MM,HUB menu
    class TUT,BAT,REP,END play
```
