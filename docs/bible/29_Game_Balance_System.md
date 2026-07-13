# Ace Career Game Design Document
## Global Balance System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Game Balance System（游戏平衡系统）负责保证整个 Career Mode 在几十个赛季内始终保持可玩性。

它不是调整数值。

而是控制整个职业网球世界的发展速度。

包括：

- 球员成长
- AI 强度
- 奖金
- 积分
- 伤病
- 新秀
- 年龄
- 排名
- 比赛数量

所有系统最终都必须受到 Balance System 控制。

---

# 2. Design Goal

Balance System 必须保证：

- 不存在唯一最优玩法
- 所有打法都能成功
- AI 与玩家长期公平
- 世界不会数值崩坏
- Career 可持续运行 50+ Season

---

# 3. Core Philosophy

Ace Career 的目标不是：

让玩家越来越强。

而是：

让整个世界始终保持竞争。

随着玩家成长：

AI 也在成长。

新秀不断出现。

传奇不断退役。

世界始终维持动态平衡。

---

# 4. Balance Layers

平衡分为五层：

```text
Player Balance
↓
AI Balance
↓
Tournament Balance
↓
Economy Balance
↓
World Balance
```

任何修改必须明确属于哪一层。

---

# 5. Player Balance

玩家成长受到：

- 年龄
- 潜力
- 训练质量
- 比赛经验
- 教练
- 伤病
- 疲劳

共同决定。

不存在无限成长。

---

# 6. AI Balance

AI 不允许作弊。

AI 与玩家使用：

完全一致：

- 成长
- 训练
- 伤病
- 恢复
- 奖金
- 排名

唯一不同：

AI 自动决策。

---

# 7. Tournament Balance

赛事收益必须合理。

例如：

ITF：

成长价值高。

奖金低。

ATP250：

奖金提高。

竞争提高。

Grand Slam：

收益最高。

风险最高。

玩家必须始终做选择。

---

# 8. Risk vs Reward

所有行为必须满足：

高收益。

高风险。

例如：

连续参加：

Grand Slam。

收益：

最高。

但：

Fatigue。

伤病。

旅行压力。

同时增加。

---

# 9. Growth Balance

成长速度：

不能固定。

例如：

18 岁。

成长快。

26 岁。

成长慢。

33 岁。

开始下降。

成长：

必须符合年龄规律。

---

# 10. Economy Balance

经济不能失控。

例如：

连续：

ITF 冠军。

不能：

拥有：

千万资产。

Top10。

奖金：

明显高于：

ITF。

收入：

符合现实。

---

# 11. Injury Balance

伤病：

不能：

太多。

也不能：

太少。

目标：

健康球员：

占：

80~90%。

Minor Injury：

10~15%。

Major Injury：

<3%。

整个 Tour：

保持真实。

---

# 12. Ranking Balance

Top10：

变化缓慢。

Top100：

持续竞争。

ITF：

快速流动。

避免：

世界第一：

每周变化。

也避免：

十年不变。

---

# 13. Rookie Balance

每年：

新秀：

约：

60~120。

其中：

真正天才：

极少。

Top10 级别：

平均：

3~5 年。

出现：

1~2 人。

---

# 14. Retirement Balance

平均退役年龄：

35~38。

伤病球员：

可能：

提前退役。

传奇：

可能：

坚持更久。

世界人口：

保持稳定。

---

# 15. Difficulty Balance

不同难度：

改变：

AI 决策质量。

不是：

直接修改：

能力值。

例如：

Hard：

AI：

赛程规划更合理。

不是：

Overall +10。

---

# 16. Long Career Balance

连续：

30 Season。

必须满足：

冠军：

不断变化。

Top100：

不断更新。

新秀：

不断成长。

传奇：

不断退役。

世界：

持续演化。

---

# 17. Balance Metrics

系统持续统计：

```text
Average Career Length
Average Injury Rate
Average Titles
Top10 Turnover
Rookie Success Rate
Tournament Participation
Average Prize Money
Ranking Distribution
```

发现异常。

自动提示开发。

---

# 18. Debug Dashboard

开发模式：

提供：

World Population

Top10 Age

Injury %

Economy

AI Strength

Rookie Count

Retirement Count

Balance Score

方便：

持续调优。

---

# 19. Acceptance Criteria

✓ 所有打法可玩

✓ AI 不作弊

✓ 世界长期稳定

✓ 经济合理

✓ 排名合理

✓ 新秀合理

✓ 伤病合理

✓ 支持 50+ Season

---

End of Document
