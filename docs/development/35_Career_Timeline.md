# Ace Career Development Bible
# 35 · Career Timeline

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Career Timeline 定义整个 Ace Career 的职业生涯时间线。

它不是新闻流、不是比赛记录、更不是日志。它是一部自动生成的职业纪录片。十年后回顾职业生涯时，人们不会翻每一场比赛，而会回顾那些真正值得记住的瞬间。

---

# Design Goals

✓ 自动生成 ✓ 永久保存 ✓ Story 驱动 ✓ AI 球员同样拥有 ✓ 时间连续 ✓ 支持回顾 ✓ 百年稳定

---

# Timeline 五层架构

```
Career → Season → Tournament → Match → Moment
```

---

# 12 种 Timeline Categories

| Category | 示例 |
|----------|------|
| Debut | Professional Debut / First ATP Match / First ATP Win / Grand Slam Debut |
| Ranking | Top500 / Top100 / Top50 / Top10 / Top5 / World No.1 |
| Titles | First ATP Title / First Masters / First Grand Slam / Career Slam / Olympic Gold |
| Milestone | 100 Wins / 500 Wins / 1000 Aces / 300 Matches / 50 Titles |
| Rivalry | First Meeting / 10th Match / Grand Slam Final / H2H Lead / Final Meeting |
| Injury | Major Injury→Surgery→Return→First Victory（完整恢复过程）|
| Comeback | Outside Top100→Back To Top10→Champion（自动串联）|
| Records | Fastest Serve / Most Aces / Youngest/Oldest Champion |
| Historic | Career Grand Slam / Golden Slam / Longest Winning Streak / Historic Rivalry |
| Legacy | Career Arc 整体轨迹 |
| Retirement | Final Match→Farewell Ceremony→Retirement→Hall Of Fame |
| Awards | Player Of The Year / Most Improved / Sportsmanship 等 |

---

# Key Features

- **Timeline Importance**：Legendary / Historic / Major / Normal / Minor → 决定展示大小
- **Apple 风格卡片 UI**：🏆 2032 First Grand Slam Wimbledon → 点击展开完整故事
- **Memory System**：不仅保存事件，还保存 Story/Highlights/Statistics/Photos/News/Replay
- **Timeline Search**：按类别筛选（只显示 Titles / Injuries / Ranking）
- **Timeline Relationships**：First Slam→No.1→Dynasty→Retirement（形成 Career Arc）
- **Timeline Sharing**（未来）：Career Poster / Album / Video / Share Card
- **AI Timeline**：所有 AI 同样拥有完整 Timeline
- **Archive**：退役后永久保存，二十年后的传奇球员仍可查看

---

# Config Files

timeline.json / milestone.json / importance.json / career_arc.json

---

# Performance

- Timeline Query Realtime
- Career Load <10ms
- Search Realtime

---

# Definition of Done

✓ 自动记录职业生涯 ✓ Story 自动关联 ✓ 永久保存 ✓ AI 同样拥有 Timeline ✓ Apple 风格展示 ✓ Config 驱动 ✓ 支持未来 Career Album

---

# Final Principle

真正伟大的职业生涯不是由数字组成，而是由那些值得铭记的时刻组成。

Career Timeline 就是玩家职业生涯最珍贵的记忆相册。

---

End of Document
