# Ace Career Game Design Document
## Appendix · Constants, Naming Convention & Design Standards

Version: 1.0
Status: Final
Priority: Reference

---

# 1. Purpose

本文件作为整个 Ace Career GDD 的附录。

它统一规定：

- 名词定义
- 命名规范
- 枚举规范
- 文件规范
- 数据规范
- UI 规范
- 设计约束

所有文档均默认遵守本附录。

---

# 2. Naming Convention

所有系统统一采用英文命名。

例如：

```text
Career
Season
Week
Tournament
Entry
Acceptance
Draw
Match
Ranking
Training
Recovery
Health
Coach
Finance
News
Legacy
HallOfFame
```

禁止：

同一对象出现多个名称。

例如：

Ranking

×

Leaderboard

×

Standing

统一：

Ranking。

---

# 3. Week Standard

整个 Career 唯一时间单位：

```text
Season
↓
Week
```

禁止：

Day。

Month。

Hour。

作为主要时间推进单位。

日期：

仅作为展示。

---

# 4. World Standard

整个游戏：

只有：

一个：

World。

所有系统：

共享。

例如：

```text
World
↓
Calendar
↓
Tournament
↓
Ranking
↓
News
↓
History
```

不得：

创建：

多个世界。

---

# 5. Player Types

系统支持：

```text
Human Player
AI Player
Retired Player
Junior Player
```

未来：

支持：

Online Player。

---

# 6. Tournament Categories

统一：

```text
ITF
Challenger
ATP250
ATP500
Masters1000
Grand Slam
ATP Finals
Olympics
Davis Cup
```

新增赛事：

必须属于：

其中之一。

---

# 7. Surface Types

统一：

```text
Hard
Clay
Grass
Indoor Hard
```

未来：

扩展：

Carpet。

---

# 8. Difficulty Levels

统一：

```text
Easy
Normal
Hard
Legend
```

Difficulty：

影响：

AI 决策。

不是：

能力值。

---

# 9. Attribute Range

所有能力：

统一：

```text
1 ~ 99
```

禁止：

100。

禁止：

无限增长。

---

# 10. Fatigue Range

统一：

```text
0 ~ 100
```

推荐：

```text
0~30
Excellent
31~60
Normal
61~80
Fatigued
81~100
Critical
```

所有系统：

统一读取。

---

# 11. Confidence Range

统一：

```text
0~100
```

不会：

超过：

100。

---

# 12. Health States

统一：

```text
Healthy
Fatigued
Minor Injury
Moderate Injury
Major Injury
Treatment
Recovery
Match Ready
```

禁止：

新增：

重复状态。

---

# 13. Save Version

统一：

Semantic Version。

例如：

```text
1.0.0
1.1.0
2.0.0
```

不得：

使用：

整数版本。

---

# 14. UI Principles

整个 App：

遵循：

Apple Human Interface Guidelines。

核心原则：

- 单屏优先
- 少层级
- 高信息密度
- 大留白
- 一致性

Today：

永远：

单屏。

---

# 15. Color Rules

统一：

```text
Green
Positive
Blue
Information
Orange
Warning
Red
Danger
Gray
Inactive
```

避免：

同一种颜色。

多个含义。

---

# 16. Typography

统一：

标题：

Title

副标题：

Headline

正文：

Body

辅助信息：

Caption

禁止：

一个页面：

出现过多字号。

---

# 17. Icons

统一：

SF Symbols。

禁止：

混用：

第三方图标。

未来：

品牌 Logo。

除外。

---

# 18. File Naming Rules

统一：

```text
01_ATP_Calendar.md
02_Tournament_Generation.md
03_Entry_System.md
```

禁止：

中文文件名。

禁止：

空格。

---

# 19. Future Documents

后续新增 GDD：

继续编号。

例如：

```text
37_Online_Career.md
38_WTA_System.md
39_Doubles_System.md
```

不得：

修改：

已有编号。

---

# 20. Final Principle

Ace Career 所有系统最终必须遵循一句话：

> **Build the World First. Let the Career Tell the Story.**

玩家不是世界的创造者。

玩家只是世界中的一位职业球员。

真正的主角。

永远是这个不断演化的职业网球世界。

---

# End of Bible

Ace Career Engine v1.0

Total Documents

36

Status

Foundation Complete

Next Phase

Implementation

---

End of Document
