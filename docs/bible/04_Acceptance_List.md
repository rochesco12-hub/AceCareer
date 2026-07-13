# Ace Career Game Design Document
## Tournament Acceptance List System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Acceptance List（参赛名单系统）负责决定：

**哪些球员最终进入赛事。**

它连接：

- Entry System
- Qualifying
- Draw
- Tournament

Acceptance List 一旦锁定，就代表赛事正式进入组织阶段。

---

# 2. Design Goal

Acceptance List 必须保证：

- 世界所有赛事公平录取
- 玩家与 AI 使用完全相同规则
- 排名决定录取顺序
- Wild Card、Protected Ranking、Special Exempt 有固定席位
- Withdrawal 后自动补位

Acceptance List 不是随机生成。

而是一个完整算法。

---

# 3. Acceptance Pipeline

所有赛事都遵循统一流程：

```text
Entry Closed
↓
Collect Entries
↓
Sort Ranking
↓
Apply Protected Ranking
↓
Allocate Wild Card
↓
Allocate Special Exempt
↓
Main Draw Filled
↓
Waiting List
↓
Acceptance Published
```

---

# 4. Draw Composition

以 32 签位赛事为例：

```text
Main Draw
24 Direct Acceptance
4 Qualifiers
4 Wild Cards
```

若赛事没有资格赛：

```text
28 Direct Acceptance
4 Wild Cards
```

Draw Structure 由 Tournament 决定。

Acceptance List 必须根据赛事模板自动生成。

---

# 5. Direct Acceptance

Direct Acceptance 为：

按照 Entry Deadline 时的 ATP 排名排序。

例如：

Entry Closed

↓

ATP Ranking Snapshot

↓

排序

↓

录取前 N 名

录取后：

状态：

```text
DIRECT_ACCEPTANCE
```

---

# 6. Entry Ranking Snapshot

Acceptance 使用：

报名截止时排名。

不是：

比赛开始时排名。

例如：

Week16

报名截止。

Week17

排名变化。

Acceptance：

保持：

Week16 Snapshot。

符合 ATP 规则。

---

# 7. Protected Ranking

长期伤病复出球员。

拥有：

Protected Ranking。

Acceptance 判断：

优先：

Protected Ranking。

不是：

Current Ranking。

PR 使用次数：

Career 中独立记录。

例如：

Remaining PR Entries：

8

每使用一次：

减少一次。

---

# 8. Wild Card

每站赛事拥有：

固定 Wild Card 数。

例如：

ATP250

4

Challenger

4

ITF

2

Wild Card 来源：

Tournament Committee。

玩家：

可申请。

AI：

可申请。

审批算法：

由 Tournament AI 决定。

不是：

100% 获得。

---

# 9. Special Exempt

若球员：

上一周仍在高级赛事。

导致：

无法参加资格赛。

允许：

Special Exempt。

SE：

直接进入 Main Draw。

不占 Wild Card。

---

# 10. Qualifying Allocation

资格赛名额：

固定。

例如：

32 Draw。

Qualification：

24 人。

Qualification 决定：

4 名晋级。

Acceptance List：

必须保留：

Qualifier Slot。

---

# 11. Waiting List

Main Draw 满员。

剩余报名者：

进入：

Waiting List。

Waiting List：

按照：

Acceptance Ranking。

排序。

不是：

随机。

---

# 12. Withdrawal Before Draw

Acceptance 发布后。

Draw 前。

有人 Withdrawal。

系统：

Waiting List 第一位：

自动进入：

Main Draw。

Acceptance：

重新生成。

Draw：

保持未发布。

---

# 13. Withdrawal After Draw

Draw 已完成。

Withdrawal。

系统：

不重新生成 Acceptance。

而是：

Lucky Loser。

补位。

保持 Draw 不变。

---

# 14. Acceptance States

每位球员拥有：

```text
DIRECT_ACCEPTANCE
QUALIFYING
WAITING_LIST
WILD_CARD
SPECIAL_EXEMPT
WITHDRAWN
REJECTED
```

所有状态：

互斥。

---

# 15. Acceptance UI

Acceptance 页面：

显示：

Main Draw

↓

Qualifying

↓

Waiting List

玩家：

可以查看：

自己：

当前位置。

例如：

```text
Waiting List
Position
3
```

系统：

自动预测：

进入概率。

---

# 16. Acceptance Refresh

Acceptance 不实时刷新。

刷新节点：

Entry Closed

↓

Withdrawal

↓

Protected Ranking Change

↓

Tournament Cancelled

避免：

排名实时变化。

导致：

Acceptance 不稳定。

---

# 17. AI Behaviour

AI：

报名结束后。

不会：

无限 Withdrawal。

AI：

只会：

根据：

伤病。

疲劳。

赛程冲突。

决定：

是否退出。

保持世界稳定。

---

# 18. Data Model

```text
AcceptanceEntry

AcceptanceID

TournamentID

PlayerID

AcceptanceType

AcceptanceRanking

CurrentRanking

ProtectedRanking

WildCard

SpecialExempt

Qualifier

WaitingPosition

Status

CreatedAt
```

---

# 19. Edge Cases

必须支持：

- Protected Ranking 超过 Draw 数量
- Wild Card 未发放完
- Qualification 取消
- Tournament Cancelled
- 多人同时 Withdrawal
- Waiting List 用尽
- Lucky Loser 不足
- AI 临时退赛

不得：

破坏 Draw。

---

# 20. Acceptance Criteria

Acceptance List 完成后：

✓ Main Draw 自动生成

✓ Waiting List 正常排序

✓ Wild Card 正常发放

✓ Protected Ranking 正常工作

✓ Special Exempt 正常工作

✓ Withdrawal 自动补位

✓ Draw 数据稳定

✓ 玩家与 AI 共用 Acceptance

✓ 长期 Career 无冲突

---

End of Document
