# Ace Career Bible
## Chapter 01 · ATP Calendar System

Version: 1.0
Status: Design Draft
Priority: P0

---

# 1. Purpose

ATP Calendar 是 Ace Career 最重要的底层系统。

它不是日期系统。

它是整个游戏世界的时间引擎（World Timeline Engine）。

所有系统都只能依赖 Calendar 推进时间。

禁止任何系统自行推进时间。

例如：

错误：

Training 完成以后自己推进一天。

正确：

Training 请求 Calendar。

Calendar 决定是否推进时间。

因此：

Calendar 是整个 Career 唯一合法的时间来源（Single Source of Truth）。

---

# 2. Calendar Responsibilities

Calendar 负责：

- Season
- Week
- Tournament Window
- World Update
- Ranking Update
- AI Update
- News Update
- Player Schedule
- Tournament Timeline

Calendar 不负责：

- Match Simulation
- Training Calculation
- Injury Calculation
- Ranking Calculation
- Economy Calculation

这些系统只能监听 Calendar。

---

# 3. Core Philosophy

Calendar 必须遵循以下原则。

---

### Rule 01

世界不会等待玩家。

玩家离线。

世界继续运行。

所有 AI：

继续：

- 报名
- 比赛
- 排名
- 受伤
- 恢复
- 退役

玩家只是世界中的一个职业球员。

不是世界中心。

---

### Rule 02

Week 是唯一主要时间单位。

玩家看到的是：

2026 Season

Week 18

而不是：

2026-05-14 Thursday

日期属于辅助信息。

Week 才是主要信息。

---

### Rule 03

真正推进的是事件。

不是日期。

例如：

Week 12

↓

报名截止

↓

抽签

↓

第一轮

↓

第二轮

↓

四强

↓

决赛

↓

冠军

而不是：

Monday

↓

Tuesday

↓

Wednesday

↓

Thursday

玩家不需要感知每天。

玩家需要感知职业生涯。

---

### Rule 04

Calendar 永远领先其它系统。

推进顺序必须固定。

Calendar

↓

Tournament

↓

Training

↓

Injury

↓

Ranking

↓

Media

↓

Save

任何系统不得改变执行顺序。

---

# 4. Season Structure

每一个 Career 包含无限多个 Season。

例如：

2026

↓

2027

↓

2028

↓

……

Season 没有理论上限。

玩家可以：

连续进行：

20+

30+

40+

赛季。

Season 保存：

- 年度冠军
- 年终世界第一
- Race 冠军
- 大满贯冠军
- ATP Finals 冠军
- Hall of Fame 数据
- 历史新闻

Season 永不删除。

---

# 5. Week Structure

一年固定：

52 Week。

Week 是整个游戏运行单位。

Week 保存：

```text
Week Number

Season

Open Tournaments

Closed Tournaments

Ranking Update

Player Schedule

AI Schedule

World News

Surface

Region
```

Week 生命周期：

```text
Week Start

↓

World Update

↓

Player Decision

↓

AI Decision

↓

Tournament Update

↓

Match Update

↓

Ranking Update

↓

News Update

↓

Auto Save

↓

Week End
```

任何 Week 都必须按照这一顺序执行。

不得跳过。

不得插队。

---

# 6. Week Types

Calendar 定义六种 Week。

### Tournament Week

存在正式赛事。

例如：

ATP250

Challenger

ITF

允许：

报名

比赛

恢复

新闻

积分

---

### Training Week

没有重要赛事。

系统建议：

训练

恢复

能力成长

不会自动安排比赛。

---

### Recovery Week

玩家连续参赛。

系统建议：

完全休息。

恢复速度增加。

伤病风险降低。

AI 同样遵守。

---

### Transition Week

用于：

跨洲旅行。

例如：

欧洲

↓

北美

系统自动增加旅行疲劳。

调整时差。

旅行结束后：

恢复正常状态。

---

### Off Season

赛季结束。

没有 ATP 巡回赛。

允许：

更换教练

更换装备

体能储备

长期训练

恢复旧伤

制定新赛季目标

---

### Special Week

特殊赛事：

Olympics

Davis Cup

Laver Cup（预留）

ATP Finals

拥有独立规则。

不影响普通巡回赛逻辑。

---

# 7. Week Update Pipeline

Week 每次推进。

严格按照以下 Pipeline。

Step 1

更新世界时间。

↓

Step 2

检查所有赛事状态。

↓

Step 3

关闭报名。

↓

Step 4

生成 Acceptance List。

↓

Step 5

生成 Draw。

↓

Step 6

AI 安排赛程。

↓

Step 7

玩家收到通知。

↓

Step 8

更新新闻。

↓

Step 9

更新排名。

↓

Step 10

自动保存。

任何模块不得修改 Pipeline。

---

# 8. Calendar State

Calendar 只有以下状态。

```text
PRE_SEASON

REGULAR_SEASON

TOURNAMENT_WEEK

OFF_SEASON

SPECIAL_EVENT
```

所有系统根据 CalendarState 判断自身行为。

例如：

TOURNAMENT_WEEK：

禁止高强度训练。

OFF_SEASON：

允许高强度训练。

SPECIAL_EVENT：

读取特殊赛事规则。

---

# 9. World Update

每进入新 Week。

世界自动执行：

- AI 报名
- AI 训练
- AI 比赛
- AI 恢复
- AI 排名
- AI 新闻
- AI 伤病
- AI 退役
- AI 新秀生成（达到对应时间）

世界更新必须在玩家行动之前完成。

保证玩家看到的是最新世界状态。

---

# 10. Player Update

玩家进入新 Week 后：

依次获得：

- 最新排名
- 最新新闻
- 本周赛事
- 推荐赛事
- 身体状态
- 本周计划建议

然后才允许玩家做决策。

玩家不能先报名，再更新世界。

顺序固定。

---

# 11. Tournament Windows

Tournament Window 定义赛事在 Calendar 中何时出现、何时开放报名、何时开始、何时结束。

每一站赛事都必须拥有完整生命周期。

生命周期如下：

```text
Planning
↓
Created
↓
Entry Open
↓
Entry Closed
↓
Acceptance List
↓
Draw Released
↓
Tournament Active
↓
Completed
↓
Archived
```

每一个阶段都有严格触发条件。

不得跳跃。

---

### Planning

赛事已存在于赛历。

但玩家不可报名。

作用：

- 提前显示未来赛程
- 玩家制定长期计划
- AI 开始规划赛程

UI：

未来赛事

距离开始：

8 周

状态：

Coming Soon

---

### Created

赛事正式创建。

系统生成：

- Tournament ID
- 城市
- 场地
- Surface
- Prize Money
- ATP Points
- Draw Size
- Qualification Size

AI 可以开始评估是否参加。

玩家仍不能报名。

---

### Entry Open

开放报名。

允许：

玩家报名。

AI 报名。

系统开始维护：

Entry List。

默认开放时间：

提前 3~4 周。

例如：

Week 12 ATP250

Week 8 开放报名。

---

### Entry Closed

报名结束。

禁止：

新增报名。

允许：

Withdrawal。

系统开始计算：

Acceptance List。

---

### Acceptance List

根据：

排名。

Protected Ranking。

Wild Card。

Special Exempt。

Qualification。

最终确定：

正赛名单。

等待名单。

资格赛名单。

Acceptance List 一旦生成。

不可修改。

除非：

Withdrawal。

---

### Draw Released

系统抽签。

生成：

Bracket。

Seed。

Bye。

Qualifier。

Lucky Loser 位置。

抽签完成后：

正式进入 Tournament Mode。

---

### Tournament Active

赛事正式开始。

Calendar 将控制：

Round 1

↓

Round 2

↓

Quarterfinal

↓

Semifinal

↓

Final

期间：

禁止报名其它正式赛事。

---

### Completed

比赛全部结束。

系统结算：

冠军。

奖金。

ATP积分。

排名变化。

新闻。

统计。

历史。

---

### Archived

赛事归档。

进入：

History Database。

永久保存：

冠军。

亚军。

比分。

奖金。

积分。

新闻。

之后：

不可修改。

---

# 12. Surface Rotation

Surface 对整个赛季影响巨大。

系统必须模拟真实 ATP Surface。

Surface 包括：

Hard

Clay

Grass

Indoor Hard

未来可扩展：

Carpet。

---

### Surface Seasons

Australian Swing

Hard

↓

Sunshine Double

Hard

↓

Clay Season

Clay

↓

Grass Season

Grass

↓

North America

Hard

↓

Asia

Hard

↓

Indoor

Indoor Hard

玩家需要：

适应：

不同 Surface。

AI 同样适应。

---

### Surface Effects

Surface 影响：

发球。

移动。

耐力。

比赛节奏。

恢复。

不同球风：

拥有不同收益。

例如：

Serve Bot。

Grass 更强。

Topspin。

Clay 更强。

---

### Surface Transition

连续切换 Surface。

增加：

适应成本。

例如：

Clay

↓

Grass

训练效率下降。

恢复速度下降。

AI 同样遵守。

---

# 13. Travel System

旅行不是动画。

而是：

Calendar 行为。

玩家参加：

欧洲赛事。

↓

北美赛事。

系统自动：

增加：

Travel Fatigue。

减少：

Recovery。

跨洲旅行：

默认：

1~3 天。

Week Mode 自动处理。

玩家无需每天点击。

---

### Long Distance Travel

例如：

Rome

↓

Toronto

系统：

自动：

Travel Week。

期间：

禁止：

高强度训练。

推荐：

恢复。

---

# 14. Ranking Update Timing

ATP 排名：

每周更新一次。

默认：

Week Start。

赛事结束：

立即计算：

预测排名。

正式排名：

Week Start 更新。

保持：

真实 ATP 节奏。

---

# 15. News Timing

每进入新 Week。

新闻系统：

自动生成：

上一周：

冠军。

冷门。

伤病。

退赛。

排名变化。

新秀表现。

玩家只有成绩足够重要。

才会上头条。

新闻不会围绕玩家生成。

---

# 16. Calendar Events

Calendar 支持以下事件：

Entry Open

Entry Closed

Acceptance List

Draw

Travel

Practice

Match

Recovery

Ranking Update

News Update

Tournament End

Season End

Off Season

所有系统监听这些 Event。

禁止自行创建时间事件。

---

# 17. UI Rules

Today 首页：

固定显示：

2026 Season

Week 18

本周重点：

ATP250 Doha

还有：

2 天报名截止。

Quick Actions：

继续下一周

报名赛事

安排训练

查看赛历

Week 永远比具体日期更醒目。

日期仅作为辅助信息。

---

# 18. Edge Cases

Calendar 必须处理：

- Withdrawal
- Retirement
- Walkover
- Rain Delay（预留）
- Protected Ranking
- Wild Card
- Lucky Loser
- Olympics
- Davis Cup
- ATP Finals
- Injury Before Match
- Injury During Tournament
- Tournament Cancelled（预留）

任何特殊情况。

不得破坏 Week Pipeline。

---

# 19. Acceptance Criteria

Calendar 完成后必须满足：

✓ 世界始终运行

✓ AI 不依赖玩家

✓ 每周都有赛事

✓ 比赛自动进入 Tournament Mode

✓ 赛事结束自动回到 Week Mode

✓ 排名固定每周更新

✓ 新闻固定每周更新

✓ Surface 正常轮换

✓ Travel 正常产生疲劳

✓ Calendar 可以稳定运行 20+ Season

---

End of Document
