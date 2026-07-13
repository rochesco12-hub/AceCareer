# Ace Career Game Design Document
## Coach & Support Team System

Version: 1.0
Status: Draft
Priority: P1

---

# 1. Purpose

Coach & Support Team System（教练团队系统）负责模拟职业网球运动员背后的整个团队。

职业球员的成长不仅来自训练，更来自团队的长期支持。

团队建设将成为 Career Mode 的长期经营玩法。

---

# 2. Design Goal

团队系统必须满足：

- 每位球员拥有完整团队
- 团队影响训练、比赛、恢复
- 不同团队拥有不同特点
- AI 同样拥有团队
- 长期培养，而不是频繁更换

---

# 3. Team Structure

每位球员最多拥有：

Head Coach

Fitness Coach

Physio

Sports Psychologist

Nutritionist（Future）

Analyst（Future）

不同职位负责不同系统。

---

# 4. Head Coach

负责：

- 技术成长
- 战术建议
- 比赛策略
- 赛季规划

能力值：

Serve Coaching

Groundstroke

Volley

Tactics

Development

Leadership

Experience

---

# 5. Fitness Coach

负责：

- 力量训练
- 爆发力
- 速度
- 耐力
- 敏捷

效果：

提升训练效率。

降低疲劳。

---

# 6. Physio

负责：

- 恢复
- 按摩
- 理疗
- 伤病恢复

影响：

Recovery Speed

Injury Risk

Medical Cost

---

# 7. Sports Psychologist

负责：

- Confidence
- Pressure Resistance
- Focus
- Comeback Ability

大满贯期间效果明显。

---

# 8. Coach Level

所有教练拥有：

Level

1~10

等级越高：

费用越高。

效果越明显。

---

# 9. Coach Personality

教练拥有不同风格。

例如：

Aggressive

Balanced

Technical

Fitness

Young Talent

Veteran

人格影响：

推荐训练。

推荐赛事。

---

# 10. Coach Contract

每位教练拥有：

Contract：

Week

Salary

Bonus

Contract End

到期：

可：

续约。

更换。

---

# 11. Coach Relationship

新增：

Relationship。

范围：

0~100。

长期合作：

关系提高。

频繁解约：

关系下降。

未来：

影响：

训练效率。

---

# 12. Coach Recommendation

每周：

教练自动提出建议。

例如：

建议：

参加 Challenger。

预计夺冠概率：

41%。

建议：

休息。

当前疲劳：

83。

建议：

加强发球训练。

玩家：

可采纳。

也可忽略。

---

# 13. Team Synergy

团队拥有：

协同效果。

例如：

Head Coach

+

Fitness Coach

长期合作。

训练效率：

+8%。

未来：

支持：

传奇团队。

---

# 14. Hiring

玩家可：

雇佣。

解雇。

升级。

筛选：

教练。

筛选条件：

国家。

等级。

薪资。

专长。

---

# 15. AI Coach

AI：

自动聘请：

适合自己的团队。

AI：

也会：

更换教练。

升级团队。

不会：

永久同一个教练。

---

# 16. Financial Impact

所有团队：

拥有：

Weekly Salary。

系统：

每周自动扣费。

现金不足：

自动提醒。

---

# 17. Data Model

Coach：

```text
CoachID
Name
Nationality
Level
Serve
Fitness
Recovery
Mental
Salary
Relationship
ContractEnd
```

Team：

```text
PlayerID
HeadCoachID
FitnessCoachID
PhysioID
PsychologistID
```

---

# 18. Edge Cases

支持：

- 教练退休
- 合同到期
- 解约
- 薪资不足
- AI 更换教练
- 团队全部解散

---

# 19. Acceptance Criteria

✓ 玩家拥有完整团队

✓ AI 拥有团队

✓ 团队影响成长

✓ 每周自动结算薪资

✓ 教练提供建议

✓ 长期 Career 稳定运行

---

End of Document
