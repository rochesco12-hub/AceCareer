# Ace Career Development Bible
# 24 · Fatigue System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Fatigue System 定义整个 Ace Career 的疲劳系统。

疲劳是连接 Training / Match / Recovery / Injury / Calendar / AI Decision 的核心纽带。没有 Fatigue，整个 Career 就会退化成无限训练、无限参赛、无限巅峰。

Fatigue 不代表体力值，而代表整个身体系统的综合负荷：身体疲劳 + 神经疲劳 + 心理疲劳 + 飞行疲劳 + 比赛压力。

---

# Design Goals

✓ 长期积累 ✓ 可恢复 ✓ Config Driven ✓ 非线性变化 ✓ AI/玩家一致 ✓ 影响职业规划 ✓ 百年稳定

---

# Fatigue Scale（0~100）

| Range | 状态 |
|-------|------|
| 0~20 | 完全恢复 |
| 20~40 | 轻度疲劳 |
| 40~60 | 正常职业状态（大部分球员长期维持）|
| 60~75 | 明显疲劳 |
| 75~90 | 高风险 |
| 90~100 | 危险状态 |

---

# Fatigue Sources + Modifiers

| Source | Fatigue Gain |
|--------|-------------|
| Serve Training | +6 |
| Strength Training | +12 |
| Endurance Training | +15 |
| Match Practice | +10 |
| Straight Sets Win | +12 |
| 3 Sets Close Match | +18 |
| 5 Sets Epic | +32 |
| Same City Travel | 0 |
| Domestic Travel | +3 |
| Europe Tour | +5 |
| Intercontinental | +12 |

**Surface Modifier**：Hard 100% / Clay 115% / Grass 90% / Indoor 95%

**Threshold Effects**：Fatigue >75 → Movement -8% Reaction -5%；Fatigue >90 → Injury Risk +40% Growth -50%

---

# 联动效应

- **Mental Fatigue**：Pressure/Losing Streak/Media → 影响 Confidence/Decision（不影响 Movement）
- **Seasonal Fatigue**：澳网→印第安维尔斯→迈阿密→蒙特卡洛→巴塞罗那→马德里→罗马→法网，即使无伤病 Fatigue 也会累积
- **Fatigue Decay**：只有 Recovery Engine 能降低 Fatigue，不会自动清零
- **长期高疲劳**：Growth↓ Recovery↓ Injury↑ Ranking↓ → 真实职业循环

---

# AI Fatigue

Fatigue >80 → AI 倾向 Skip Tournament / Recovery Week / Lower Training Load。不是无限比赛。

---

# UI

Today 页面显示：Fresh / Good / Normal / Heavy / Critical（不显示数字，更符合职业体验）。

---

# Config Files

fatigue.json / travel.json / surface.json / match_load.json / training_load.json

---

# Performance

- Single Update <0.01ms
- 2200 Players <8ms
- Week Simulation Realtime

---

# Definition of Done

✓ Fatigue 长期累积 ✓ 非线性影响能力 ✓ AI/玩家一致 ✓ Travel 纳入 ✓ Surface 纳入 ✓ Config 驱动 ✓ 世界长期稳定

---

# Final Principle

真正限制职业球员的从来不是天赋，而是身体能否支撑他继续走上下一块球场。Fatigue 就是整个职业网球世界最真实的限制。

---

End of Document
