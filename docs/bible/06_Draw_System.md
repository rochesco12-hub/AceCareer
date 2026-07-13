# Ace Career Game Design Document
## Tournament Draw System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Draw System（抽签系统）负责在报名结束后，为赛事生成正式签表（Main Draw）。

Draw 的目标不是随机排序球员。

而是在符合 ATP 官方规则的前提下，生成公平、稳定、可复现的签表。

Draw System 是 Tournament Week 的正式开始。

Draw 发布后：

- 玩家正式知道第一轮对手
- AI 开始制定比赛计划
- 新闻系统生成抽签报道
- Tournament 正式进入 Active 阶段

---

# 2. Design Goal

Draw System 必须满足：

- 遵循 ATP 抽签规则
- 支持所有赛事级别
- 支持不同签位规模
- 支持种子保护
- 支持 Bye
- 支持 Wild Card
- 支持 Qualifier
- 支持 Lucky Loser
- 支持 Withdrawal 补位
- 保证同一 Seed 不会提前相遇

---

# 3. Draw Lifecycle

```text
Acceptance List Locked
↓
Seed Generated
↓
Bracket Generated
↓
Wild Card Assigned
↓
Qualifier Slots Reserved
↓
Random Draw
↓
Draw Published
↓
Tournament Active
```

Draw 一旦发布。

不得重新抽签。

---

# 4. Supported Draw Sizes

系统支持：

| Draw Size | Typical Tournament |
|-----------|-------------------|
| 8 | 小型邀请赛 |
| 16 | ITF |
| 28 | ATP250 |
| 32 | Challenger / ATP250 |
| 48 | ATP500（部分） |
| 56 | Masters1000 |
| 64 | Challenger（部分） |
| 96 | Masters1000 |
| 128 | Grand Slam |

所有 Draw 使用统一算法。

---

# 5. Draw Components

一个 Draw 包含：

- Seeds
- Direct Acceptance
- Wild Card
- Qualifier
- Lucky Loser
- Bye（如适用）

所有类型统一存放于：

Draw Entry。

---

# 6. Seed Placement

Seed 必须优先放置。

例如：

32 Draw：

Seed1

固定：

Position 1

Seed2

固定：

Position 32

Seed3~4

随机：

上下半区。

Seed5~8

随机：

四分之一区。

Seed9~16

随机：

八分之一区。

符合 ATP 官方规则。

---

# 7. Bye Rules

部分赛事：

拥有 Bye。

例如：

Masters1000

Top Seeds：

自动 Bye。

Bye：

只允许：

Round1。

进入：

Round2。

Bye 不属于球员。

属于：

Bracket Position。

---

# 8. Wild Card Placement

Wild Card：

随机进入：

非 Seed 位置。

不得：

替代 Seed。

不得：

替代 Bye。

Wild Card：

可能第一轮遇见 Seed。

符合 ATP 规则。

---

# 9. Qualifier Placement

Qualifier：

抽签前：

未知身份。

Bracket：

预留：

Q Slot。

Qualification 完成后。

自动：

填入：

对应位置。

Draw：

保持不变。

---

# 10. Lucky Loser Placement

若：

Main Draw 已发布。

有人 Withdrawal。

系统：

Lucky Loser。

替换：

对应签位。

不会：

重新抽签。

---

# 11. Same Nation Rule

Alpha：

不处理。

Beta：

支持：

同国球员：

第一轮尽量分开。

Grand Slam：

必须支持。

---

# 12. Draw Generation Algorithm

```text
Step1
Create Empty Bracket
↓
Step2
Place Seeds
↓
Step3
Place Bye
↓
Step4
Reserve Q Slots
↓
Step5
Place Wild Cards
↓
Step6
Random Remaining Players
↓
Step7
Validate
↓
Publish
```

任何一步失败。

整个 Draw 回滚。

---

# 13. Draw Validation

生成后必须验证：

✓ 所有 Seed 正确

✓ Draw 人数正确

✓ Bye 数量正确

✓ Wild Card 数量正确

✓ Qualification 数量正确

✓ 无重复 Player

✓ 无空 Slot

验证失败：

重新生成。

---

# 14. Draw Publish

Draw 发布后：

自动触发：

- Tournament Active
- 新闻
- 玩家通知
- AI 战术准备
- 对阵分析

发布时间：

通常：

比赛前：

2~3 天。

---

# 15. UI

Draw 页面：

显示：

Tournament Header

↓

Bracket

↓

Player Card

↓

Seed

↓

Nationality

↓

Ranking

↓

Surface

点击球员：

查看资料。

点击比赛：

查看 Match Detail。

---

# 16. Interactive Draw（Ace League）

如果赛事由玩家创建：

支持：

Interactive Draw。

管理员：

拖动。

随机。

抽签动画。

骰子。

Emoji。

最终结果：

仍写入：

统一 Draw Database。

保证：

线上线下：

同一规则。

---

# 17. Data Model

```text
Draw
DrawID
TournamentID
DrawSize
Status
CreatedAt
```

Draw Entry：

```text
EntryID
DrawID
PlayerID
Position
Seed
EntryType
Round
Result
```

EntryType：

```text
DIRECT
SEED
WILD_CARD
QUALIFIER
LUCKY_LOSER
BYE
```

---

# 18. Edge Cases

必须支持：

- Withdrawal Before Draw
- Withdrawal After Draw
- Qualification Delay
- Rain Delay（预留）
- Lucky Loser 补位
- Seed Withdrawal
- Wild Card Withdrawal
- Tournament Cancelled
- Walkover Before Match

不得：

重新抽签。

---

# 19. Acceptance Criteria

Draw System 完成后：

✓ 支持所有 Draw Size

✓ Seed 正确分布

✓ Wild Card 正常进入

✓ Qualification 正常进入

✓ Lucky Loser 正常补位

✓ Draw 一旦发布不可修改

✓ Interactive Draw 与自动 Draw 共用数据结构

✓ 长期 Career 稳定运行

---

End of Document
