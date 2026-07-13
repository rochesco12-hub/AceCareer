# Ace Career Development Bible
# 14 · Match Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Match Engine 是整个 Ace Career 最核心的 Engine。

Match Schema 保存比赛。Match Engine 创造比赛。它决定每一分、每一局、每一盘、每一场比赛如何发生。

---

# Design Goals

✓ 完全自动模拟 ✓ 可解释 ✓ 可复现 ✓ Config Driven ✓ 不作弊 ✓ 支持 Live Match ✓ 支持 Replay

---

# Match Hierarchy

```
Match → Set → Game → Point → Shot
```

---

# Simulation Flow

Initialize Match → Generate Conditions → Play Set → Play Game → Play Point → Determine Winner → Generate Statistics → Generate Highlights → Save Match

---

# Core Engine Components

| Engine | 职责 |
|--------|------|
| Point Engine | 每一分的模拟（Serve → Return → Rally → Winner/Error）|
| Game Engine | 局内规则（0/15/30/40/Deuce/Advantage/Game）|
| Set Engine | 盘内规则（6-4 / 7-6 / 抢七 / 换边）|
| Shot Engine | 未来：完整回合模拟（Forehand/Backhand/Slice/Volley/Smash）|
| Momentum Engine | 比赛走势（连续破发→Momentum↑，连续失误→↓）|
| Pressure System | 关键分心理（Break/Set/Match Point/Tiebreak 时 Mental 权重提高）|
| Statistics Generator | 自动生成 Ace/双误/Winner/UE/破发点等完整技术统计 |
| Highlight Generator | 自动寻找最长回合/转折点/最大逆转/最快发球/赛点 |

---

# Modifiers（全部来自 Config）

- **Surface Modifier**：Clay → Movement+10% Serve-5%；Grass → Serve+12% Volley+8%
- **Fatigue Modifier**：Fatigue 85 → Movement-12%/Mental-8%/Serve-4%，比赛越长影响越大
- **Confidence Modifier**：连续破发↑ 连续双误↓ 影响关键分
- **Injury Modifier**：轻伤 Movement-15% Serve-6%；重伤 → Retirement
- **Difficulty**：Easy 下 AI 战术失误更多，Hard 下 AI 更合理，绝不直接修改能力值

---

# Deterministic Rule

同样 Seed + 同样 Player + 同样 Config = 同一结果。方便 Debug / Replay / Cloud。

---

# Performance

- Best Of 3 <20ms
- Best Of 5 <35ms
- Statistics <5ms
- Highlights <10ms

---

# Match Result Output

```swift
MatchResult { winner / loser / score / statistics / highlights / duration }
```

交给 Career / Ranking / News 下游消费。

---

# Definition of Done

✓ 完整模拟一场比赛 ✓ 支持所有比赛规则 ✓ 未来 Live Match

✓ Statistics 自动生成 ✓ Highlights 自动生成 ✓ Replay 可复现 ✓ Deterministic

---

# Final Principle

一场比赛不是随机决定胜负，而是由数千个真实发生的回合，共同组成一段值得被记住的职业网球故事。

---

End of Document
