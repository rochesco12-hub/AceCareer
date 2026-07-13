# Ace Career Development Bible
# 53 · Player Progression System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Player Progression System 定义整个 Ace Career 的成长系统。

Progression 不等于升级。它是一整套天赋→训练→比赛→成长→巅峰→衰退的人生曲线。回答：为什么有些球员成为传奇，而有些球员始终停留在普通职业球员。

---

# Design Goals

✓ 长期成长 ✓ 非线性成长 ✓ Config Driven ✓ AI/玩家一致 ✓ 百年稳定 ✓ 每位球员不同 ✓ 没有固定剧本

---

# Six Growth Stages

```
Junior → Prospect → Developing → Peak → Veteran → Decline
```

---

# Growth Curve（S Curve）

18↑↑↑ / 22↑↑ / 26↑ / 29 Peak / 32↓ / 35↓↓ / 38↓↓↓

---

# Growth Formula

```
Development Speed = Potential × Training × Coach × Discipline × Recovery
```

---

# Key Features

- **Potential**（0~100）：决定理论上限，不一定达到
- **Match Learning**：Lost Five Sets → Experience↑（成长不只来自胜利）
- **Skill Development**：Serve/Forehand/Volley/Movement/Mental 独立成长（不整体增加）
- **Plateau**：Serve 92 → Need Elite Coach → Breakthrough（高能力越来越难提升）
- **Peak Window**：26~31 能力最稳定
- **Decline**：30+ Recovery↓/Speed↓/Endurance↓/但 Experience↑/Mental↑（真实老将）
- **Late Bloomers**：24 Normal→30 Peak（来自 Personality+Training+Story）
- **Early Peak**：19 Top10→24 Peak→28 Decline（世界更加真实）
- **Injury Impact**：ACL → Movement Cap↓/Recovery Speed↓（不是休息结束就恢复原样）
- **Confidence Impact**：长期失败→Confidence↓→Growth↓（Story 真正影响成长）
- **Coach Impact**：影响成长效率而非能力上限
- **Dynamic Ceiling**：Potential 85 + Legendary Career → Potential 87（极少数可突破）
- **AI Progression**：完全遵循相同成长规则，不作弊

---

# Config Files

progression.json / growth_curve.json / potential.json / decline.json

---

# Performance

- Growth Update <5ms
- Weekly Progression <20ms
- 2200 Players Stable

---

# Definition of Done

✓ 非线性成长 ✓ AI/玩家一致 ✓ 成长平台期 ✓ 巅峰与衰退 ✓ Story 深度联动 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

真正伟大的职业生涯不是不断变强，而是在正确的时间成长、在巅峰时统治世界、在衰退时学会坚持。

Player Progression System 负责塑造每一位球员独一无二的人生曲线。

---

End of Document
