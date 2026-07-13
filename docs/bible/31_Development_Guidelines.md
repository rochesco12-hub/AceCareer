# Ace Career Game Design Document
## Development Guidelines & Architecture Rules

Version: 1.0
Status: Final
Priority: P0

---

# 1. Purpose

本文件定义 Ace Career 的开发规范。

所有代码、数据结构、系统设计都必须遵守本规范。

它不是编码风格文档。

而是整个项目的最高开发原则。

任何新增功能都必须符合本文件。

---

# 2. Core Principles

整个项目遵循五条原则：

### Single Source of Truth

任何数据只能存在一个来源。

例如：

Ranking

只能来自：

Ranking System。

不能：

Player。

Tournament。

News。

各自维护一份。

---

### Event Driven

所有系统：

只能通过 Event 通信。

例如：

```text
Match Finished
↓
Ranking Updated
↓
News Generated
↓
History Saved
```

禁止：

系统之间直接调用。

---

### Data Driven

所有数值：

必须来自 Config。

禁止：

Magic Number。

例如：

错误：

```swift
if championPoints == 250
```

正确：

```swift
TournamentConfig.championPoints
```

---

### Stateless UI

UI：

只负责展示。

禁止：

UI 保存业务状态。

所有状态：

来自：

Engine。

---

### Deterministic Logic

同样输入。

必须得到：

同样输出。

例如：

使用相同 Seed。

重新模拟比赛。

结果一致。

方便：

Debug。

Replay。

---

# 3. Architecture

项目分为五层：

```text
Presentation
↓
Application
↓
Game Engine
↓
Data Layer
↓
Persistence
```

UI：

永远不能直接访问数据库。

---

# 4. Module Independence

所有模块必须独立。

例如：

Training：

不知道：

News。

News：

不知道：

Training。

统一通过：

EventBus。

通信。

---

# 5. Folder Structure

```text
Core
Calendar
Tournament
Ranking
Match
Training
Health
AI
Economy
Persistence
Presentation
Shared
```

禁止：

功能代码混放。

---

# 6. Naming Rules

统一命名：

```text
Player
Tournament
Match
Season
Week
Coach
News
```

禁止：

缩写。

例如：

Tmt。

Ply。

Rnk。

---

# 7. State Rules

所有对象：

必须拥有：

```text
ID
State
CreatedAt
UpdatedAt
```

所有状态变化：

必须记录。

---

# 8. Event Rules

事件统一格式：

```text
EventID
EventType
Source
Payload
Timestamp
```

事件：

不可修改。

只能消费。

---

# 9. Save Rules

任何新系统：

必须支持：

Save。

Load。

Version Migration。

否则：

禁止上线。

---

# 10. Testing Rules

新增系统：

必须提供：

Unit Test。

Integration Test。

Simulation Test。

Regression Test。

全部通过。

才能 Merge。

---

# 11. Performance Rules

目标：

Week Simulation：

<100ms

Auto Save：

<300ms

Load：

<3s

100 Season：

稳定运行。

---

# 12. Coding Rules

禁止：

- 全局变量
- 循环引用
- UI 写业务逻辑
- 重复数据
- 硬编码配置

必须：

- Dependency Injection
- Protocol
- Config
- Immutable Event

---

# 13. Acceptance Criteria

✓ 所有系统解耦

✓ Event Driven

✓ Data Driven

✓ Save Compatible

✓ Long Career Stable

✓ 易于扩展

---

End of Document
