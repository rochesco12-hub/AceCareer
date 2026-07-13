# Ace Career Development Bible
# 18 · Highlight Generator

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Highlight Generator 负责从一场已经完成的比赛中自动提取真正值得被记住的瞬间。

它回答："如果我向别人讲这场比赛，只能讲三件事，我应该讲什么？"

---

# Design Goals

✓ 自动生成 ✓ 完全数据驱动 ✓ 不依赖 AI ✓ 支持 Story/News/Replay/Career Timeline ✓ Deterministic

---

# Architecture

```
Point Events → Game Events → Set Events → Match Events → Highlight Detector → Importance Scoring → Highlight Timeline → Story Engine
```

---

# Eight Highlight Categories

| Category | 检测逻辑 |
|----------|----------|
| Turning Point | 比赛转折点（如 3:5→连赢四局→7:5）|
| Momentum | Momentum 大幅变化（连丢5分→连赢12分）|
| Pressure | Break/Set/Match Point / Tiebreak / Final Set |
| Comeback | 0:2→3:2 或 1:5→7:5 |
| Record | Fastest Serve / Longest Rally / Most Aces |
| Statistics | 超过阈值（25 Aces / 92% 1st Serve / 82 Winners）|
| Milestone | First ATP Win / Top100 Debut / 100th Win / 500th Ace |
| Special Events | Medical Timeout / Retirement / Code Violation / Challenge |

---

# Highlight Score

```
Importance × Pressure × Rarity × Story Value = Final Score
```

按分数排序，每场保留 Top 10，低分自动丢弃。

---

# Outputs

- **Story Tags**：Comeback / Upset / Dominant Win / Marathon / Revenge / Historic → Story Engine 直接读取
- **Match Rating**：Drama + Competition + Quality + Statistics + History = 8.7/10
- **Replay Hook**：Replay 直接跳转到 Highlight Point Timeline
- **News Hook**：News Engine 读取 Top Highlights → Headline → Summary

---

# Config Driven

所有阈值来自 `highlight.json`（Longest Rally ≥18 / Fastest Serve ≥220km/h / Comeback ≥3 Games 等）。

---

# Performance

- Generate Highlights <10ms
- Replay Jump <5ms
- Highlight Query Realtime

---

# Definition of Done

✓ 自动识别精彩瞬间 ✓ 自动评分 ✓ 自动生成 Story Tags ✓ 支持 Replay ✓ 支持 Career Timeline ✓ Config 驱动 ✓ Deterministic

---

# Final Principle

真正令人难忘的比赛不是因为比分，而是因为那些改变比赛、改变职业生涯、甚至改变历史的瞬间。

Highlight Generator 的职责就是把这些瞬间永久保留下来。

---

End of Document
