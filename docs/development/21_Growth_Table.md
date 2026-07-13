# Ace Career Development Bible
# 21 · Growth Table

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Growth Table 定义整个 Ace Career 的成长系统。

它不是经验值/升级系统，而是训练、比赛经验、年龄、潜力共同作用后的长期变化。Growth System 决定整个 Career 的节奏。

---

# Design Goals

✓ 完全长期模拟 ✓ 非线性成长 ✓ Config Driven ✓ AI/玩家一致 ✓ 不可刷经验 ✓ 每位球员不同 ✓ 百年稳定

---

# Growth Formula

```
Growth = Training × Potential × Age Modifier × Coach Modifier × Recovery Modifier × Random Variance
```

---

# Age Curve（全部来自 Config）

| Age | Multiplier | 阶段 |
|-----|-----------|------|
| 16 | 2.20 | 快速成长期 |
| 17-18 | 2.00~1.80 | |
| 19-21 | 1.65~1.40 | |
| 22-24 | 1.30~1.10 | |
| 25 | 1.00 | 基准 |
| 26-29 | 0.95~0.80 | 缓慢下降 |
| 30+ | Decline | 衰退阶段 |

---

# Key Rules

- **Diminishing Return**：Serve 40→41 容易，92→93 极难（S Curve）
- **Training 专项化**：Serve Training → Serve +0.32 / Volley +0.05 / Movement +0.02
- **Match Experience**：ATP > Challenger > ITF（高质量比赛成长更多但疲劳更高）
- **Coach Modifier**：Elite +18% / Local +4%
- **Recovery Modifier**：Poor -20% / Excellent +8%
- **Confidence Modifier**：High +5% / Low -8%
- **Injury Modifier**：Minor -35% / Major -90%
- **Rookie Bonus**：前 3 赛季 +15%
- **Veteran Bonus**：Mental/Tactics/Pressure/Experience 仍可微弱成长

---

# Growth Cap

Current ≥ Potential → 停止成长。未来只能维护或下降。

Peak（~26 岁）：维持。Decline（30+）：Movement↓ Stamina↓ Recovery↓ Serve 最后下降。

---

# Growth Validation（每赛季自动检查）

Average Growth / Peak Age / Top100 Age / Junior Growth / Retirement Curve

---

# Config Files

growth.json / age_curve.json / training_growth.json / coach_bonus.json / injury_growth.json

---

# Performance

- Single Growth <0.05ms
- Weekly Growth <5ms
- 2200 Players <30ms

---

# Definition of Done

✓ 非线性成长 ✓ 年龄曲线合理 ✓ Potential 生效 ✓ AI/玩家一致 ✓ Config 驱动 ✓ 百年稳定 ✓ 无经验值系统

---

# Final Principle

真正优秀的职业球员不是一夜之间变强，而是在数千小时训练、数百场比赛、无数次失败与恢复中，一点一点成长为冠军。

---

End of Document
