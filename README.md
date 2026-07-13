# Ace Career

> **Build the World First. Let the Career Tell the Story.**

职业网球运动员模拟器（Professional Tennis Career Simulator）。玩家体验的不是一场比赛，而是一整个职业生涯。世界不围绕玩家旋转——AI 球员会成长、受伤、夺冠、退役，历史会不断书写。

---

## 项目状态

```
Ace Career Engine v1.0
Status: Foundation Complete → Implementation Phase
```

---

## 文档结构

完整的 36 章 Game Design Document（Ace Career Bible）：

### 核心引擎（P0）
| # | 系统 | 说明 |
|---|------|------|
| 01 | ATP Calendar | 世界时间引擎，唯一时间来源 |
| 02 | Tournament Generation | 赛事生成系统 |
| 03 | Entry System | 报名系统 + Eligibility Engine |
| 04 | Acceptance List | 参赛名单系统 |
| 05 | Qualifying | 资格赛系统 |
| 06 | Draw System | 抽签系统 |
| 07 | Seeding | 种子系统 |
| 08 | Match Week | 比赛周系统 |
| 09 | Points & Prize Money | 积分与奖金系统 |
| 10 | News & Media | 新闻媒体系统 |
| 11 | AI Tournament Logic | AI 赛事决策系统 |
| 12 | Player Decision | 玩家决策系统 |
| 13 | State Machine | 全局状态机 |
| 14 | Data Model | 全局数据模型 |
| 15 | Test Cases | 测试与验证标准 |

### 玩法系统（P1）
| # | 系统 | 说明 |
|---|------|------|
| 16 | Economy System | 经济系统 |
| 17 | Training System | 训练系统 |
| 18 | Injury System | 伤病与恢复系统 |
| 19 | Coach & Team | 教练团队系统 |
| 20 | Match Simulation | 比赛模拟系统 |
| 21 | Player Progression | 球员成长系统 |
| 22 | Player Attributes | 球员属性系统 |

### 世界持久化
| # | 系统 | 说明 |
|---|------|------|
| 23 | World Simulation | 世界模拟系统 |
| 24 | Save & Load | 存档系统 |
| 25 | Rookie Generation | 新秀生成系统 |
| 26 | Rivalry & Legacy | 宿敌与传奇系统 |
| 27 | Endgame System | 退役终局系统 |

### 基础设施
| # | 系统 | 说明 |
|---|------|------|
| 28 | Mod System | 世界配置系统 |
| 29 | Game Balance | 全局平衡系统 |
| 30 | Roadmap | 开发路线图 |
| 31 | Development Guidelines | 开发规范 |
| 32 | Design Principles | 核心设计原则 |
| 33 | Content Expansion | 内容扩展路线 |
| 34 | Future Backlog | 未来扩展规划 |
| 35 | Release Checklist | 发布检查清单 |
| 36 | Appendix | 命名规范与设计标准 |

---

## 核心设计原则

1. **世界先于玩家存在（World First）** — 玩家加入一个已经在运行的世界
2. **玩家不是唯一主角** — AI 拥有完整职业生涯
3. **决策比点击重要** — 乐趣来自职业规划，不是操作
4. **每一周都必须有意义** — 不存在"空白周"
5. **长期规划优于短期收益** — 赛季规划 > 单场比赛
6. **没有唯一正确答案** — 所有选择都有代价
7. **数据驱动世界** — 新闻来源于真实模拟，不是随机生成
8. **失败也是游戏内容** — 伤病、连败、排名下滑产生故事
9. **所有系统互相影响** — 训练→疲劳→伤病→退赛→排名下降→...
10. **玩家体验职业生涯，不是单场比赛**

---

## Phase 1 — Core Engine（开发中）

目标：建立可连续模拟 10+ 赛季的职业网球世界。

---

## 技术方向

- 首选原型：本地 Web App（TypeScript / React / Next.js）
- 未来集成：Ace League iOS App 内置 Career Mode
- 模拟引擎：规则驱动，AI 仅用于新闻和自然语言理解
- 存档：本地 JSON，支持云端同步

---

## 相关仓库

- [AceLeague](https://github.com/rochesco12-hub/AceLeague) — 网球赛事管理 iOS App

---

## 许可

Private — All Rights Reserved
