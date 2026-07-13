# Ace Career Game Design Document
## Global Data Model

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Data Model（数据模型）定义 Ace Career 整个世界的数据结构。

所有系统：

- Tournament
- Match
- Ranking
- Training
- Injury
- Economy
- News
- AI
- Save

全部依赖这一套数据模型。

任何系统不得自行创建新的核心数据结构。

所有数据必须通过统一 Schema 管理。

---

# 2. Design Goal

Data Model 必须满足：

- 单一数据源（Single Source of Truth）
- 长期 Career（20~50 Season）
- 可存档
- 可同步
- 可扩展
- 不产生重复数据

每一个对象只保存一次。

其它系统全部引用。

---

# 3. Core Objects

Ace Career 核心对象：

```text
Career
Season
Week
Player
Tournament
Draw
Match
Ranking
Training
Health
Finance
News
Coach
History
Save
```

所有对象均拥有唯一 ID。

---

# 4. Career Object

```text
Career
CareerID
PlayerID
CreatedAt
Difficulty
CurrentSeason
CurrentWeek
CurrentRanking
CareerStatus
CareerEarnings
Titles
GrandSlams
HighestRanking
CurrentCoach
CurrentFitness
CurrentHealth
```

Career 永久存在。

不会重置。

---

# 5. Season Object

```text
Season
SeasonID
Year
Week
Status
ChampionList
RaceChampion
WorldNo1
Completed
```

Season 保存年度数据。

赛季结束后归档。

---

# 6. Week Object

```text
Week
WeekID
Season
WeekNumber
WeekType
CurrentSurface
CurrentRegion
RankingUpdated
NewsGenerated
TournamentList
Status
```

Week 是所有系统的时间入口。

---

# 7. Player Object

```text
Player
PlayerID
FirstName
LastName
Nationality
Birthday
Age
Height
Weight
DominantHand
Backhand
TurnedPro
CurrentRanking
CareerHigh
CurrentPoints
RacePoints
Confidence
Fatigue
HealthState
CoachID
HomeCountry
PreferredSurface
CurrentLocation
```

Player 不保存比赛记录。

比赛记录属于 Match。

---

# 8. Tournament Object

```text
Tournament
TournamentID
Category
Name
Country
City
Surface
PrizeMoney
ChampionPoints
DrawSize
QualifyingSize
Week
Status
Champion
RunnerUp
```

Tournament 保存赛事信息。

不保存比赛过程。

---

# 9. Draw Object

```text
Draw
DrawID
TournamentID
DrawSize
SeedList
MainDraw
QualifyingDraw
Status
CreatedAt
```

Draw 负责签表。

不负责比分。

---

# 10. Match Object

```text
Match
MatchID
TournamentID
Round
PlayerA
PlayerB
Winner
Loser
Score
Duration
Court
Status
CompletedAt
```

Match 永久保存。

不得删除。

---

# 11. Ranking Object

```text
Ranking
PlayerID
CurrentRanking
CareerHigh
ATPPoints
RacePoints
Week
Season
UpdatedAt
```

Ranking：

每周更新。

历史：

永久保存。

---

# 12. Training Object

```text
Training
TrainingID
PlayerID
Category
Intensity
Completed
FatigueGain
Improvement
Week
```

Training：

只保存训练。

成长数据：

写入 Player。

---

# 13. Health Object

```text
Health
PlayerID
CurrentState
Fatigue
InjuryType
RecoveryWeeks
MedicalRisk
MatchReady
TrainingReady
```

Health：

独立维护。

---

# 14. Finance Object

```text
Finance
PlayerID
CareerMoney
SeasonMoney
Cash
PrizeMoney
SponsorIncome
TravelCost
CoachSalary
MedicalCost
```

所有收入。

全部流水保存。

---

# 15. News Object

```text
News
NewsID
Category
Headline
Summary
Body
Priority
PlayerID
TournamentID
Season
Week
```

News 永久保存。

---

# 16. Coach Object

```text
Coach
CoachID
Name
Level
ServeBonus
FitnessBonus
RecoveryBonus
Salary
ContractEnd
```

未来：

可扩展：

Physio。

Fitness Coach。

Psychologist。

---

# 17. History Object

```text
History
HistoryID
Season
Week
TournamentID
Champion
RunnerUp
RankingHistory
NewsHistory
Statistics
```

History：

不可修改。

---

# 18. Save Object

```text
Save
SaveID
CareerID
Season
Week
Timestamp
Version
Checksum
CloudVersion
LocalVersion
```

支持：

自动存档。

云同步。

版本恢复。

---

# 19. Object Relationship

```text
Career
├── Player
├── Season
│   ├── Week
│   │   ├── Tournament
│   │   │   ├── Draw
│   │   │   │   └── Match
│   │   ├── Ranking
│   │   ├── News
│   │   ├── Training
│   │   ├── Health
│   │   └── Finance
└── History
```

所有对象：

唯一引用。

禁止重复保存。

---

# 20. Primary Keys

所有核心对象：

必须使用 UUID。

例如：

```text
career_xxxxx
player_xxxxx
tournament_xxxxx
match_xxxxx
week_xxxxx
```

禁止：

使用数组索引。

禁止：

使用 Position。

作为唯一 ID。

---

# 21. Data Rules

所有对象必须满足：

✓ 不重复

✓ 可序列化

✓ 可存档

✓ 可云同步

✓ 可版本升级

✓ 可长期维护

---

# 22. Acceptance Criteria

完成后：

✓ 全部系统共享同一 Data Model

✓ 不存在重复数据

✓ Save 可恢复

✓ Cloud 可同步

✓ 支持长期 Career

✓ 支持未来 Ace League 集成

---

End of Document
