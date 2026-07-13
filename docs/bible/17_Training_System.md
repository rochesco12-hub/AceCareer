# Ace Career Game Design Document
## Training System

Version: 1.0
Status: Draft
Priority: P1

---

# 1. Purpose

Training System（训练系统）负责模拟职业球员的长期成长。

训练不会立即提升能力。

而是在长期职业生涯中不断积累，最终形成不同类型的球员。

训练是 Career Mode 最重要的长期成长系统之一。

---

# 2. Design Goal

训练系统必须满足：

- 长期成长
- 存在取舍
- 真实职业训练
- 与疲劳、伤病联动
- AI 与玩家一致

玩家不能无限训练。

成长必须付出恢复成本。

---

# 3. Training Philosophy

现实职业球员不会每天都练所有项目。

每周必须决定：

- 提高什么
- 放弃什么
- 是否恢复

成长来源于长期规划。

不是一次训练。

---

# 4. Training Categories

训练分为六大类：

Technical

Physical

Mental

Recovery

Strategy

Serve Practice

每个类别拥有不同成长曲线。

---

# 5. Technical Training

提升：

- Forehand
- Backhand
- Volley
- Slice
- Return

副作用：

Fatigue +10

---

# 6. Physical Training

提升：

- Strength
- Speed
- Agility
- Endurance
- Explosive Power

副作用：

Fatigue +20

Injury Risk +5%

---

# 7. Mental Training

提升：

- Confidence
- Pressure Resistance
- Focus

适合：

Grand Slam 前。

Fatigue：

极低。

---

# 8. Recovery Training

包括：

- Stretch
- Yoga
- Massage
- Mobility

恢复：

Fatigue

减少：

Injury Risk

不会增加能力值。

---

# 9. Strategy Training

包括：

- Match Review
- Opponent Analysis
- Tactical Simulation

提升：

Match IQ

未来 Match AI 将引用。

---

# 10. Serve Practice

独立训练：

- First Serve
- Second Serve
- Serve Accuracy
- Serve Speed

不会提升：

Forehand。

---

# 11. Weekly Training Plan

每周最多安排：

3 个 Training Block。

例如：

Monday

Strength

Wednesday

Serve

Friday

Recovery

系统自动计算：

疲劳。

---

# 12. Training Intensity

支持：

Light

Medium

Heavy

Recovery

不同强度：

成长速度不同。

Fatigue 不同。

---

# 13. Progress Curve

成长不是线性。

例如：

Forehand：

40→60

成长快。

90→95

成长极慢。

避免：

无限成长。

---

# 14. Training Fatigue

训练后：

增加：

Fatigue。

Fatigue：

超过：

80。

成长效率下降。

超过：

90。

增加：

伤病风险。

---

# 15. AI Training

AI：

每周自动训练。

根据：

年龄。

伤病。

赛季目标。

制定计划。

不会：

无限练力量。

---

# 16. Coach Bonus

不同教练：

提供不同成长加成。

例如：

Serve Coach

Serve +15%

Fitness Coach

Strength +10%

Psychologist

Mental +20%

---

# 17. Data Model

```text
TrainingPlan
PlayerID
Week
TrainingType
Intensity
Duration
FatigueGain
Improvement
CoachBonus
```

---

# 18. Acceptance Criteria

✓ 每周可安排训练

✓ Fatigue 正确增加

✓ Recovery 生效

✓ AI 自动训练

✓ 长期成长合理

✓ 与 Injury 系统联动

---

End of Document
