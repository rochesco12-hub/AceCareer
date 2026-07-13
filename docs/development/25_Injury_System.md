# Ace Career Development Bible
# 25 · Injury System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Injury System 定义整个 Ace Career 的伤病系统。

伤病不是随机惩罚，而是训练/比赛/恢复/年龄/运气共同作用后的自然结果。

一个好的 Injury System 应该让玩家觉得"这次受伤是我应该预料到的"，而不是"游戏在针对我"。

---

# Design Goals

✓ 数据驱动 ✓ 长期累积 ✓ Config Driven ✓ AI/玩家一致 ✓ 真实伤病类型 ✓ 恢复周期 ✓ 长期职业规划

---

# Injury Probability Formula

```
Base Risk × Fatigue × Age × Training Load × Recovery × Surface × Luck
```

Base Risk = 0.02%/天（极低），之后 Modifier 逐渐提高。

---

# Severity Levels

| Severity | Recovery | 示例 |
|----------|----------|------|
| Minor | 2~7 天 | 轻微肌肉不适 |
| Moderate | 1~4 周 | 肩部炎症/腰部拉伤 |
| Major | 1~4 月 | 踝关节扭伤 |
| Chronic | 长期管理 | 背部持续管理，Movement -3% |
| Career Threatening | 极少 | — |

---

# 伤病类型

Muscle / Hamstring / Calf / Shoulder / Elbow / Wrist / Back / Hip / Knee / Ankle / Illness（感冒/流感/食物中毒）

---

# Modifiers

- **Fatigue**：30→1.0x / 60→1.3x / 80→1.8x / 95→2.8x
- **Training**：Strength +8% / Endurance +12%
- **Match**：3场 Normal → 7场 Higher → 12场 Very High
- **Surface**：Clay→Muscle↑ / Hard→Knee+Back↑ / Grass→Ankle↓ Slip Risk↑
- **Age**：20→1.0x / 28→1.1x / 32→1.4x / 36→1.9x
- **Previous Injury**：同一位置复发 +15%

---

# 比赛中伤病

Medical Timeout → Continue 或 Retirement → 自动生成 Highlight/News/Story

---

# 恢复四阶段

Acute → Treatment → Rehabilitation → Return To Play

刚复出时（Recovery 80%）再次受伤风险 +20%，避免立刻满负荷。

---

# 未来：Medical Team

Doctor / Physio / Rehab Coach / Sports Scientist → 提高恢复速度 / 降低复发率

---

# AI 伤病

AI 自动决定 Continue / Withdraw / Recovery / Skip Tournament。不带伤无限比赛。

---

# Story Hook

重大伤病 → Career Crisis / Comeback / Retirement / Miracle Return → Story Engine 直接读取

---

# Config Files

injury.json / injury_probability.json / injury_recovery.json / surface_injury.json / medical.json

---

# Performance

- Risk Calculation <0.01ms
- 2200 Players <8ms
- Week Simulation Realtime

---

# Definition of Done

✓ 伤病完全概率驱动 ✓ Fatigue 深度参与 ✓ AI/玩家一致 ✓ 长期伤病 ✓ 比赛退赛 ✓ Story 可直接使用 ✓ 世界长期稳定

---

# Final Principle

真正的职业球员，最大的对手很多时候不是球网另一边的人，而是自己的身体。

Injury System 让每一次坚持、每一次复出、每一次冠军都拥有真正的价值。

---

End of Document
