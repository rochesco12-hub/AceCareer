# Ace Career Development Bible
# 16 · Probability Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Probability Engine 是整个 Ace Career 所有模拟系统的数学核心。

它不负责比赛/排名/AI/新闻。它只负责一件事：**计算概率。**

整个游戏中所有"可能发生"的事情，都必须通过 Probability Engine 计算，而不是直接随机。

---

# Design Goals

✓ 可预测 ✓ 可解释 ✓ 可配置 ✓ 可复现 ✓ 可测试 ✓ 不作弊 ✓ 禁止直接 Random()

---

# Architecture

```
Probability Engine
├── Base Probability      基础概率
├── Modifier System       逐层叠加（Surface→Fatigue→Confidence→Momentum→Pressure→Weather）
├── Weight Calculator     各因素权重（Serve 35%/Return 25%/Fatigue 10%/Confidence 10%/Surface 8%/Momentum 7%/Weather 5%）
├── Random Generator      统一入口（禁止 Bool.random()/Int.random()）
├── Distribution Models   Normal / Uniform / Poisson / Exponential / Custom Curve
└── Result Resolver       归一化 + Clamp [0%~100%]
```

---

# Probability Pipeline

```
Input → Base Value → Apply Modifiers → Normalize → Clamp → Random Sample → Result
```

---

# Seed System

```
World Seed → Week Seed → Match Seed → Point Seed
```

保证同一场比赛永远一致。

---

# 关键曲线（全部非线性）

- **能力曲线**：S Curve — Serve 90→92 的成长远小于 40→42
- **Confidence 曲线**：指数衰减 — 50→90 不是简单的 +40%
- **Fatigue 曲线**：20几乎无影响 / 50轻微下降 / 80明显下降 / 95急剧下降
- **Injury 曲线**：Fatigue↑ + 连续比赛 + Recovery↓ → Risk↑
- **Growth 曲线**：18快速 / 22稳定 / 26Peak / 31轻微下降 / 35明显下降
- **AI Decision 曲线**：不是 100% 最优选择，保留随机性保证世界多样性

---

# 职责范围

Point Probability / Shot Probability / Serve/Return/Rally Probability / Injury Probability / Growth Probability / AI Decision Probability / Narrative Trigger Probability

全部统一来源。

---

# Config Driven

所有概率来自 `probability.json` / `serve.json` / `growth.json` / `injury.json` / `story.json`。Engine 不保存任何数字。

---

# Deterministic

Same Seed + Same Config + Same Inputs = Same Result。任何平台一致。

---

# Performance

- One Probability <0.001ms
- One Point <0.05ms
- One Match <20ms
- Week Simulation <100ms

---

# Definition of Done

✓ 所有随机统一管理 ✓ 所有概率可解释 ✓ 支持 Replay ✓ Debug ✓ Config 驱动 ✓ 非线性成长 ✓ Deterministic

---

# Final Principle

在 Ace Career 中，没有任何事情是"随机发生"的。

所有结果都是无数个真实概率共同作用后的必然结果。

Probability Engine 就是整个职业网球世界背后的数学基础。

---

End of Document
