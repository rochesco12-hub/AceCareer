# Ace Career Development Bible
# 15 · Point Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Point Engine 是整个 Match Engine 的核心。它决定每一分到底是怎么产生的。

---

# Design Goals

✓ 完全概率驱动 ✓ 完全可解释 ✓ Config Driven ✓ 支持不同打法 ✓ 支持逐球动画 ✓ 完整技术统计

---

# Design Philosophy

不是 "Overall 92 vs 88 → Random → 92 赢"。

而是 "发球 → 接发 → 底线相持 → 机会球 → 终结 → 得分"。一分来自完整过程。

---

# Point Lifecycle

```
Start → Determine Server → Serve → Return → Baseline Rally → Attack Opportunity → Winner/Error → End
```

---

# Five Stages

| Stage | 内容 | 关键因素 |
|-------|------|----------|
| 1. Serve | Ace / Service Winner / In / Fault / Double Fault | Serve Power / Confidence / Fatigue / Surface |
| 2. Return | Winner Return / Neutral / Weak / Error | Return / Reaction / Movement / Mental |
| 3. Rally | 相持拍数（按分布模型：1拍8% / 2-4拍34% / 5-8拍32% / 9-15拍18% / 16+拍8%）| Forehand / Backhand / Movement / 打法风格 |
| 4. Attack | 机会球处理（短球/高球/弱回球→进攻）| Aggression / Volley / Mental |
| 5. Finish | Winner / Forced Error / Unforced Error | 全部属性综合 |

---

# Modifiers

- **Pressure**：Break Point → Winner↓ Error↑（顶级球员影响小，年轻球员影响大）
- **Momentum**：Momentum +8% → Attack Success +3%（作用很小，避免脚本感）
- **Surface**：Clay → Long Rally↑ Ace↓；Grass → Ace↑ Volley↑ Short Rally↑
- **Fatigue**：实时降低 Movement/Recovery，增加 Error，长盘越来越明显
- **Confidence**：主要影响关键分，普通分影响极小

---

# Key Rules

- Point Engine 永远调用 Probability Engine，自身不计算概率
- 所有概率来自 Config（serve.json / return.json / rally.json / surface.json / pressure.json）
- 同样 Seed + 同样 Player + 同样 Config = 100% 一致（Deterministic）

---

# Performance

- Single Point <0.05ms
- One Match <20ms
- Statistics Realtime
- Replay Deterministic

---

# PointResult Output

```swift
PointResult { winner / loser / reason / rallyLength / serveType / endingShot }
```

所有技术统计实时累计，无需赛后计算。

---

# Definition of Done

✓ 每一分拥有完整生命周期 ✓ 发球/接发/相持独立模拟

✓ 技术统计实时生成 ✓ 支持逐球动画 ✓ Deterministic ✓ Config 完全驱动

---

# Final Principle

一场伟大的比赛不是由最终比分组成，而是由几百分精彩的回合共同构成。

Point Engine 就是整个职业网球世界最小、也是最重要的真实单位。

---

End of Document
