# Ace Career Game Design Document
## Player Decision System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Player Decision System（玩家决策系统）定义玩家在整个职业生涯中可以做出的所有决策。

Ace Career 的核心玩法不是不停点击"下一周"。

而是：

> 每一周都做出职业球员真正需要做出的决定。

所有系统最终都汇聚到 Player Decision。

---

# 2. Design Goal

玩家打开 Today 页面后，必须能够立即回答：

- 我这周应该去哪站？
- 我要不要训练？
- 我要不要休息？
- 我要不要带伤参赛？
- 我要不要冲排名？
- 我要不要放弃这站准备下一站？

玩家每周都必须拥有真正有意义的选择。

---

# 3. Decision Philosophy

玩家不能：

被迫执行唯一正确答案。

例如：

Week18

只有：

Monastir M15

↓

点击报名

↓

下一周

这种设计失败。

系统必须保证：

每周至少拥有：

3~5 个合理选择。

---

# 4. Weekly Decision Pipeline

进入新 Week：

```text
World Update
↓
Ranking Update
↓
News
↓
Health Update
↓
Tournament Recommendation
↓
Player Decision
↓
Simulation
↓
Week End
```

玩家决策：

永远发生在世界更新之后。

---

# 5. Weekly Decisions

玩家每周可以：

- 报名赛事
- 安排训练
- 安排恢复
- 查看赛历
- 查看排名
- 查看新闻
- 调整团队
- 管理资金
- 跳过本周

并不是每周都必须比赛。

---

# 6. Tournament Decision

玩家拥有多个候选赛事。

例如：

```text
Monastir M15
预计夺冠概率
42%
预计积分
15
预计奖金
$2,100
--------------
Antalya M15
预计夺冠概率
36%
预计积分
15
预计奖金
$2,300
--------------
Koblenz Challenger
预计晋级第二轮
41%
预计积分
25
预计奖金
$5,500
```

系统：

推荐。

不替玩家决定。

---

# 7. Training Decision

若：

本周没有比赛。

玩家可安排：

技术训练

力量训练

速度训练

耐力训练

恢复训练

心理训练

不同训练：

影响：

成长。

疲劳。

伤病风险。

---

# 8. Recovery Decision

Recovery：

不是自动行为。

玩家需要选择：

完全休息

↓

理疗

↓

按摩

↓

主动恢复

↓

恢复训练

不同方案：

恢复速度不同。

费用不同。

---

# 9. Medical Decision

Minor Injury：

玩家可以：

继续比赛

↓

退出赛事

↓

恢复

Major Injury：

建议：

停止比赛。

系统：

给出风险评估。

最终：

玩家决定。

---

# 10. Career Goal

玩家可以设定：

赛季目标。

例如：

进入 Top100

↓

赢 Challenger

↓

打进 ATP

↓

Grand Slam 正赛

AI：

根据目标。

推荐赛事。

---

# 11. Coach Recommendation

教练：

主动提出建议。

例如：

```text
建议：
本周休息。
疲劳已经达到82。
继续参赛。
受伤风险提升43%。
```

玩家：

可采纳。

也可忽略。

---

# 12. Financial Decision

玩家：

决定：

是否：

雇佣：

更好的教练。

是否：

乘坐经济舱。

是否：

入住高级酒店。

是否：

聘请理疗师。

这些都会影响：

恢复。

疲劳。

现金流。

---

# 13. Schedule Decision

玩家：

可提前查看：

未来：

4 周。

例如：

```text
Week19
Rome Challenger
Week20
休息
Week21
Roland Garros Qualification
```

帮助：

规划赛季。

---

# 14. Risk Decision

系统：

显示：

每项选择风险。

例如：

继续比赛：

```text
伤病风险
+18%
疲劳
+12
奖金预期
+$6,000
```

休息：

```text
恢复
+35
伤病风险
-22%
收入
0
```

最终：

玩家承担选择结果。

---

# 15. Recommendation Engine

Today 页面：

自动推荐：

本周最佳方案。

例如：

```text
推荐：
参加 Challenger50。
理由：
预计可获得：
58 ATP Points。
预计世界排名：
提升12位。
```

Recommendation：

不是：

自动执行。

只是：

建议。

---

# 16. Decision History

系统保存：

所有重大决定。

例如：

2027

Week18

放弃 ATP250

↓

选择 Challenger

↓

最终夺冠。

未来：

Career Summary：

引用。

---

# 17. Quick Actions

Today 页面：

最多显示：

4 个按钮。

例如：

Week Mode：

继续下一周

报名赛事

安排训练

查看赛历

Tournament Mode：

开始比赛

恢复

训练

查看签表

按钮：

必须动态变化。

---

# 18. Data Model

```text
PlayerDecision
DecisionID
Season
Week
Category
Choice
Reason
CreatedAt
```

Decision Category：

```text
Tournament
Training
Recovery
Medical
Finance
Coach
Travel
```

---

# 19. Edge Cases

支持：

- 带伤参赛
- 放弃报名
- 连续休息
- 连续比赛
- 临时 Withdrawal
- Recovery 中报名
- 教练建议冲突
- 资金不足

---

# 20. Acceptance Criteria

完成后：

✓ 每周至少拥有多个决策

✓ Today 页面不超过4个主要操作

✓ Recommendation Engine 正常工作

✓ 玩家拥有完全自由选择

✓ AI 不替玩家做决定

✓ 所有决定进入 Career History

✓ 决策影响整个职业生涯

✓ 支持长期 Career

---

End of Document
