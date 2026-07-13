# Ace Career Development Bible
# 01 · Database Architecture

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Database Architecture 定义整个 Ace Career 的数据结构。

它不是数据库表。

而是整个游戏世界的数据组织方式。

如果 Engine 是世界运行规则。

那么 Database 就是世界本身。

整个项目只有一个数据源（Single Source of Truth）。

任何功能。

都必须建立在 Database Architecture 之上。

---

# Design Goals

Database 必须满足：

- 可扩展（Extensible）
- 可维护（Maintainable）
- 可同步（Syncable）
- 可配置（Config Driven）
- 可版本升级（Versioned）
- 支持 Offline First
- 支持未来 Online Career

任何新增功能。

不能修改已有 Schema。

只能扩展。

---

# Core Principles

### Principle 1 — Single Source Of Truth

所有数据只有一份。

例如：

Player Ranking 只能存在 Ranking System。

不能 Player / Tournament / News 各自维护一份。

---

### Principle 2 — Reference Instead Of Copy

对象之间永远引用。

正确：`Match.winnerPlayerId`

错误：`Match.winnerName / winnerCountry / winnerRanking`

所有信息都来自 Player。

---

### Principle 3 — Immutable History

历史数据永远不可修改。

冠军、Career History — Append Only。

---

### Principle 4 — Current State + Historical State

任何对象同时拥有 Current 和 History。

---

# Database Layers

六层架构：

```text
World → Competition → Player → Career → Simulation → System
```

- **World**：Calendar / Ranking / Population / History / News / Season / Config
- **Competition**：Tournament / Entry / Draw / Match / Statistics / Prize / Points
- **Player**：Attributes / Ratings / Coach / Training / Recovery / Injury / Finance
- **Career**：Timeline / Achievements / Titles / Records / Hall Of Fame
- **Simulation**：AI Decision / World Sim / Narrative / Probability / Growth
- **System**：Config / Save / Cloud / Settings / Analytics / Version

---

# Root Object

整个游戏只有一个 Root：`World`。

```
World
├── Players
├── Rankings
├── Calendar
├── Tournaments
├── News
├── History
├── Config
└── Save
```

---

# Entity Relationship

```
World
├── Player → Career / Coach / Injury / Training / Finance / Statistics
├── Tournament → Entry / Draw / Match / Prize / Points
├── Ranking
├── Calendar
├── News
└── History
```

---

# Primary Entities（12个）

Player / Tournament / Match / Ranking / Calendar / Career
Coach / News / History / Season / Config / Save

---

# IDs & Relationships

全部 UUID。拒绝 Name/Ranking/Index 作为关联。

---

# Read / Write Flow

View 永远只读。所有修改统一经过 Engine。

---

# Save Strategy

只保存变化数据。Config 完全独立（JSON 文件）。

---

# Performance Goals

- 2200 Players：<50 MB
- 100 Years History：<200 MB
- Week Simulation：<100 ms
- Today Query：<20 ms

---

# Breaking Changes

修改 PlayerID / TournamentID / Root Entity / Save Format 需升级 Database Version。

---

# Definition of Done

✓ World 为唯一 Root

✓ Entity 职责清晰

✓ 数据无重复

✓ 全部 UUID 引用

✓ Config 与 Data 分离

✓ 支持 Offline First

✓ 支持未来十年以上扩展

---

# Final Principle

Database 不属于玩家。Database 属于整个职业网球世界。

世界先存在。数据永远真实。

所有系统都只是这个世界的不同观察方式。

---

End of Document
