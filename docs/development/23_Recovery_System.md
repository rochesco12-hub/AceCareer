# Ace Career Development Bible
# 23 · Recovery System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Recovery System 定义整个 Ace Career 的恢复系统。

恢复不是等待，而是职业网球最重要的一部分。恢复越好 → 训练效率越高 → 伤病越少 → 职业寿命越长。

---

# Design Goals

✓ 战略性 ✓ 长期影响 ✓ Config Driven ✓ AI/玩家一致 ✓ 不只是恢复体力 ✓ 支持未来 Recovery Center ✓ 百年稳定

---

# Recovery Types

| Type | Fatigue | Injury Risk | Confidence | Growth | 适合场景 |
|------|---------|-------------|------------|--------|----------|
| Complete Rest | ★★★★★ | ↓ | ★★★ | 无 | 连续赛事后 |
| Active Recovery | ★★★★ | ↓ | ★★ | 极微 | 保持状态 |
| Massage | ★★★★ | ↓↓ | ↑ | 无 | 连续赛事 |
| Medical Treatment | ★★★★★ | ↓↓↓ | ↑ | 无 | 伤病恢复（费用高）|
| Recovery Camp | ★★★★★ | ↓↓↓ | ↑↑ | 微 | 未来：高原/运动科学 |

---

# Recovery Formula

```
Recovery = Base × Recovery Quality × Age Modifier × Coach Bonus × Medical Bonus
```

---

# 非线性恢复曲线

- Fatigue 20 → 恢复极少（边际效应）
- Fatigue 50 → 正常恢复
- Fatigue 80 → 恢复明显
- Fatigue 95 → 恢复最快

---

# Age Modifier

| Age | Modifier |
|-----|----------|
| 20 | 1.10 |
| 25 | 1.00 |
| 30 | 0.92 |
| 35 | 0.78 |
| 38 | 0.65 |

---

# 特殊恢复

- **Injury Recovery**：Minor 3天 / Moderate 14天 / Major 2月（期间成长降低）
- **Mental Recovery**：恢复 Confidence/Motivation/Morale/Pressure（连续失败后更重要）
- **Match Recovery**：比赛结束自动进入，Best Of 3 → Fatigue 68 → Recovery
- **Tournament Recovery**：Monte Carlo → 1周 → Barcelona，玩家决定继续还是休息

---

# 联动效应

- **Coach Bonus**：Elite → Recovery +12%
- **Recovery → Growth**：Recovery Excellent → Training Efficiency +10%
- **Overtraining 惩罚**：连续训练恢复不足 → Fatigue↑ Growth↓ Injury↑

---

# Config Files

recovery.json / fatigue.json / age_modifier.json / medical.json / coach_bonus.json

---

# Performance

- Single Recovery <0.02ms
- 2200 Players <10ms
- Week Recovery Realtime

---

# Definition of Done

✓ 多种恢复方式 ✓ 身体/心理同时恢复 ✓ 年龄影响恢复 ✓ AI 自动恢复 ✓ Config 驱动 ✓ 支持未来医疗团队 ✓ 长期稳定

---

# Final Principle

冠军之间真正的差距很多时候不在训练，而在恢复。恢复得更快的人，才能训练得更多、比赛得更久、赢得更多冠军。

---

End of Document
