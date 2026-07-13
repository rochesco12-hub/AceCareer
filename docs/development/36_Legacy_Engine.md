# Ace Career Development Bible
# 36 · Legacy Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Legacy Engine 定义整个 Ace Career 的传奇系统。

它回答："当球员退役以后，人们会如何记住他？" Legacy 不等于冠军数量/世界第一周数/奖金。真正的 Legacy 是整个职业生涯留下的影响力。Federer 的 Legacy 不仅来自 20 座大满贯，还来自优雅打法、统治时代、超长巅峰、全球影响力、宿敌、纪录。Legacy 永远大于冠军。

---

# Design Goals

✓ 长期累计 ✓ 多维评价 ✓ Config Driven ✓ AI/玩家一致 ✓ Hall of Fame ✓ GOAT 排行 ✓ 百年稳定

---

# Legacy 十维评价体系

| 维度 | 内容 | 权重 |
|------|------|------|
| Titles | Grand Slam ★5 / Masters ★4 / ATP500 ★3 / ATP250 ★2（质量>数量）|
| Ranking | Weeks No.1 / Career High / Top10 Weeks / Top100 Weeks（长期>短暂）|
| Longevity | Career Length / Peak Length / Consecutive Seasons / Matches Played |
| Records | Most Titles/Wins/Aces / Youngest/Oldest Champion |
| Rivalries | 15 Matches→Classic Rivalry→Historic Rivalry（没有宿敌很难成为传奇）|
| Historic Moments | Career Slam / Golden Slam / Five-set Epic / Historic Comeback |
| Popularity | (未来) Fans / Media / Global Influence / Nationality |
| Awards | Player Of Year / Sportsmanship / Comeback Award / Best Match |
| Era Impact | Dominated 2030s → Era Player（传奇球员通常代表一个时代）|
| Story | Career Arc / Narrative Weight / Memorable Moments |

---

# Legacy Grades

```
Local Hero → National Star → ATP Star → Grand Slam Legend → All-time Great → GOAT Candidate
```

---

# Legacy Score Formula

```
Titles + Ranking + Records + Longevity + Story + Historic Moments + Era = Legacy Score
```

---

# Key Features

- **GOAT Candidate**：20 Slams + 300 Weeks No.1 + Career Slam + Long Peak → GOAT 候选
- **Legacy Comparison**：Player A vs Player B（Titles/Ranking/Records/Legacy Score）
- **Hall of Fame Hook**：退役自动读取 Legacy Score → 不只是冠军数量
- **World Legacy**：Top10/100 Greatest / Era Legends 持续更新，每一代都会变化
- **Story Hook**：GOAT Debate / Historic Career / Legend Retires 自动生成

---

# Config Files

legacy.json / goat.json / awards.json / importance.json

---

# Performance

- Legacy Update <10ms
- Career Compare Realtime
- GOAT Ranking <20ms

---

# Definition of Done

✓ 多维 Legacy 评价 ✓ AI/玩家一致 ✓ 自动 GOAT 排名 ✓ 自动 Hall of Fame ✓ Story 深度联动 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

冠军会被超越。纪录会被打破。排名终将改变。真正留下来的，只有传奇。

Legacy Engine 负责决定这个世界会如何记住每一位职业球员。

---

End of Document
