# Ace Career Development Bible
# 11 · Data Flow

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Data Flow 定义整个 Ace Career 的数据流转方式。

整个项目必须遵循统一的数据流。任何模块都不能绕过 Data Flow。

---

# Design Goals

✓ 单向数据流 ✓ Single Source of Truth ✓ Engine 唯一负责业务计算 ✓ UI 永远只负责展示 ✓ 数据来源唯一 ✓ 易于调试和测试

---

# Core Principle

```
User → UI → ViewModel → Engine → Repository → Database
                                              ↓
           UI ← ViewModel ← Repository ← (Event)
```

---

# Golden Rule（三道禁令）

- View ⇸ Database（禁止直接读写）
- View ⇸ Player（禁止直接修改）
- View ⇸ CloudKit（禁止直接操作）

---

# 示例：Start Training

```
Button → TrainingViewModel → TrainingEngine → GrowthEngine → PlayerRepository → Database
                                                                                    ↓
                                TodayViewModel ← PlayerUpdated Event ← (Event Bus)
                                      ↓
                                  UI Refresh
```

---

# 示例：Finish Match

```
MatchEngine → CareerEngine → RankingEngine → StoryEngine → NewsEngine → Repositories → Database
                                                                                          ↓
                    Today / Ranking / Career / News 全部刷新 ← WorldUpdated Event
```

UI 完全不知道发生了什么，只知道数据更新了。

---

# Event Bus（核心事件类型）

PlayerUpdated / CareerUpdated / TournamentUpdated / RankingUpdated / WorldUpdated / StoryUpdated / SaveCompleted / CloudSynced

---

# 关键规则

- **Transaction 保证**：重要操作（如比赛结束）必须全部成功或全部回滚
- **Async**：Cloud Sync 后台执行，UI 无需等待
- **State Ownership**：每个状态只有一个 Owner（如 Fatigue 只属于 Player，不属于 Today/Training/Recovery）
- **Offline 与 Online 同一流程**，联网后 Repository 自动同步

---

# Week Advance Flow

Continue Week → Simulation → Tournament → Ranking → Career → Story → News → Save → UI

任何步骤失败，整个事务回滚。

---

# Definition of Done

✓ 单向数据流 ✓ UI 不直接操作数据库 ✓ Engine 唯一负责业务逻辑

✓ Repository 唯一负责数据访问 ✓ Event 驱动模块通信 ✓ Transaction 保证一致性 ✓ Offline/Online 同一流程

---

# Final Principle

数据永远沿着一个方向流动。任何模块都不能绕过这条路径。

稳定的数据流，才是一个能够持续开发十年的项目真正的基础。

---

End of Document
