# Ace Career Game Design Document
## Injury & Recovery System

Version: 1.0
Status: Draft
Priority: P1

---

# 1. Purpose

Injury System（伤病系统）负责模拟职业网球运动员整个职业生涯中的身体状态。

它不是随机扣血系统。

而是根据：

- 比赛
- 训练
- 疲劳
- 年龄
- 恢复质量

动态决定球员是否受伤。

伤病应该成为职业规划的一部分，而不是随机惩罚。

---

# 2. Design Goal

伤病系统必须做到：

- 足够真实
- 可以预防
- 可以恢复
- 不会无限受伤
- 不会完全没有伤病
- AI 与玩家遵循同一规则

---

# 3. Core Philosophy

现实职业球员：

不会：

每天受伤。

也不会：

永远健康。

伤病来自：

长期疲劳累积。

而不是：

随机事件。

---

# 4. Injury Pipeline

```text
Training
↓
Fatigue
↓
Risk Evaluation
↓
Minor Injury
↓
Treatment
↓
Recovery
↓
Healthy
```

比赛也会触发：

Risk Evaluation。

---

# 5. Health Model

每位球员拥有：

```text
Health
100
Fatigue
0~100
Fitness
0~100
Recovery
0~100
```

系统：

每周更新一次。

---

# 6. Injury Risk

受伤概率：

不是固定。

而是：

综合计算。

```text
Risk
=
Fatigue
+
Training Load
+
Age
+
Match Frequency
-
Recovery
-
Medical Bonus
```

---

# 7. Injury Types

支持：

Muscle Fatigue

↓

Back Pain

↓

Shoulder Pain

↓

Elbow

↓

Wrist

↓

Knee

↓

Ankle

↓

Hamstring

↓

Illness

未来：

继续扩展。

---

# 8. Injury Severity

四个等级：

Healthy

↓

Minor

↓

Moderate

↓

Major

不同等级：

恢复时间不同。

---

# 9. Minor Injury

例如：

腰部轻微拉伤。

允许：

继续比赛。

能力：

下降。

恢复：

1~2 周。

---

# 10. Moderate Injury

建议：

退赛。

恢复：

2~6 周。

继续比赛：

伤势恶化概率增加。

---

# 11. Major Injury

立即退出赛事。

进入：

Medical。

恢复：

6~40 周。

期间：

禁止比赛。

---

# 12. Fatigue

Fatigue 来源：

训练。

比赛。

旅行。

恢复不足。

Fatigue：

超过：

80。

风险快速增加。

超过：

95。

系统强烈建议：

休息。

---

# 13. Recovery

恢复方式：

Passive

↓

Recovery Training

↓

Massage

↓

Physio

↓

Medical Treatment

恢复速度：

不同。

费用：

不同。

---

# 14. Medical Team

未来：

支持：

普通 Physio

↓

高级 Physio

↓

ATP Medical Team

恢复速度：

提高。

费用：

提高。

---

# 15. AI Behaviour

AI：

会：

主动休息。

主动退赛。

主动治疗。

不会：

一直带伤比赛。

---

# 16. Injury History

保存：

Career Injury。

例如：

```text
2027
Back Injury
4 Weeks
Recovered
```

未来：

影响：

复发概率。

---

# 17. UI

Today：

显示：

Health

Fatigue

Recovery

Injury Risk

颜色：

绿色

黄色

橙色

红色

---

# 18. Data Model

```text
Injury
PlayerID
Type
Severity
Week
RecoveryWeeks
Status
MedicalPlan
Risk
```

---

# 19. Edge Cases

支持：

- Match Injury
- Training Injury
- Illness
- Withdrawal
- Retirement
- Recurring Injury
- Recovery Interrupted

---

# 20. Acceptance Criteria

✓ Fatigue 正常累计

✓ Recovery 正常恢复

✓ AI 正常受伤

✓ 不会无限受伤

✓ 不会永远健康

✓ 长期 Career 稳定运行

---

End of Document
