# Ace Career Development Bible
# 27 · World Simulation Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

World Simulation Engine 是整个 Ace Career 的世界运行引擎。

它回答："当玩家没有看到的时候，这个世界发生了什么。" 整个职业网球世界不会因为玩家关闭比赛页面而停止。

Ace Career 不是一个玩家+NPC 的游戏，而是一个真实存在的职业网球世界。玩家只是其中一名职业球员。

---

# Design Goals

✓ 世界持续运行 ✓ 完全数据驱动 ✓ AI 自主发展 ✓ 长期稳定 ✓ Config Driven ✓ 百年稳定 ✓ 玩家不是世界中心

---

# Weekly Pipeline（固定执行顺序）

```
Advance Week → Calendar → Tournament → Match → Ranking → Career → Story → News → World Update → Save
```

世界最小模拟单位：**One Week**（不是一天也不是一年）。ATP Calendar 本身就是 Week Driven。

---

# 每周模拟内容

Tournament Entry → Matches → Ranking Update → Training → Recovery → Travel → Coach → Retirement → Story → News

---

# 各系统自动运行

- **Tournament**：AI 自动报名/抽签/比赛/冠军/奖金/积分（玩家未参加同样模拟）
- **Match**：全部 AI 比赛统一调用 Match Engine，没有快速随机
- **Ranking**：赛事结束统一更新，世界排名永远真实
- **Recovery**：比赛结束全部 AI 自动恢复，不会无限满状态
- **Training**：无比赛时 AI 根据 Goal/Fatigue/Coach/Potential 自动训练
- **Coach**：AI 自动 Hire/Fire/Upgrade/Renew，教练持续流动
- **Injury**：训练+比赛+旅行共同产生伤病
- **Retirement**：赛季结束自动评估 Health/Ranking/Money/Goal
- **New Players**：每赛季自动生成 16~18 岁 Junior→ITF→ATP
- **Hall of Fame**：退役后 Career Evaluation → 永久保存

---

# 关键规则

- **Population Balance**：Active ≈2200 / Junior ≈400 / Retired Unlimited
- **Deterministic**：Same Seed + Config + Save = 100% 一致
- **Background vs Foreground**：Week Simulation 必须由玩家主动推进，避免世界自动流逝
- **Fast Simulation**（未来）：Advance 1 Week / 1 Month / 1 Season 全部调用同一 Engine

---

# Performance

- Advance Week <100ms
- One Season <3s
- 100 Seasons <5min
- Memory Stable

---

# Definition of Done

✓ 世界持续运行 ✓ AI 自主发展 ✓ 新老交替 ✓ 新闻持续生成 ✓ 历史永久积累 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

玩家不是这个世界的创造者。玩家只是这个世界里的一名职业球员。

即使玩家什么都不做，这个世界依然会不断前进。

---

End of Document
