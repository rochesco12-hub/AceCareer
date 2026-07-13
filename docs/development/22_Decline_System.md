# Ace Career Development Bible
# 22 · Decline System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Decline System 定义整个 Ace Career 的能力衰退系统。

成长让球员成为冠军。衰退让冠军成为传奇。没有 Decline，整个世界最终会变成 2200 个 99 Overall。

---

# Design Goals

✓ 自然衰退 ✓ 非线性 ✓ 不可避免 ✓ 可延缓 ✓ Config Driven ✓ AI/玩家一致 ✓ 世界长期稳定

---

# Decline 是一个过程，不是一个事件

```
Age → Recovery↓ → Fatigue↑ → Injury↑ → Training Efficiency↓ → 能力缓慢下降 → 最终退役
```

---

# Decline Curve（非线性）

| Age | Decline Rate | 描述 |
|-----|-------------|------|
| 28 | 0% | 基准 |
| 29 | 0.2% | 开始 |
| 30 | 0.5% | |
| 31 | 0.8% | |
| 32 | 1.2% | |
| 33 | 1.8% | 明显 |
| 34 | 2.6% | |
| 35 | 3.5% | 快速 |
| 36 | 4.5% | |
| 38+ | Rapid | 剧烈 |

---

# 不同属性衰退速度不同

- **★★★★★**：Movement / Recovery → 最先下降
- **★★★★☆**：Stamina
- **★★★☆☆**：Volley
- **★★☆☆☆**：Serve → 保持较久
- **★☆☆☆☆**：Mental / Experience → **仍可成长**（+0.3%/年）

---

# 年龄对各系统的影响

- **Injury**：恢复速度 22岁100% → 32岁85% → 35岁70% → 38岁55%
- **Fatigue**：35 岁连续三站状态明显下降
- **Training**：Elite Training 可延缓 Decline 15%，但不能停止
- **Late Bloomers**：少数球员 Peak 在 31-34，增加多样性
- **Fast Decliners**：长期伤病/疲劳导致 Peak 很短

---

# Retirement Trigger

Decline 不直接退役，而通过：Ranking↓ → Income↓ → Motivation↓ → Retirement Decision（属于 AI Decision）

---

# World Balance（每 20 年自动检查）

Average Retirement Age / Top10 Average Age / Career Length / Peak Age / Decline Speed

---

# Config Files

decline.json / age_curve.json / physical_decline.json / mental_growth.json / recovery_curve.json

---

# Performance

- Single Player <0.02ms
- 2200 Players <15ms
- 100 Years Stable

---

# Definition of Done

✓ 自然衰退 ✓ 非线性年龄曲线 ✓ 身体先衰退 ✓ Mental 可继续成长 ✓ Config 驱动 ✓ AI/玩家一致 ✓ 世界长期稳定

---

# Final Principle

成长让球员成为冠军。衰退让冠军成为传奇。如果没有衰退，职业网球就不会有时代。

---

End of Document
