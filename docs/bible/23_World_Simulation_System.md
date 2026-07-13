# Ace Career Game Design Document
## Living World Simulation System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

World Simulation System（世界模拟系统）负责驱动整个 Ace Career 世界。

玩家并不是世界中心。

即使玩家连续一年没有参加任何比赛，整个职业网球世界仍然会继续发展。

所有 AI 球员、赛事、排名、新闻、赞助、退役、新秀都由本系统驱动。

---

# 2. Design Goal

World Simulation 必须做到：

- 世界持续运行
- 玩家不是唯一主角
- AI 拥有完整职业生涯
- 世界每天（每周）都在变化
- 每一年都与上一年不同
- 支持无限 Career

---

# 3. Core Philosophy

整个世界由 AI 驱动。

不是：

玩家推动世界。

而是：

玩家加入世界。

例如：

玩家没有参加澳网。

澳网仍然：

正常举办。

冠军照常产生。

世界第一照常变化。

新闻照常更新。

---

# 4. World Update Pipeline

每进入新的 Week：

执行：

```text
Calendar Update
↓
Tournament Update
↓
AI Decisions
↓
Match Simulation
↓
Ranking Update
↓
Financial Update
↓
Media Update
↓
History Update
↓
Auto Save
```

所有世界事件：

必须按照固定顺序。

---

# 5. AI Population

世界拥有固定职业球员数量。

默认：

```text
ATP Tour
250
Challenger
400
ITF
800
Junior
600
Total
2050 Players
```

未来：

支持动态数量。

---

# 6. Player Lifecycle

每位 AI 都拥有完整生命周期：

```text
Junior
↓
Professional
↓
Peak
↓
Veteran
↓
Retired
↓
Hall of Fame
```

不是：

固定存在。

---

# 7. Retirement

AI 到达：

退役条件：

自动进入：

Retirement。

判断依据：

- 年龄
- 排名
- 收入
- 伤病
- Motivation

退役：

永久退出巡回赛。

---

# 8. New Generation

每年：

自动生成：

新秀。

包括：

姓名。

国籍。

身高。

打法。

潜力。

人格。

成长速度。

世界不会：

越来越少人。

---

# 9. Country Distribution

新秀：

按照国家比例生成。

例如：

Spain

Italy

USA

France

Australia

Japan

China

Argentina

保持：

世界格局真实。

---

# 10. Dynamic Strength

不同年代：

国家实力：

允许变化。

例如：

未来：

中国。

拥有：

大量 Top100。

也可能：

西班牙：

黄金一代结束。

世界：

自然演化。

---

# 11. AI Rivalries

AI 自动形成：

宿敌。

例如：

Alcaraz

vs

Sinner

连续：

12 次交手。

新闻：

自动报道。

未来：

加入：

Head To Head。

---

# 12. AI Career Records

每位 AI：

永久保存：

冠军数。

胜率。

Career High。

奖金。

大满贯。

退役后：

进入：

History。

---

# 13. Dynamic History

每一年：

都会新增：

历史。

例如：

2034

French Open Champion

↓

History。

不会覆盖。

不会删除。

---

# 14. World News

世界新闻：

来源：

AI。

例如：

世界第一更换。

ATP500 爆冷。

17岁新秀首冠。

传奇退役。

玩家：

只是新闻的一部分。

---

# 15. Economy Evolution

世界奖金：

允许：

缓慢上涨。

例如：

2038。

ATP250：

奖金：

上涨：

6%。

增强：

时代变化。

---

# 16. Hall of Fame

退役球员：

自动进入：

Hall of Fame。

保存：

Career：

全部数据。

未来：

玩家可以查看：

任何传奇。

---

# 17. Historical Timeline

系统自动生成：

```text
2026
↓
2027
↓
2028
↓
...
2045
```

每一年：

拥有：

冠军。

排名。

新闻。

纪录。

世界真正拥有历史。

---

# 18. World Database

```text
World
Season
Week
Players
Tournaments
News
History
RetiredPlayers
JuniorPlayers
HallOfFame
```

整个 Career：

只有：

一个 World。

---

# 19. Edge Cases

支持：

- 世界第一退役
- 同年多人退役
- Grand Slam 取消（未来）
- 新秀大量涌现
- 黄金一代结束
- AI 长期伤病
- AI 长期统治

---

# 20. Acceptance Criteria

✓ 世界不会停止

✓ 玩家不是世界中心

✓ AI 完整职业生涯

✓ 每年自动生成新秀

✓ 每年自动有人退役

✓ 历史永久保存

✓ Hall of Fame 正常建立

✓ 支持 50+ Season

---

End of Document
