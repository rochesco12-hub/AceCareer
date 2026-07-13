# Ace Career Development Bible
# 56 · Travel Engine

Version: 1.0
Status: Final
Priority: P1

---

# Overview

Travel Engine 定义整个 Ace Career 的职业巡回旅行系统。

职业网球不是固定联赛，而是真正意义上的全球巡回。一周在澳大利亚，下一周在美国，再下一周在欧洲。Travel 完全自动完成，玩家只需要决定继续比赛还是休息。

---

# Design Goals

✓ 全球巡回 ✓ Calendar 驱动 ✓ Config Driven ✓ AI/玩家一致 ✓ 不增加繁琐操作 ✓ 时差与疲劳 ✓ 百年稳定

---

# Travel Lifecycle

```
Tournament Ends → Travel Day → Arrival → Jet Lag → Recovery → Tournament Starts
```

---

# Five Travel Categories

Domestic / Regional / International / Intercontinental / Home Return

---

# Key Metrics

| Metric | 示例 |
|--------|------|
| Distance | Paris→London ≈ Low / Tokyo→New York ≈ Very High |
| Travel Fatigue | Flight 14 Hours → +25（独立于 Match Fatigue）|
| Jet Lag | Time Zones → Recovery Needed（数天调整，不立刻恢复）|
| Arrival Status | Fresh / Normal / Tired / Exhausted |

---

# Key Features

- **Home Advantage**：Nationality = Tournament Country → No Jet Lag + Crowd Bonus + Popularity↑
- **Travel Recovery**：Rest Day/Massage/Sleep/Recovery Training
- **Schedule Planning**：选择 Play/Skip/Rest/Train → Travel 自动重新规划
- **AI Travel**：同样遵循 Travel→Recover→Compete（不瞬间移动）
- **Story Connection**：Long Road Trip / World Tour / Exhausted Champion
- **Media Connection**：Back-to-back Titles Across Continents → News
- **Economy Connection**：Flights/Hotels/Transportation 自动进入 Economy
- **Calendar Connection**：Travel 完全读取 Calendar，无需重复配置
- **Today Integration**：✈ Next Destination / Travel Time / Arrival Date / Jet Lag / Recovery Suggestion
- **World Map**（未来）：Melbourne→Indian Wells→Miami→Monte Carlo→Madrid→Rome→Paris→London 完整巡回路线

---

# Config Files

travel.json / flights.json / jetlag.json / travel_cost.json

---

# Performance

- Travel Update <5ms
- Route Query Realtime
- 2200 Players Stable

---

# Definition of Done

✓ 全球巡回模拟 ✓ Jet Lag 独立系统 ✓ AI/玩家一致 ✓ Today 深度整合 ✓ Story 自动联动 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

职业网球真正困难的不只是比赛，而是在世界各地不停奔波之后依然能够站上赛场。

Travel Engine 负责让玩家真正体验什么叫 ATP Tour。

---

End of Document
