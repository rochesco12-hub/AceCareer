# Ace Career Gameplay Bible
# 09 · Coach Gameplay

Version: 1.0
Status: Draft
Priority: P1

---

# Overview

Coach Gameplay 定义教练团队在整个 Career 中的玩法。

教练不是一个：

+5% Serve

+10% Recovery

这样的 Buff 系统。

现实职业网球中。

优秀教练真正提供的是：

- 职业规划
- 战术分析
- 心理支持
- 训练安排
- 比赛建议
- 长期成长

Ace Career 的教练应该成为：

玩家整个职业生涯最重要的伙伴。

---

# Design Goal

Coach Gameplay 必须做到：

① 教练主动提供建议

② 教练拥有不同执教风格

③ 玩家建立长期合作关系

④ 教练真正影响职业生涯

玩家不会因为 Buff。

记住教练。

而会因为：

"他陪我从 ITF 打到了 Grand Slam。"

---

# Design Philosophy

现实职业球员。

不会每天打开：

教练菜单。

而是：

教练主动帮助球员。

因此：

Coach Gameplay 是：

主动系统。

不是：

玩家主动管理系统。

---

# Coach Gameplay Loop

完整循环：

```text
Career Review
↓
Coach Analysis
↓
Coach Recommendation
↓
Player Decision
↓
Tournament
↓
Coach Feedback
↓
Relationship Growth
```

整个职业生涯持续循环。

---

# Coach Relationship

每位教练拥有：

Relationship。

范围：

```text
0 ~ 100
```

长期合作。

共同赢得冠军。

关系提高。

频繁解约。

关系下降。

关系：

影响建议可信度。

未来：

影响成长效率。

---

# Coach Personality

每位教练都有：

执教风格。

例如：

Aggressive

Balanced

Technical

Fitness

Mental

Young Talent

Veteran

不同风格。

推荐内容不同。

---

# Aggressive Coach

例如：

```text
Current Ranking
31
Recommendation
Play ATP500.
Take The Risk.
```

更倾向：

挑战高等级赛事。

---

# Balanced Coach

例如：

```text
Fatigue
72
Recommendation
Recovery Week.
Prepare For Wimbledon.
```

更加稳定。

长期规划。

---

# Young Talent Coach

更关注：

成长。

例如：

```text
Skip ATP250.
Focus On Training.
Long-term Improvement Matters.
```

---

# Veteran Coach

更关注：

职业寿命。

例如：

```text
Do Not Rush Back.
Your Career Is More Important.
```

---

# Weekly Coach Report

每进入一周。

Today 自动出现：

Coach Card。

例如：

```text
Coach Report
This week's priority:
Recovery.
Confidence
High
```

玩家：

无需打开教练界面。

---

# Tournament Recommendation

每周。

教练分析：

所有赛事。

例如：

```text
Rome Masters
Expected Result
Round3
Probability
68%
Recommended
★★★★☆
```

Phoenix Challenger：

```text
Champion Chance
42%
Recommended
★★★☆☆
```

帮助玩家：

职业规划。

---

# Training Recommendation

训练周。

自动分析。

例如：

```text
Your Serve
Has Stopped Improving.
Recommend
Serve Block ×2
```

或者：

```text
Strength Is Overtrained.
Switch To Recovery.
```

---

# Match Preparation

比赛日前。

Coach 自动生成：

Opponent Report。

例如：

```text
Opponent
Jannik Sinner
Strength
Baseline
Weakness
Second Serve
Recommendation
Attack Early.
```

增加：

职业氛围。

---

# Between Matches

比赛结束。

Coach：

自动点评。

例如：

```text
Excellent Win.
Recovery Tomorrow.
Do Not Train.
```

或者：

```text
Long Match.
Energy Is Low.
Recovery Strongly Recommended.
```

---

# Long-Term Goals

教练帮助制定：

职业目标。

例如：

```text
Current Goal
Top20
Expected
12 Weeks
```

完成以后。

自动更新。

Top10。

Grand Slam。

No.1。

---

# Coach Meeting

每隔：

4~6 周。

自动触发：

Coach Meeting。

例如：

```text
Season Review
Progress
Excellent
Need More Physical Training
```

整个职业规划。

重新调整。

---

# Conflict

玩家长期忽略建议。

教练会主动提醒。

例如：

```text
You Have Ignored
Recovery Advice
Three Weeks In A Row.
```

不是惩罚。

只是职业互动。

---

# Career Milestones

重大节点。

教练一定出现。

例如：

首次冠军。

首次Top100。

首次Grand Slam。

首次世界第一。

退役。

这些时刻。

教练给予评价。

增强情感连接。

---

# Coach Evolution

教练不会永远一样。

长期合作。

关系变化。

执教理念变化。

甚至：

年龄增长。

退休。

玩家需要：

寻找下一位教练。

---

# Hiring A Coach

更换教练。

不是：

能力最高。

而是：

是否适合。

例如：

红土赛季。

寻找：

Clay Specialist。

草地赛季。

寻找：

Serve Coach。

形成：

职业策略。

---

# AI Coaches

AI 球员。

同样拥有：

教练。

AI：

也会：

更换教练。

续约。

退休。

整个世界：

一致。

---

# Coach History

Career 自动记录：

例如：

```text
Head Coach
2026-2034
8 Years
Grand Slams
3
Titles
28
```

退役后。

Career Timeline。

仍然可以查看。

---

# Emotional Curve

教练玩法：

应该形成：

```text
建议
↓
思考
↓
比赛
↓
反馈
↓
成长
↓
信任
```

教练越来越像：

真正的团队。

而不是：

属性卡。

---

# UX Rules

Today：

只显示：

一条建议。

不要：

长篇文字。

点击以后。

展开完整分析。

所有 Coach 内容。

默认：

轻量。

---

# Success Metrics

Coach Gameplay 完成以后。

玩家应该：

开始记住：

自己的教练。

相信教练。

甚至：

纠结是否更换教练。

如果玩家会说：

"这位教练陪我拿到了第一个 Grand Slam。"

那么：

Coach Gameplay 就成功了。

---

# Definition of Done

✓ 教练主动提供建议

✓ 不同教练拥有不同风格

✓ 长期合作建立关系

✓ 教练影响职业规划

✓ 教练参与比赛与训练

✓ AI 使用同一系统

✓ 教练成为 Career 的重要角色

Coach 不是 Buff。

Coach 是职业生涯中最重要的伙伴。

---

End of Document
