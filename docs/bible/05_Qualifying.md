# Ace Career Game Design Document
## Tournament Qualifying System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Qualifying System（资格赛系统）负责决定：

哪些球员能够通过资格赛进入正赛。

它连接：

- Entry System
- Acceptance List
- Draw System

Qualification 并不是独立赛事。

它属于 Tournament 的组成部分。

---

# 2. Design Goal

Qualification 必须满足：

- 真实 ATP 规则
- AI 与玩家规则一致
- 公平竞争
- 产生 Qualifier
- 产生 Lucky Loser

资格赛不是"第二个比赛"。

而是进入 Main Draw 的唯一正式渠道。

---

# 3. Qualification Flow

```text
Entry Closed
↓
Acceptance List
↓
Qualification List
↓
Qualification Draw
↓
Qualification Round 1
↓
Qualification Final Round
↓
Qualified
↓
Main Draw
```

Qualification 永远发生在 Main Draw 前。

---

# 4. Qualification Size

不同赛事拥有不同资格赛规模。

例如：

| Tournament | Qualifying |
|------------|-----------:|
| ITF M15 | 16 |
| ITF M25 | 16 |
| Challenger | 24 |
| ATP250 | 24 |
| ATP500 | 32 |
| Masters1000 | 48 |
| Grand Slam | 128 |

系统允许不同模板配置。

---

# 5. Qualification Slots

Qualification 晋级人数由 Tournament 决定。

例如：

32 Draw：

4 Qualifiers

28 Draw：

4 Qualifiers

64 Draw：

8 Qualifiers

128 Draw：

16 Qualifiers

Draw 创建时必须预留：

Qualifier Slot。

---

# 6. Qualification Eligibility

以下球员进入 Qualification：

- 排名低于 Direct Acceptance
- 高于 Waiting List Cut
- 未获得 Wild Card
- 未获得 Protected Ranking

玩家：

可主动报名资格赛。

AI：

自动决定。

---

# 7. Qualification Seeding

Qualification 同样拥有种子。

排序规则：

ATP Ranking Snapshot。

不是：

当前实时排名。

Qualification Seed：

独立计算。

不影响 Main Draw Seed。

---

# 8. Qualification Draw

Draw 采用随机抽签。

遵循：

- Seed 分区
- 同国尽量分散（预留）
- Qualification Bracket 固定

Qualification Draw 一旦生成。

不得重新抽签。

---

# 9. Qualification Match

Qualification Match：

与正式比赛一致。

只是：

积分。

奖金。

不同。

Qualification 失败：

直接淘汰。

Qualification 成功：

进入 Main Draw。

---

# 10. Lucky Loser

Qualification Final Round。

失败球员。

进入：

Lucky Loser Pool。

若：

Main Draw Withdrawal。

系统：

按 Lucky Loser 排序。

自动补位。

---

# 11. Lucky Loser Priority

排序依据：

1. Qualification 最后一轮失败

2. ATP 排名

3. 抽签

完全符合 ATP。

不是：

随机。

---

# 12. Qualification Rewards

Qualification：

也拥有奖励。

例如：

- 少量 ATP Points
- 少量 Prize Money
- Confidence
- Match Experience

不会：

空手而归。

---

# 13. AI Behaviour

AI 判断：

是否参加资格赛：

依据：

Priority Score。

若：

Qualification 成功率过低。

AI：

可能放弃。

改打：

ITF。

现实职业球员：

也是如此。

---

# 14. Player Decision

Qualification 页面：

展示：

Main Draw Cut：

180

你的排名：

194

预计进入概率：

68%

推荐：

参加 Qualification。

系统：

不替玩家决定。

---

# 15. Qualification UI

显示：

Qualification Draw

Qualification Round

Remaining Matches

Qualification Slots

Lucky Loser Position

Qualification History

玩家：

可查看完整资格赛签表。

---

# 16. Qualification Data

```text
Qualification
QualificationID
TournamentID
DrawSize
QualifiedSlots
CurrentRound
Status
CreatedAt
```

Qualification Entry：

```text
QualificationEntry
PlayerID
Seed
Ranking
Result
LuckyLoserRank
```

---

# 17. Edge Cases

必须支持：

- Qualification Withdrawal
- Injury Before Qualification
- Injury During Qualification
- Rain Delay（预留）
- Lucky Loser 不足
- Qualification Cancelled
- Wild Card 转 Qualification
- Tournament Cancelled

---

# 18. Acceptance Criteria

Qualification System 完成后：

✓ Qualification Draw 自动生成

✓ AI 自动参加资格赛

✓ 玩家可报名资格赛

✓ Qualification 正常晋级

✓ Lucky Loser 自动补位

✓ Qualification 奖励正确结算

✓ Qualification 历史保存

✓ 长期 Career 稳定运行

---

End of Document
