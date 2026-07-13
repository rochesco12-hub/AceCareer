# Ace Career Development Bible
# 12 · State Management

Version: 1.0
Status: Final
Priority: P0

---

# Overview

State Management 定义整个 Ace Career 的状态管理体系。

三个核心问题：谁拥有状态、谁可以修改状态、UI 为什么刷新。

---

# Design Goals

✓ Single Source of Truth ✓ Predictable ✓ Reactive ✓ Testable ✓ Offline First ✓ Engine Driven

---

# Five-Layer State Hierarchy

```
App State         App 生命周期（Current Career / Theme / Language / Network）
World State       Career 生命周期（Season / Week / Tournament / Ranking / Calendar / News）
Feature State     功能拥有（Training Result / Recovery Progress / Match State）
View State        页面状态（Loading / Success / Empty / Error）
Temporary State   UI 临时（Sheet / Tab / Scroll / Keyboard）→ 退出即释放
```

---

# State Ownership（唯一 Owner）

| State | Owner |
|-------|-------|
| Player | Player Engine |
| Career | Career Engine |
| Ranking | Ranking Engine |
| Match | Match Engine |
| Tournament | Tournament Engine |
| News | Story Engine |
| Calendar | World Engine |
| Save | Save Engine |

---

# 关键规则

- **Mutation Rules**：只有 Engine 能修改状态（Button → Engine → State，不是 Button → State）
- **Derived State 不保存**：Overall Rating / Power Ranking / Form / Prediction / Win Rate 全部实时计算
- **Observable 限制**：建议只有 AppState / WorldState / TodayState / CareerState 为 Observable，避免 2200 名球员全部刷新
- **Cache Policy**：Today / Career Summary / Top100 / News Feed 允许缓存；Player Ability / Ranking Points / Fatigue / Confidence 禁止缓存

---

# 状态变化流程

```
Engine → Repository → Database → Published → ViewModel → View
```

任何 View 禁止直接监听 Database。

---

# Snapshot & Undo

推进 Week 前自动生成 Snapshot。失败自动恢复。所有修改经过 Command，未来支持 Undo。

---

# Thread Safety

状态更新：Main Actor。后台计算：Engine Queue。禁止多线程同时修改 Player。

---

# Performance

- State Update <5ms
- Today Refresh <16ms
- Ranking Refresh <30ms
- Week Advance 无掉帧

---

# Definition of Done

✓ 所有状态唯一拥有者 ✓ UI 不保存业务状态 ✓ Engine 唯一修改状态

✓ ViewModel 仅负责展示 ✓ Derived State 不存储 ✓ Event 自动刷新 ✓ 支持 Undo/Snapshot

---

# Final Principle

状态不是数据的副本。状态就是当前世界的真实状态。

任何人、任何页面、任何系统，都应该看到同一个世界。

---

End of Document
