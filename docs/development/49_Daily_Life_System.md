# Ace Career Development Bible
# 49 · Daily Life System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Daily Life System 定义整个 Ace Career 的日常生活系统。

它让玩家真正感受到自己不是在玩一个比赛模拟器，而是在经历一位职业网球运动员的人生。Daily Life 是整个 Career Mode 最重要的沉浸系统。

---

# Design Goals

✓ 沉浸感 ✓ 节奏感 ✓ 长期循环 ✓ Config Driven ✓ AI/玩家一致 ✓ 不增加重复劳动 ✓ 百年稳定

---

# Daily Structure（五段式节奏）

```
Morning Brief → Training/Recovery → Events → Simulation → Evening Summary
```

---

# Day Types

| Day Type | Today 展示 |
|----------|-----------|
| Training Day | Serve Session / Movement / Mental / Gym / Recovery |
| Match Day | Opponent / Surface / Weather / Condition / Tournament Round |
| Recovery Day | Massage / Stretch / Ice Bath / Sleep / Rest |
| Travel Day | Flight / Jet Lag / Travel Time / Arrival |
| Rest Day | Recovery / Media / Training Suggestion / Upcoming Goals |

---

# Daily Decisions（每天 1~3 个关键决策，不是 20 个按钮）

Training / Recovery / Rest / Medical / Coach / Travel / Media

---

# Key Features

- **Morning Brief**：Current Ranking / Today's Schedule / Fatigue / Mood / Upcoming Tournament / Top News（一眼了解今天）
- **Weekly Planning**：This Week's Tournament / Training / Recovery / Objectives
- **Dynamic Recommendations**：Fatigue 88 → Recovery Recommended（推荐而非强制）
- **Mood System**（未来）：Fresh/Focused/Tired/Excited/Frustrated → 影响训练效率
- **Daily Goals**：Prepare For Wimbledon / Recover / Improve Serve（来自 Career Goal）
- **Notifications**：Coach Contract Ending / Need Recovery / Sponsor Meeting / Media Interview
- **Daily Story**：Rival Wins / Ranking Update / New Record / Coach Change
- **Weekly Review**：Matches / Training / Growth / Income / News / Ranking
- **Monthly Review**：Titles / Record / Improvement / Goals / Highlights
- **Seasonal Review**：Season Awards / Best Match / Career Growth / Financial Summary / Legacy Progress（年度纪录片）
- **AI Daily Life**：AI 每天同样经历 Training/Recovery/Travel/Coach/Media/Matches
- **Apple Health 风格**：Good Morning→Today's Match→Recovery→Training→News→Career Progress（强调信息而非菜单）

---

# Config Files

daily.json / today.json / recommendations.json / events.json

---

# Performance

- Today Load <20ms
- Daily Update <30ms
- Weekly Summary <50ms

---

# Definition of Done

✓ 每天拥有职业节奏 ✓ Today 成为核心入口 ✓ 推荐而非强制 ✓ AI 同样拥有 Daily Life ✓ Apple 风格信息流 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

职业球员的人生并不是一年四大满贯，而是那些冠军之间的每一天。

Daily Life System 负责让玩家真正生活在这个职业网球世界里。

---

End of Document
