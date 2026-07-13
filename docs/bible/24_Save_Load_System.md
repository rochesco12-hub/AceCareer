# Ace Career Game Design Document
## Save / Load & Persistence System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Save System（存档系统）负责整个 Career 世界的数据持久化。

它不仅保存玩家。

而是保存：

整个世界。

包括：

- 世界排名
- 所有 AI 球员
- 所有赛事
- 所有新闻
- 所有历史
- 所有教练
- 所有奖金
- 所有伤病
- 所有职业生涯

任何时候重新进入游戏。

整个世界必须恢复到退出前完全一致的状态。

---

# 2. Design Goal

Save System 必须满足：

- 秒存档
- 自动存档
- 手动存档
- 云同步
- 多存档
- 不坏档
- 不丢数据
- 支持50年以上 Career

---

# 3. Save Philosophy

Ace Career 不保存：

一个玩家。

而是保存：

一个世界。

例如：

Save001

实际上保存：

```text
Career
+
World
+
Calendar
+
History
+
AI
+
Tournament
+
News
```

恢复时：

整个世界恢复。

---

# 4. Save Pipeline

任何自动存档：

必须执行：

```text
Freeze World
↓
Collect Dirty Objects
↓
Serialize
↓
Compress
↓
Checksum
↓
Write Save
↓
Verify
↓
Unlock World
```

若失败：

保持旧存档。

不得覆盖。

---

# 5. Auto Save

默认：

以下时机：

自动存档。

- 新 Week 开始
- Tournament 结束
- Season 结束
- 排名更新
- Career 创建
- Career 退出

玩家无需手动保存。

---

# 6. Manual Save

玩家：

可：

创建：

手动存档。

包括：

Save Slot

名称

时间

Career Week

Ranking

Location

方便：

回档。

---

# 7. Save Slots

默认：

支持：

10 个手动存档。

Auto Save：

独立。

不会占用。

支持：

未来扩展。

---

# 8. Save Content

必须保存：

Career

Player

AI

World

Season

Week

Ranking

Tournament

Draw

Match

Training

Health

Finance

Coach

News

History

Hall Of Fame

全部恢复。

---

# 9. Incremental Save

系统采用：

Dirty Object。

只有：

发生变化：

对象。

重新写入。

避免：

整个世界。

全部重写。

提高速度。

---

# 10. Save Version

每份存档：

拥有：

```text
Version
1.0.0
SchemaVersion
DatabaseVersion
```

未来：

升级：

兼容旧版本。

---

# 11. Cloud Save

支持：

Cloud。

流程：

```text
Local Save
↓
Upload
↓
Cloud
↓
Verify
↓
Sync Success
```

冲突：

保留：

最新版本。

未来：

支持：

Merge。

---

# 12. Corruption Protection

每份 Save：

保存：

Checksum。

读取：

验证。

若失败：

恢复：

上一份：

Auto Save。

保证：

不坏档。

---

# 13. Backup Strategy

系统：

始终保留：

最近：

3 次 Auto Save。

例如：

AutoSave_A

AutoSave_B

AutoSave_C

最新失败：

自动恢复。

---

# 14. Migration

未来：

更新：

Data Schema。

旧 Save：

自动：

Migration。

不得：

要求玩家：

重新开档。

---

# 15. Save Metadata

首页：

显示：

Career Name

Season

Week

Ranking

Career Earnings

Play Time

Save Time

Version

方便：

管理。

---

# 16. Performance

Auto Save：

目标：

<300ms。

Manual Save：

目标：

<2s。

读取：

<3s。

世界：

2000+

AI。

依旧：

稳定。

---

# 17. Data Model

```text
SaveFile
SaveID
CareerID
Season
Week
Timestamp
Version
Checksum
PlayTime
CloudVersion
DirtyObjects
```

---

# 18. Edge Cases

支持：

- 强制退出
- App 崩溃
- 云同步失败
- Schema 升级
- Save 回滚
- AutoSave 损坏
- 重复存档
- 多设备登录

---

# 19. Developer Tools

Debug：

支持：

Force Save

Force Load

Corrupt Save

Migration Test

Rollback

Compare Save

Dump Save

方便：

开发。

---

# 20. Acceptance Criteria

✓ 自动存档正常

✓ 手动存档正常

✓ 云同步正常

✓ 长期 Career 不坏档

✓ Schema 可升级

✓ 支持 50+ Season

✓ 世界完整恢复

---

End of Document
