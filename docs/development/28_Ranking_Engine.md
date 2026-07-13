# Ace Career Development Bible
# 28 · Ranking Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Ranking Engine 定义整个 Ace Career 的世界排名系统。

排名不是积分排行榜，而是整个职业世界竞争关系的体现。它决定参赛资格、种子席位、赞助、AI 规划、新闻报道。

---

# Design Goals

✓ 完全遵循 ATP 积分体系 ✓ Config Driven ✓ 长期稳定 ✓ Race Ranking ✓ 历史排名 ✓ 未来 WTA ✓ 百年稳定

---

# Design Philosophy

世界排名不是累计积分，而是 **Rolling 52 Weeks**。任何赛事一年后自动失效，新成绩自动替换。整个排名始终保持动态。

---

# Four Ranking Types

| Type | 计算规则 | 用途 |
|------|----------|------|
| ATP Ranking | Last 52 Weeks Best Results | 唯一官方排名 |
| Race Ranking | Current Season Only | ATP Finals |
| Surface Ranking | Hard/Clay/Grass/Indoor 分别计算 | Story / AI / 数据分析 |
| Historical Ranking | 每周 Snapshot 永久保存 | 走势图 / Career / History |

---

# Ranking Update Flow（事务执行）

```
Award Points → Remove Expired Points → Recalculate → Sort → Tie Break → Publish Events
```

---

# Tie Break Rules

More Titles → Better Slam Result → Recent Result → Alphabetical ID

---

# Key Features

- **Rolling Points**：2028 Wimbledon Champion 2000pts → 2029 Wimbledon 赛前自动移除
- **Best Results**（未来）：Grand Slam/Masters 强制计入，ATP500/250 取最佳
- **Ranking Movement**：自动计算 +12 / -5 / No Change → News/Today/Career 使用
- **Ranking Events**：自动检测 Top500/100/50/10/5/No.1 → Story/News/Career Timeline
- **Seed Generation**：读取 Current Ranking（不读取 Overall）
- **Protected Ranking**（未来）：6个月伤病 → Protected Ranking
- **Live Ranking**（未来）：Quarterfinal → Projected Ranking 12
- **Weekly Snapshot**：Top100 每周存档 → 完整历史
- **Validation**：每周检查 Duplicate Rank/Points/Gap/Expired/History Integrity

---

# Ranking Pressure（影响 AI）

Rank 103 → Need Top100 → Play Challenger。世界第 5 不会这样做。

---

# Hall of Fame

Career High / Weeks No.1 / Top10 Weeks — 全部来自 Ranking History。

---

# Config Files

ranking.json / points.json / best_results.json / seed.json / tie_break.json

---

# Performance

- Ranking Update <20ms
- 2200 Players <40ms
- History Save <5ms
- Live Projection Realtime

---

# Definition of Done

✓ Rolling 52 Weeks ✓ ATP 与 Race 分离 ✓ 历史排名永久保存 ✓ 自动生成种子 ✓ Config 驱动 ✓ 支持 Live Ranking ✓ 百年稳定

---

# Final Principle

真正重要的不是世界第一，而是成为世界第一之后还能在那里待多久。

Ranking Engine 记录着整个职业网球世界每一周的兴衰更替。

---

End of Document
