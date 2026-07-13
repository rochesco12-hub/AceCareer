# Ace Career Game Design Document
## Global State Machine

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

State Machine（状态机）定义 Ace Career 中所有对象的生命周期。

任何对象（Player、Tournament、Match、Season）都必须拥有明确状态。

所有状态变化只能通过合法 Transition 发生。

禁止直接修改最终状态。

例如：

❌

Healthy

↓

Major Injury

↓

Healthy

这是非法转换。

必须：

Healthy

↓

Fatigued

↓

Minor Injury

↓

Treatment

↓

Rehabilitation

↓

Training Ready

↓

Match Ready

↓

Healthy

---

# 2. Design Philosophy

整个 Career 不允许出现：

"瞬间变化"

所有状态必须：

可追踪

可恢复

可回放

可存档

所有状态变化：

必须记录日志。

---

# 3. Global State Categories

Ace Career 包含以下 State Machine：

Player State

Tournament State

Match State

Career State

Season State

Training State

Health State

Travel State

AI State

Finance State（未来）

---

# 4. Player Career State

玩家职业状态：

```text
Junior
↓
ITF Player
↓
Challenger Player
↓
ATP Player
↓
Top100
↓
Top50
↓
Top10
↓
World No.1
↓
Veteran
↓
Retired
```

系统自动判断。

无需手动升级。

---

# 5. Tournament State

赛事状态：

```text
Planning
↓
Created
↓
Entry Open
↓
Entry Closed
↓
Acceptance Published
↓
Draw Released
↓
Active
↓
Completed
↓
Archived
```

任何赛事：

必须遵循此流程。

---

# 6. Match State

比赛状态：

```text
Scheduled
↓
Warm Up
↓
Playing
↓
Medical Timeout
↓
Completed
↓
Verified
↓
Archived
```

若发生：

Walkover：

```text
Scheduled
↓
Walkover
↓
Completed
```

---

# 7. Health State

健康状态：

```text
Healthy
↓
Fatigued
↓
Minor Injury
↓
Major Injury
↓
Treatment
↓
Rehabilitation
↓
Training Ready
↓
Match Ready
↓
Healthy
```

禁止：

直接恢复。

---

# 8. Training State

训练状态：

```text
Idle
↓
Training Planned
↓
Training Active
↓
Training Completed
↓
Recovery
↓
Idle
```

比赛周：

禁止：

High Intensity。

---

# 9. Travel State

旅行状态：

```text
At Home
↓
Preparing
↓
Travelling
↓
Arrived
↓
Recovered
↓
Ready
```

长途旅行：

增加：

Fatigue。

---

# 10. AI State

AI 每周：

```text
Planning
↓
Evaluating
↓
Entering Tournament
↓
Training
↓
Travelling
↓
Competing
↓
Recovering
↓
Planning
```

无限循环。

---

# 11. Season State

赛季：

```text
Pre Season
↓
Regular Season
↓
Grand Slam Season
↓
ATP Finals
↓
Off Season
↓
Next Season
```

Season：

永远不会倒退。

---

# 12. Career State

Career：

```text
Career Created
↓
Active Career
↓
Paused
↓
Retired
↓
Hall Of Fame
```

Retired：

禁止恢复。

未来可支持：

Comeback（特殊模式）。

---

# 13. State Transition Rules

所有状态变化：

必须满足：

Current State

+

Trigger

+

Validation

+

Next State

例如：

Health

Current：

Healthy

Trigger：

Heavy Training

Validation：

Fatigue > 80

Next：

Fatigued

不能：

直接：

Healthy

↓

Major Injury

---

# 14. Event Trigger

所有状态变化：

必须来源：

Event。

例如：

Tournament Created

↓

Tournament State 更新

Match Finished

↓

Ranking 更新

Recovery Completed

↓

Health 更新

State：

不能：

主动变化。

---

# 15. State Log

所有变化：

记录：

```text
StateID
ObjectID
OldState
NewState
Reason
Week
Timestamp
```

方便：

Career Replay。

Bug 排查。

未来：

Career Timeline。

---

# 16. Invalid Transition

必须阻止：

例如：

Major Injury

↓

Champion

Fatigued

↓

Heavy Training

↓

Match

Recovery

↓

Grand Slam Final

系统：

必须拒绝。

---

# 17. UI Rules

Today 页面：

状态：

必须可见。

例如：

Health

Match Ready

Tournament

Draw Released

Training

Recovery

Travel

Arrived

玩家：

不用进入详情。

即可知道：

当前状态。

---

# 18. Developer Rules

新增任何系统。

必须：

拥有：

State Machine。

否则：

禁止开发。

所有：

State：

统一：

Enum。

禁止：

String。

---

# 19. Edge Cases

支持：

- Tournament Cancelled
- Injury During Match
- Retirement
- Walkover
- Rain Delay
- Save / Load
- Crash Recovery
- AI Pause

所有状态：

必须可恢复。

---

# 20. Acceptance Criteria

完成后：

✓ 所有对象拥有 State

✓ Transition 合法

✓ 所有变化可记录

✓ Save 可恢复

✓ Career 可回放

✓ AI 与玩家一致

✓ 支持长期 Career

---

End of Document
