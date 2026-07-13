# Ace Career Game Design Document
## Player Progression System

Version: 1.0
Status: Draft
Priority: P1

---

# 1. Purpose

Player Progression System（球员成长系统）负责模拟职业球员整个职业生涯的成长过程。

它决定：

- 能力成长
- 巅峰形成
- 年龄衰退
- 球风塑造
- 天赋兑现

Training System 负责"训练什么"。

Progression System 负责"最终成长成什么样的球员"。

---

# 2. Design Goal

成长系统必须满足：

- 不存在无限成长
- 每位球员成长轨迹不同
- 天赋决定上限
- 训练决定兑现程度
- 年龄决定成长阶段
- AI 与玩家完全一致

---

# 3. Career Progression Pipeline

```text
Training
↓
Match Experience
↓
Confidence
↓
Growth Calculation
↓
Attribute Progress
↓
Age Modifier
↓
Potential Modifier
↓
Update Overall Rating
```

成长不是一次完成。

而是长期累积。

---

# 4. Career Stages

所有球员都会经历：

```text
Junior
↓
Prospect
↓
Developing
↓
Prime
↓
Veteran
↓
Decline
↓
Retirement
```

不同阶段：

成长速度不同。

---

# 5. Age Curve

默认成长曲线：

| 年龄 | 阶段 |
|------|------|
| 16-18 | 快速成长 |
| 19-22 | 高速成长 |
| 23-28 | 巅峰 |
| 29-32 | 稳定 |
| 33-36 | 缓慢下降 |
| 37+ | 明显下降 |

未来支持：

Late Bloomer。

---

# 6. Potential

每位球员拥有：

Potential。

范围：

```text
40~99
```

Potential：

决定理论最高能力。

训练：

决定最终是否达到。

---

# 7. Current Ability

Current Ability：

简称：

CA。

代表：

当前真实实力。

CA 永远：

≤ Potential。

---

# 8. Growth Speed

成长速度来源：

- 年龄
- 教练
- 训练质量
- 比赛数量
- Confidence
- Injury
- Talent

不是：

固定成长。

---

# 9. Match Experience

正式比赛：

提供：

Experience。

Grand Slam：

成长更多。

ITF：

成长较少。

长期比赛：

促进成长。

---

# 10. Attribute Groups

能力分组：

Technical

Physical

Mental

Serve

Return

Movement

Experience

每组：

独立成长。

---

# 11. Hidden Attributes

隐藏属性：

Work Ethic

Professionalism

Consistency

Big Match

Injury Proneness

Learning Ability

玩家默认不可见。

未来：

球探系统。

可逐渐发现。

---

# 12. Peak Years

巅峰：

不是固定年龄。

系统根据：

训练。

比赛。

伤病。

自动决定。

例如：

球员A：

24~29。

球员B：

27~32。

---

# 13. Decline

Decline：

逐步发生。

不会：

突然：

Overall

95

↓

82。

能力：

缓慢下降。

经验：

继续增长。

---

# 14. Experience

Experience：

永久成长。

不会下降。

影响：

关键分。

压力。

比赛阅读能力。

老将：

虽然速度下降。

经验：

更丰富。

---

# 15. Playing Style

成长过程中：

逐渐形成：

Aggressive Baseliner

Counter Puncher

Serve Bot

All Court

Net Player

Clay Specialist

Grass Specialist

不同风格：

影响：

Match AI。

---

# 16. AI Growth

AI：

使用：

同一成长算法。

不会：

作弊成长。

不会：

固定 Overall。

---

# 17. Progress Report

每月：

生成：

成长报告。

例如：

```text
Forehand
+2
Serve
+1
Speed
+0
Confidence
+4
```

帮助玩家了解成长。

---

# 18. Data Model

```text
PlayerProgression
PlayerID
CurrentAbility
Potential
Age
CareerStage
GrowthRate
Experience
PlayingStyle
HiddenAttributes
```

---

# 19. Edge Cases

支持：

- 长期伤病影响成长
- 提前退役
- 天才球员
- 大器晚成
- 低天赋高努力
- 连续多年低迷

---

# 20. Acceptance Criteria

✓ 每位球员成长曲线不同

✓ AI 与玩家一致

✓ 年龄影响成长

✓ 巅峰自然形成

✓ 能力不会无限增长

✓ 支持长期 Career

---

End of Document
