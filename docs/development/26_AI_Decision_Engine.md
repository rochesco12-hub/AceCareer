# Ace Career Development Bible
# 26 · AI Decision Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

AI Decision Engine 定义整个 Ace Career 中所有 AI 球员的决策系统。

AI 不应该像脚本或机器人。每位 AI 都应该拥有自己的性格/偏好/风险倾向/职业目标/长期规划，最终形成完全不同的职业生涯。

AI 永远不会问"最优解是什么"，只会问"对我来说，什么是最好的选择"。

---

# Design Goals

✓ 长期规划 ✓ 个性化 ✓ 数据驱动 ✓ 非脚本化 ✓ Config Driven ✓ 支持 Story Engine ✓ 百年稳定

---

# AI 九层架构

```
Personality → Career Goal → Current Situation → Evaluate Options → Score Options → Probability Engine → Decision → Action → Learning
```

---

# Personality（终身基本不变）

Aggressive / Conservative / Disciplined / Emotional / Professional / Risk Taker / Workaholic / Lazy

---

# Decision Score

```
Expected Reward + Career Goal + Risk + Fatigue + Economy + Surface Preference = Decision Score
```

分数最高不一定选择，进入 Probability Engine 保留随机性。

---

# Decision Categories

Tournament / Training / Recovery / Travel / Coach / Medical / Retirement / Lifestyle

---

# 关键行为规则

- **Tournament**：世界第 280 → ATP250× Challenger✓（积分收益更高）
- **Training**：自动选择当前短板 + 长期目标方向
- **Recovery**：Fatigue 85 → Skip Tournament → Recovery Week
- **Medical**：年轻球员更保守，老将可能坚持
- **Retirement**：Ranking + Motivation + Health + Money + Legacy + Goal Completion 综合决定，非固定年龄
- **Learning**：每赛季微调 Risk/Training/Tournament/Recovery；年轻时 Aggressive → 老将时 Stable

---

# AI Diversity

Clay Lover / Serve Bot / Counter Puncher / Big Match Player / Late Bloomer / Fragile Talent — 不会 2200 个一样。

---

# Story Hook

Unexpected Retirement / Coach Change / Skip Wimbledon / Return From Injury → Story Engine 直接读取

---

# Config Files

ai_personality.json / career_goal.json / decision_weight.json / risk.json / retirement.json

---

# Performance

- Single Decision <0.05ms
- 2200 Players <40ms
- Week Simulation Realtime

---

# Definition of Done

✓ AI 拥有独立人格 ✓ 长期职业目标 ✓ 非脚本决策 ✓ 学习能力 ✓ Config 驱动 ✓ 支持 Story Engine ✓ 世界长期稳定

---

# Final Principle

Ace Career 中最真实的对手，不是能力值最高的人，而是那个和你一样拥有梦想、性格、野心与遗憾的职业球员。

AI Decision Engine 赋予整个职业网球世界真正的生命。

---

End of Document
