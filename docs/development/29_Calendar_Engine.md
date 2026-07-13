# Ace Career Development Bible
# 29 · Calendar Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Calendar Engine 定义整个 Ace Career 的职业赛历系统。

Calendar 是整个世界唯一的时间系统。所有 Engine 都围绕 Calendar 运转。没有 Calendar 就没有 Tournament/Ranking/Recovery/Training/Story/World Simulation。

---

# Design Goals

✓ 完整 ATP 赛历 ✓ 支持未来 WTA ✓ Olympic Cycle ✓ Config Driven ✓ 长期稳定 ✓ 百年稳定 ✓ 唯一时间来源

---

# Design Philosophy

Ace Career 采用 **Week-Based Calendar**。整个职业世界每周推进一次（不是 Day Based）。ATP 所有赛事天然就是 Week Driven。

---

# Calendar Hierarchy

```
World → Season → Week → Day（Optional，未来 Live Match）→ Event
```

---

# Calendar Structure

```swift
Calendar {
    currentSeason / currentWeek / currentDay
    activeTournament / upcomingEvents / completedEvents
}
```

---

# Season = 52 Weeks

| 示例 | 内容 |
|------|------|
| Week 1-2 | Australian Open |
| Week 3 | Recovery |
| Week 4 | ATP250 |
| ... | ... |
| Week 48-52 | Off Season（恢复/训练/转会/教练更换/故事）|

---

# Key Features

- **Tournament Weeks**：Calendar 决定赛事顺序
- **Off Season**：Week 48~52，恢复/训练/教练更换/赛季规划
- **Travel Window**：Paris→London 自动生成 2 Days Travel → 影响 Fatigue
- **Recovery Window**：赛事结束→Recovery→下周
- **Olympic Cycle**（未来）：2032 Olympics 独立 Calendar Slot，不影响 ATP Ranking
- **Davis Cup**（未来）：独立 Slot，不影响 ATP Ranking
- **Calendar Conflict Detection**：同周两赛事 → Reject
- **Future Scheduling**：AI 读取未来 6 周 Calendar 规划赛季（不是只看下一站）
- **Weather Season**（未来）：Summer→Heat→Fatigue↑
- **Calendar Snapshot**：每周保存，方便 Replay/History

---

# Time Progression

```
Week → Simulation → Save → Week +1 → UI Refresh
```

不会跳周。任何系统禁止自己计算日期，统一从 Calendar Engine 读取。

---

# Config Files

calendar.json / tournament_schedule.json / holiday.json / olympic_cycle.json

---

# Performance

- Week Query <1ms
- Season Load <5ms
- 100 Seasons Stable

---

# Definition of Done

✓ Calendar 成为唯一时间系统 ✓ Week Based ✓ ATP 全赛历 ✓ Off Season ✓ Olympic Cycle ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

职业网球不是一场比赛，而是一整年的旅程。

Calendar Engine 决定整个世界何时开始、何时结束、又将在什么时候迎来新的冠军。

---

End of Document
