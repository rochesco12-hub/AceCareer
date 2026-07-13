# Ace Career Game Design Document
## Core Game Design Principles

Version: 1.0
Status: Final
Priority: P0

---

# 1. Purpose

本文件不是功能文档。

它定义 Ace Career 整个游戏的设计哲学。

未来所有新增功能，都必须符合这里的原则。

如果某个功能违反了本文件。

则必须修改功能。

而不是修改原则。

---

# 2. Core Vision

Ace Career 不是一个：

网球比赛游戏。

它是一款：

职业网球运动员模拟器（Professional Tennis Career Simulator）。

玩家体验的是：

职业生涯。

不是一场比赛。

比赛只是职业生涯的一部分。

---

# 3. First Principle

## 世界先于玩家存在（World First）

世界不是因为玩家才开始运行。

玩家进入游戏时：

世界已经存在。

ATP 已经进行了很多年。

已经有：

- 世界第一
- Grand Slam 冠军
- ATP Rankings
- 历史纪录
- 伟大球员

玩家只是加入这个世界。

---

# 4. Second Principle

## 玩家不是唯一主角（Player Is Not The Center）

所有 AI：

拥有完整职业生涯。

包括：

- 报名
- 比赛
- 成长
- 伤病
- 退役
- 新闻
- Rival
- Legacy

玩家失败。

世界继续。

玩家退役。

世界继续。

---

# 5. Third Principle

## 决策比点击重要（Decision Over Action）

Ace Career 的乐趣：

来自决策。

不是操作。

例如：

是否参加 ATP250。

是否放弃法网资格赛。

是否休息一周。

是否更换教练。

这些决定。

比打一场比赛更重要。

---

# 6. Fourth Principle

## 每一周都必须有意义（Every Week Matters）

任何 Week。

玩家都必须拥有：

至少一个重要决定。

例如：

报名。

训练。

恢复。

旅行。

资金。

团队。

不能出现：

连续点击：

继续下一周。

没有任何思考。

---

# 7. Fifth Principle

## 长期规划优于短期收益（Long-Term Strategy）

真正职业球员：

规划的是：

整个赛季。

不是：

下一场比赛。

因此：

玩家需要考虑：

- 保分
- 疲劳
- Grand Slam
- 排名
- 旅行
- 训练周期

---

# 8. Sixth Principle

## 没有唯一正确答案（No Perfect Strategy）

任何选择：

都有代价。

例如：

连续参赛。

获得：

奖金。

积分。

同时：

疲劳增加。

受伤风险增加。

休息。

恢复健康。

但：

可能失去积分。

不存在：

100% 最优路线。

---

# 9. Seventh Principle

## 数据驱动世界（Simulation First）

所有世界事件：

必须来自：

模拟。

例如：

新闻。

不是随机生成。

而是：

因为：

世界第一输球。

因此：

生成新闻。

而不是：

先生成新闻。

---

# 10. Eighth Principle

## 玩家必须感受到成长（Visible Progress）

成长不仅体现在：

Overall。

还体现在：

- 排名
- 奖金
- 球队
- Rival
- 新闻
- Hall of Fame
- Legacy

职业生涯：

始终拥有反馈。

---

# 11. Ninth Principle

## 失败也是游戏内容（Failure Is Gameplay）

失败：

不会结束游戏。

例如：

首轮出局。

掉出 Top100。

长期伤病。

资金紧张。

这些都会产生：

新的职业故事。

失败：

也是 Career 的一部分。

---

# 12. Tenth Principle

## 所有系统互相影响（Everything Is Connected）

例如：

训练

↓

疲劳

↓

伤病

↓

退赛

↓

积分减少

↓

排名下降

↓

无法报名 Masters

↓

收入下降

↓

无法聘请高级教练

↓

成长变慢

整个系统：

形成闭环。

---

# 13. UX Principles

Today 页面：

始终保持：

单屏完成。

玩家打开 App：

3 秒内知道：

- 当前 Week
- 当前目标
- 下一场比赛
- 当前状态

无需进入多个页面。

---

# 14. Design Red Lines

禁止：

- 无限成长
- 无限体力
- 无限资金
- 玩家主角光环
- AI 作弊
- 随机决定比赛
- 没有代价的选择

任何违反：

必须重构。

---

# 15. Definition of Success

Ace Career 成功的标准不是：

玩家拿到所有冠军。

而是：

十年以后。

玩家还能记得：

"2034 年那次肩伤毁掉了我的赛季。"

"我和辛纳打了 27 次。"

"我为了保住 Top100 放弃了法网资格赛。"

如果玩家能记住这些故事。

那么：

Ace Career 就成功了。

---

# Acceptance Criteria

✓ 所有新增系统符合本设计原则

✓ 玩家拥有持续决策

✓ 世界独立运行

✓ 长期 Career 始终有意义

✓ 失败能够创造新的故事

✓ 玩家体验的是职业生涯，而不是单场比赛

---

End of Document
