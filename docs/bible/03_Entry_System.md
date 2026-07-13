# Ace Career Game Design Document
## Tournament Entry System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Entry System（报名系统）负责管理整个职业网球世界所有赛事的报名流程。

它决定：

- 玩家是否能够报名某站赛事
- AI 是否能够报名
- 正赛名单如何产生
- 资格赛名单如何产生
- Waiting List 如何维护
- Wild Card 如何加入
- Withdrawal 后如何补位

Entry System 是 Tournament System 的第一道核心逻辑。

---

# 2. Design Goal

报名系统必须满足以下目标：

1. 完全符合真实 ATP 报名逻辑
2. 玩家与 AI 使用同一套规则
3. 同一周只能参加一站正式赛事
4. 报名必须提前完成
5. 不允许临时空降赛事

---

# 3. Entry Lifecycle

每一个报名都必须经过以下生命周期：

```text
Tournament Created
↓
Entry Open
↓
Player / AI Entry
↓
Entry Closed
↓
Acceptance List
↓
Qualifying
↓
Draw Released
↓
Tournament Active
```

任何步骤不得跳过。

---

# 4. Tournament Entry Status

赛事报名共有八种状态：

```text
COMING_SOON
ENTRY_OPEN
ENTRY_CLOSED
WAITING_LIST
QUALIFYING
DRAW_RELEASED
ACTIVE
FINISHED
```

UI 必须根据状态显示不同颜色。

---

# 5. Entry Window

默认开放时间：

提前 4 周。

例如：

Week 20 ATP250。

Week16：

开放报名。

Week19：

截止报名。

Week20：

比赛开始。

---

# 6. Player Entry Rules

玩家点击：

报名赛事。

系统必须执行：

Eligibility Engine。

任何条件失败。

不得进入报名。

---

# 7. Eligibility Engine

Eligibility Engine 按固定顺序检查：

Step 1

Tournament Status

↓

Step 2

Week Conflict

↓

Step 3

Health

↓

Step 4

Ranking

↓

Step 5

Travel

↓

Step 6

Protected Ranking

↓

Step 7

Wild Card

↓

Step 8

Qualifying

↓

Entry Success

不得改变检查顺序。

---

# 8. Tournament Status Check

只有：

ENTRY_OPEN。

允许报名。

其它状态：

全部禁止。

返回：

```text
ENTRY_NOT_AVAILABLE
```

---

# 9. Week Conflict Check

玩家：

同一 Week。

只能拥有一个正式赛事。

例如：

Week18：

已经报名：

Monastir M15。

再次点击：

Antalya M15。

返回：

```text
WEEK_CONFLICT
```

允许：

取消当前报名。

重新选择。

截止后：

禁止修改。

---

# 10. Health Check

不同健康状态：

允许不同报名。

| Health | Can Enter |
|---------|-----------|
| Healthy | ✓ |
| Fatigued | ✓ |
| Minor Injury | ✓（提示风险） |
| Rehabilitation | ✗ |
| Major Injury | ✗ |

系统必须明确提示原因。

---

# 11. Ranking Check

每项赛事拥有：

Entry Cut。

例如：

ATP250：

Top120。

玩家：

世界排名：

280。

返回：

```text
RANKING_TOO_LOW
```

赛事：

仍然显示。

但按钮：

Disabled。

---

# 12. Travel Check

系统计算：

上一站赛事。

↓

下一站赛事。

旅行时间。

若：

无法赶到。

返回：

```text
TRAVEL_CONFLICT
```

例如：

周日。

罗马。

周一。

东京。

禁止报名。

---

# 13. Protected Ranking

长期伤病复出。

拥有：

Protected Ranking。

系统：

使用：

PR Ranking。

判断资格。

而不是：

Current Ranking。

---

# 14. Wild Card

赛事拥有：

固定 Wild Card 数量。

玩家：

可申请。

AI：

也可申请。

审批：

由 AI Tournament Committee 决定。

不是：

100% 获得。

---

# 15. Qualifying

若：

排名接近 Cut。

系统：

推荐：

Qualification。

按钮：

Join Qualifying。

资格赛结束。

自动决定：

是否进入正赛。

---

# 16. Waiting List

正赛人数已满。

进入：

Waiting List。

若：

Withdrawal。

系统：

自动：

递补。

---

# 17. Withdrawal

报名后。

截止前。

允许：

Withdraw。

截止后。

Withdrawal：

进入：

Waiting List。

重新排序。

若：

Draw 已发布。

Withdrawal：

进入：

Lucky Loser。

---

# 18. Entry Result

报名成功。

返回：

```text
SUCCESS
TournamentID
EntryType
Main Draw
or
Qualifying
or
Waiting List
```

所有 Entry：

写入：

Player Schedule。

---

# 19. UI Specification

赛事卡片：

必须显示：

赛事名称

国家

城市

场地

奖金

冠军积分

报名截止时间

预计 Cut Ranking

当前状态

按钮：

根据 Eligibility。

动态变化。

例如：

Join

Qualified

Waiting

Ranking Too Low

Week Conflict

Injured

Entry Closed

---

# 20. AI Entry Logic

AI：

每周。

重新计算：

最佳赛事。

若：

Priority。

更高。

且：

报名未截止。

允许：

Withdraw。

重新报名。

AI：

不得：

无限切换。

默认：

最多：

一次。

---

# 21. Data Model

```text
TournamentEntry

EntryID

PlayerID

TournamentID

EntryType

Status

CreatedAt

UpdatedAt

Seed

AcceptanceOrder

ProtectedRanking

WildCard

Qualifying

WaitingListPosition
```

---

# 22. Edge Cases

必须支持：

- Withdrawal Before Draw
- Withdrawal After Draw
- Injury Before Tournament
- Injury During Entry
- Protected Ranking
- Wild Card Declined
- Waiting List Promotion
- Qualifying Promotion
- Lucky Loser Promotion
- Tournament Cancelled

---

# 23. Acceptance Criteria

Entry System 完成后：

✓ 玩家可以自由报名

✓ AI 自动报名

✓ 同周只能报名一站

✓ 排名决定资格

✓ Health 正确限制报名

✓ Waiting List 正常运行

✓ Wild Card 正常运行

✓ Qualification 正常运行

✓ Withdrawal 正常补位

✓ 支持长期 Career

---

End of Document
