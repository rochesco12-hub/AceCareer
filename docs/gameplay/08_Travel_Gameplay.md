# Ace Career Gameplay Bible
# 08 · Travel Gameplay

Version: 1.0
Status: Draft
Priority: P1

---

# Overview

Travel Gameplay 定义职业球员在世界各地参加巡回赛时的完整旅行体验。

旅行不是一个 Loading。

也不是：

Barcelona

↓

Rome

↓

Done

旅行应该成为职业生涯规划的一部分。

因为现实 ATP 球员真正消耗体能的，并不仅仅是比赛。

还有：

- 飞行
- 倒时差
- 换场地
- 换国家
- 换气候
- 连续跨洲旅行

Ace Career 应该让玩家真正开始思考：

"下一站，我到底该不该去。"

---

# Design Goal

Travel Gameplay 必须满足：

① 世界巡回赛真正具有"巡回"感

② 不同地区拥有不同成本

③ 旅行影响比赛表现

④ 玩家开始规划整个赛季路线

旅行不是惩罚。

旅行是职业规划。

---

# Design Philosophy

现实 ATP 球员：

不是哪里有比赛就去哪。

他们会考虑：

积分。

奖金。

路程。

时差。

场地。

恢复。

下一站。

真正优秀的球员。

规划的是：

连续六周。

不是下一场比赛。

---

# Travel Loop

完整旅行流程：

```text
Choose Tournament
↓
Estimate Travel
↓
Book Trip
↓
Travel
↓
Arrive
↓
Adapt
↓
Tournament Begins
```

整个流程。

发生在 Week 内。

---

# Travel Preview

报名赛事之前。

系统自动展示：

旅行成本。

例如：

```text
Travel
Rome
↓
Madrid
Distance
1,360 km
Flight Time
2h 25m
Travel Fatigue
+4
Cost
$420
```

另一站：

```text
Rome
↓
Tokyo
Flight Time
13h
Travel Fatigue
+18
Jet Lag
High
Cost
$2,200
```

玩家开始真正比较。

---

# Regional Tours

整个 ATP Calendar。

天然形成：

巡回赛。

例如：

```text
Australian Swing
↓
Middle East Swing
↓
Sunshine Double
↓
Clay Season
↓
Grass Season
↓
North America
↓
Asia Swing
↓
Indoor Season
```

如果一直按照巡回赛参加。

旅行成本最低。

恢复最好。

---

# Breaking The Route

如果玩家：

为了奖金。

突然：

```text
Madrid
↓
Miami
↓
Rome
```

系统提示：

```text
Travel Load
Very High
Recommended
Stay In Europe
```

玩家依然可以选择。

承担代价。

---

# Travel Fatigue

旅行会增加：

Fatigue。

例如：

| 类型 | Fatigue |
|------|---------:|
| 同国家 | +1 |
| 欧洲境内 | +3 |
| 跨洲 | +10 |
| 长途跨洲 | +15~20 |

不是：

比赛才累。

旅行也会累。

---

# Jet Lag

跨洲旅行。

自动产生：

Jet Lag。

例如：

```text
Jet Lag
Moderate
Estimated Recovery
2 Days
```

影响：

Reaction。

Focus。

Confidence。

不会永久存在。

---

# Climate Adaptation

不同地区。

拥有不同环境。

例如：

澳洲：

高温。

北美：

硬地高速。

欧洲：

红土。

亚洲：

湿热。

初到新地区。

需要：

Adapt。

长期停留。

状态恢复。

---

# Arrival Phase

到达赛事城市。

Today 页面自动变化。

例如：

```text
Arrived
Rome
Adaptation
75%
Tournament Starts
Tomorrow
```

不是：

瞬间开始比赛。

---

# Early Arrival

玩家可以：

提前一周到达。

例如：

法网前。

提前抵达巴黎。

优势：

适应更充分。

Fatigue 更低。

Confidence 更高。

代价：

住宿费用增加。

---

# Late Arrival

也可以：

最后一天飞过去。

优势：

节约费用。

减少住宿。

劣势：

Jet Lag。

Fatigue。

第一轮容易发挥不好。

不存在最佳方案。

---

# Accommodation

旅行期间。

玩家选择：

酒店等级。

例如：

```text
Standard Hotel
$120
Recovery
+2
Luxury Hotel
$350
Recovery
+8
```

未来：

配合 Economy。

---

# Practice Before Tournament

抵达以后。

允许：

一次适应训练。

例如：

```text
Clay Adaptation
Serve Practice
Recovery
```

不是成长。

而是：

适应环境。

---

# Coach Suggestion

教练根据赛程。

提出建议。

例如：

```text
Coach
Too Much Travel.
Skip This Tournament.
```

或者：

```text
Stay One More Week.
Prepare For Wimbledon.
```

形成职业规划。

---

# Long Trip Penalty

连续跨洲。

系统自动提示：

```text
Travel Load
Critical
Fatigue
83
Injury Risk
+12%
```

玩家开始理解：

赛程规划的重要性。

---

# Home Tournament

来到自己国家。

获得：

Home Bonus。

例如：

```text
Home Crowd
Confidence
+4
```

不是能力提升。

而是心理优势。

---

# Travel Stories

旅行过程中。

自动生成新闻。

例如：

```text
Long Journey To Tokyo
Can Logan Recover In Time?
```

增加职业氛围。

---

# Travel Calendar

Today 可以查看：

未来四周。

例如：

```text
Week18
Rome
↓
Week19
Madrid
↓
Week20
Paris
↓
Week21
Rest
```

真正开始：

规划赛季。

---

# Travel Summary

赛事结束。

自动生成：

```text
Trip Summary
Travel Cost
$2,340
Travel Fatigue
+18
Countries
3
Flights
2
```

帮助玩家：

理解职业巡回。

---

# Emotional Curve

旅行玩法：

应该形成：

```text
规划
↓
启程
↓
抵达
↓
适应
↓
比赛
↓
离开
↓
下一站
```

玩家真正体验：

巡回赛。

---

# UX Rules

Travel：

默认：

自动完成。

只有重要选择。

需要玩家决定。

不会：

要求玩家：

订机票。

选航班。

微管理。

所有复杂内容。

自动处理。

---

# Success Metrics

Travel Gameplay 完成以后。

玩家应该：

开始规划：

整个赛季路线。

为了减少旅行。

主动放弃某些赛事。

而不是：

哪里都报名。

如果玩家开始说：

"法网后我就在欧洲继续打草地。"

那么：

Travel Gameplay 就成功了。

---

# Definition of Done

✓ Travel 成为职业规划的一部分

✓ 不同地区旅行成本不同

✓ Travel Fatigue 合理增加

✓ Jet Lag 影响比赛

✓ Arrival 具有适应阶段

✓ 玩家主动规划巡回路线

✓ 教练提供旅行建议

✓ Travel 与 Tournament 无缝连接

Travel 不是地图切换。

Travel 是职业网球巡回赛真正的开始。

---

End of Document
