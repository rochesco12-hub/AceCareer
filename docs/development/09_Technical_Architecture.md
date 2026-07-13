# Ace Career Development Bible
# 09 · Technical Architecture

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Technical Architecture 定义整个 Ace Career 的软件架构。

无论未来增加新系统、新页面、新平台、新玩法，整个架构都不能发生根本变化。

---

# Design Goals

✓ 高内聚 ✓ 低耦合 ✓ Offline First ✓ Data Driven ✓ Config Driven ✓ Engine 与 UI 完全分离 ✓ 支持五年以上迭代

---

# Core Philosophy

- **Engine First**：所有规则属于 Engine，UI 不允许业务逻辑
- **UI Is A Consumer**：UI 只消费数据，所有修改必须经过 Engine
- **Data Driven**：数据来自 Database，规则来自 Config，计算来自 Engine
- **Feature Modularization**：每个功能独立模块，不依赖其他 Feature

---

# 七层架构

```
Presentation     SwiftUI / Components / Animation / Charts / Widgets
Application      页面协调 / Navigation / App State
Feature          具体功能（Training/Recovery/Ranking/Coach/Match/News）
Engine           核心算法（Match/Training/Recovery/Ranking/Career/Story/Simulation）
Repository       唯一数据入口（PlayerRepo/TournamentRepo/RankingRepo/NewsRepo/SaveRepo）
Persistence      本地存储（SwiftData/Cache/Snapshot/Migration）
Infrastructure   系统层（CloudKit/Network/AI/Analytics/Notification/WidgetKit）
```

---

# 关键规则

- **Engine 通过 Event Bus 通信**，禁止互相直接调用
- **所有状态单向流动**：Database → Repository → Engine → ViewModel → View
- **依赖方向单向**：Presentation → Feature → Engine → Repository → Persistence，禁止反向
- **每个 Feature 目录结构统一**（Views/ViewModels/Engine/Models/Repository/Components/Tests）

---

# 目录结构

```
AceCareer
App/  Presentation/  Application/  Features/  Engine/
Repositories/  Persistence/  Infrastructure/  Shared/
Resources/  Configs/  Assets/  Tests/
```

---

# Performance Goals

- Cold Launch <2s
- Today <300ms
- Week Simulation <100ms
- Save <50ms
- Memory <300MB

---

# Definition of Done

✓ 七层架构明确 ✓ Engine 与 UI 完全解耦 ✓ Repository 为唯一数据入口

✓ Event 驱动所有系统 ✓ Offline First ✓ Feature 完全模块化 ✓ 支持五年以上迭代

---

# Final Principle

Ace Career 的架构不是为了今天，而是为了未来数百次版本迭代。

任何一个新功能都应该能够自然接入，而不是推翻整个项目。

---

End of Document
