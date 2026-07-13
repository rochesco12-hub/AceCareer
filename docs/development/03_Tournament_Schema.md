# Ace Career Development Bible
# 03 · Tournament Schema

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Tournament 是整个职业网球世界最重要的比赛实体。

它不仅仅代表一项赛事。

它还是 Ranking / Prize Money / News / Career History / Match Engine / World Simulation 的核心节点。

Tournament 不负责模拟比赛。

Tournament 只描述：**这项赛事是什么。**

---

# Design Goals

✓ 支持 ATP 全赛历 ✓ Challenger ✓ ITF

✓ 未来 WTA ✓ 双打 ✓ Team Event ✓ 多年历史

---

# Tournament Architecture（12 个模块）

```
Tournament
├── Identity         官方名称/缩写/赛事代码/赛季/届数
├── Classification   等级/场地/环境/签表规模
├── Schedule         周次/开始/截止/抽签/资格赛/正赛/决赛日期
├── Venue            国家/城市/球场/时区/海拔
├── Entry            报名（Accepted/Qualifying/Alternate/Wildcard/Withdrawal）
├── Draw             签表结构（种子/签位/当前轮次）
├── Rules            赛制（三盘两胜/五盘三胜/抢七/Super Tie-break）
├── Points           各轮积分（全部读取 Config）
├── PrizeMoney       各轮奖金（全部读取 Config）
├── Status           当前阶段（Entry/Qualifying/Round1/Quarterfinal/Completed）
├── Statistics       赛事级统计（场次/Ace/最长比赛/最快发球）
└── Metadata         系统字段
```

---

# Tournament Lifecycle

Created → Entry Open → Acceptance → Draw → Qualifying → Main Draw → Final → Ranking Update → Archive

---

# Key Rules

- Tournament **不保存**：Player Ability / Ranking List / Career / News Content / Simulation / Probability
- Points / Prize / Rules / Draw Size 全部来自 Config，Tournament 只保存引用
- 赛事结束后生成 Archive（冠军/签表/统计/排名）永久保存

---

# Relationships

Tournament → Entry → Draw → Match → Ranking → News → History → Career

---

# Future Expansion

✓ ATP ✓ WTA ✓ Challenger ✓ ITF ✓ Olympics ✓ Davis Cup ✓ Laver Cup ✓ Doubles ✓ Mixed

---

# Performance

- Tournament Query <10ms
- Draw Generation <30ms
- Archive 永久保存
- 支持 100+ 年历史

---

# Definition of Done

✓ Tournament 拆分为 12 个模块 ✓ Draw 与 Match 分离 ✓ Config 与数据分离

✓ 生命周期完整 ✓ 支持未来所有赛事类型 ✓ 支持百年历史存档

---

# Final Principle

Tournament 不是一组比赛。

Tournament 是整个职业网球世界在某一周发生的一次历史事件。

每一届赛事都会永久留在这个世界的历史中。

---

End of Document
