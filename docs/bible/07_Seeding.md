# Ace Career Game Design Document
## Tournament Seeding System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Seeding System（种子系统）负责确定赛事种子球员。

目标：

避免世界排名最高的球员在赛事前几轮提前相遇。

Seed System 连接：

- Ranking System
- Acceptance List
- Draw System

Draw 开始之前必须先完成 Seed。

---

# 2. Design Goal

种子系统必须满足：

- 使用 ATP 官方规则
- 玩家与 AI 共用规则
- 自动根据排名计算
- 支持所有赛事级别
- 支持 Withdraw 后重新计算（Draw 前）
- Draw 发布后不再修改

---

# 3. Seed Generation Pipeline

```text
Acceptance List Locked
↓
Read ATP Ranking Snapshot
↓
Sort Eligible Players
↓
Generate Seeds
↓
Validate
↓
Send To Draw System
```

Seed 必须在 Draw 前完成。

---

# 4. Ranking Snapshot

Seed 使用：

报名截止时 ATP Ranking。

不是：

Draw 当天。

例如：

Week18：

报名截止。

Week19：

排名更新。

Seed：

仍然使用：

Week18 Ranking。

符合 ATP 官方规则。

---

# 5. Number of Seeds

不同签位拥有不同 Seed 数量。

| Draw Size | Seeds |
|-----------|------:|
| 8 | 2 |
| 16 | 4 |
| 28 | 8 |
| 32 | 8 |
| 48 | 16 |
| 56 | 16 |
| 64 | 16 |
| 96 | 32 |
| 128 | 32 |

系统自动计算。

无需人工配置。

---

# 6. Seed Eligibility

能够成为 Seed：

必须：

- Main Draw
- Direct Acceptance
- Wild Card（若排名足够）
- Protected Ranking（特殊赛事预留）

Qualification：

不能成为 Seed。

Lucky Loser：

不能成为 Seed。

---

# 7. Seed Placement

Seed1：

固定 Position1。

Seed2：

固定最后一个 Position。

Seed3~4：

随机上下半区。

Seed5~8：

随机四分之一区。

Seed9~16：

随机八分之一区。

Seed17~32：

随机十六分之一区。

完全符合 ATP 抽签原则。

---

# 8. Seed Protection

目标：

Seed 不会提前相遇。

例如：

Seed1

不会：

Round1

遇见：

Seed2。

Quarterfinal 前：

不会：

Seed1

vs

Seed5。

Semifinal 前：

不会：

Seed1

vs

Seed3。

Draw Generator 必须保证。

---

# 9. Seed Withdrawal

Draw 前：

Seed Withdrawal。

系统：

重新计算 Seed。

重新抽签。

Draw 发布后：

Seed Withdrawal。

不重新计算 Seed。

Lucky Loser：

补位。

Bracket 保持不变。

---

# 10. Wild Card Seed

Wild Card：

若排名足够。

允许：

成为 Seed。

例如：

世界排名：

18。

获得 Wild Card。

仍然：

Seed。

不是：

普通球员。

---

# 11. Protected Ranking Seed

Protected Ranking：

默认：

不能作为 Seed。

Seed：

只参考：

当前 ATP Ranking。

符合 ATP。

---

# 12. AI Behaviour

AI：

不会：

因为 Seed。

改变报名。

AI：

只根据：

Priority。

决定赛事。

Seed：

只是比赛结果。

不是：

报名条件。

---

# 13. UI

签表：

Seed：

显示：

```text
(1)
Carlos Alcaraz
```

球员详情：

显示：

Current Seed

Career Best Seed

Seed History

---

# 14. Data Model

```text
Seed
SeedID
TournamentID
PlayerID
SeedNumber
RankingSnapshot
CreatedAt
```

---

# 15. Validation

生成 Seed 后必须验证：

✓ Seed 数量正确

✓ 排名顺序正确

✓ 无重复 Seed

✓ 所有 Seed 在 Main Draw

✓ Position 合法

验证失败：

重新生成。

---

# 16. Edge Cases

支持：

- Withdrawal Before Draw
- Withdrawal After Draw
- Wild Card Seed
- Protected Ranking
- Lucky Loser
- Tournament Cancelled
- Draw Reset（管理员赛事）

---

# 17. Acceptance Criteria

完成后：

✓ 自动计算 Seed

✓ Seed Placement 正确

✓ Draw 正确读取 Seed

✓ Withdraw 处理正确

✓ 所有赛事支持 Seed

✓ 长期 Career 无冲突

---

End of Document
