# Ace Career Game Design Document
## News & Media System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

News & Media System（新闻媒体系统）负责模拟整个职业网球世界的信息传播。

它不是玩家日志。

而是真正属于整个 ATP 世界的新闻网络。

玩家只是新闻中的一个角色。

不是新闻中心。

---

# 2. Design Goal

News System 必须做到：

- 世界每天（每周）都有新闻
- 新闻覆盖所有 AI 球员
- 玩家只有表现足够突出才会上新闻
- 新闻影响世界氛围，而不是影响比赛结果
- 新闻成为 Career 世界的重要组成部分

---

# 3. Design Principles

### Principle 1

新闻属于世界。

不是属于玩家。

即使玩家连续休息三周。

世界仍然每天都有新闻。

---

### Principle 2

新闻来源于数据。

新闻不能随机编造。

所有新闻必须来源于：

- 比赛结果
- 排名变化
- 伤病
- 转会（未来）
- 教练更换
- 新秀成长
- 退役
- 连胜
- 连败

AI 不允许凭空生成故事。

---

### Principle 3

重要事件优先。

Grand Slam

>

Masters1000

>

ATP500

>

ATP250

>

Challenger

>

ITF

新闻排序必须符合赛事等级。

---

# 4. News Pipeline

```text
Tournament End
↓
Statistics Update
↓
Ranking Update
↓
Career Update
↓
News Generator
↓
Headline Selection
↓
Publish
↓
Archive
```

所有新闻都必须进入：

News Archive。

永久保存。

---

# 5. News Categories

新闻分类：

```text
Tournament
Ranking
Injury
Retirement
Comeback
Winning Streak
Losing Streak
Young Talent
Upset
Milestone
Records
Transfer（Future）
Coach（Future）
```

每篇新闻必须属于一个分类。

---

# 6. Headline Priority

同一天存在多条新闻时。

系统按照：

Priority 排序。

例如：

Grand Slam 冠军

100

Masters1000 冠军

90

世界第一变化

88

重大伤病

85

ATP250 冠军

70

ITF 冠军

30

首页默认显示：

Priority 最高新闻。

---

# 7. Player Exposure

玩家不会因为赢下一场普通比赛就登上头条。

系统根据：

Media Score。

决定是否报道。

Media Score 来源：

- 赛事等级
- 对手排名
- 是否爆冷
- 是否创造纪录
- 是否首次夺冠
- 连胜
- 世界排名

Media Score 达到阈值。

自动生成新闻。

---

# 8. AI Exposure

AI 与玩家拥有相同曝光规则。

例如：

世界第一爆冷出局。

自动生成：

Breaking News。

而不是：

优先报道玩家。

---

# 9. Automatic Headlines

系统自动生成：

例如：

```text
Alcaraz wins Rome Masters.
Sinner returns to World No.1.
18-year-old Japanese talent wins first Challenger title.
Player reaches Top100 for the first time.
Draper withdraws due to injury.
Former World No.1 announces retirement.
```

所有标题：

来源于真实数据。

---

# 10. News Types

普通新闻：

灰色。

Breaking News：

红色。

Exclusive（未来）：

金色。

Historical Record：

紫色。

不同类型：

拥有不同展示方式。

---

# 11. Weekly News

每进入新 Week。

自动生成：

Weekly Report。

内容包括：

- 世界第一变化
- Top10 变化
- Race 排名
- 本周冠军
- 最大冷门
- 最佳新人
- 玩家表现

成为：

Career 世界周报。

---

# 12. Tournament News

赛事期间：

自动生成：

Entry List Released

↓

Draw Released

↓

Quarterfinal

↓

Semifinal

↓

Final Preview

↓

Champion

整个赛事拥有完整新闻时间线。

---

# 13. Injury News

重大伤病：

自动报道。

例如：

```text
World No.5 withdraws from Wimbledon due to ankle injury.
```

轻伤：

默认不报道。

除非：

影响重大赛事。

---

# 14. Ranking News

当发生：

Top10

Top50

Top100

世界第一

变化时。

自动生成新闻。

例如：

```text
Player breaks into ATP Top100 for the first time.
```

---

# 15. Retirement News

退役：

属于：

Major News。

自动生成：

Career Summary。

包括：

- 冠军数
- 大满贯
- 世界第一周数
- Career Earnings

永久进入：

Hall of Fame。

---

# 16. News Archive

所有新闻：

永久保存。

玩家可查看：

任何年份：

任何 Week：

任何赛事。

例如：

2032

Week18

新闻列表。

不会删除。

---

# 17. UI

底部 Tab：

News。

默认：

最新新闻。

支持：

筛选：

Tournament

Ranking

Player

Injury

History

支持：

搜索。

---

# 18. Data Model

```text
News
NewsID
Season
Week
Category
Priority
Headline
Summary
Body
RelatedPlayer
RelatedTournament
CreatedAt
```

---

# 19. Edge Cases

必须支持：

- 同一天多个 Grand Slam 新闻
- 同一球员多个新闻
- 退役后再次复出（未来）
- Tournament Cancelled
- Olympics 新闻
- Davis Cup 新闻
- Hall of Fame 新闻

---

# 20. Acceptance Criteria

完成后：

✓ 世界新闻自动生成

✓ 玩家不是新闻中心

✓ 新闻来源真实数据

✓ Weekly Report 自动生成

✓ Tournament Timeline 自动生成

✓ 历史新闻永久保存

✓ AI 与玩家共用媒体系统

✓ 支持长期 Career

---

End of Document
