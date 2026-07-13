# Ace Career Development Bible
# 02 · Player Schema

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Player 是整个 Ace Career 最核心的数据模型。

整个职业世界的所有系统：

Match Engine / Ranking / Training / Coach / News / World Simulation / Career / Statistics

最终都围绕 Player 运转。

Player 不应该是一个巨大的 God Object，而应该由多个独立子模型组成。

---

# Design Goals

✓ 单一职责 ✓ 可扩展 ✓ 易同步 ✓ 易缓存

✓ 支持 AI Player ✓ 支持 Human Player ✓ 支持未来 Online Career

Player 只保存状态，不保存业务逻辑。

---

# Player Architecture（13 个模块）

```
Player
├── Identity         永久不变（姓名/国籍/持拍/出生日期）
├── Biography        展示用（身高/体重/出生地/头像）
├── Attributes       真实能力（0~100：发球/正手/反手/接发/截击/切削/移动/耐力/心理/网前）
├── Ratings          Engine 自动计算（Overall/Hard/Clay/Grass/Indoor/Potential）
├── Physical         动态状态（Fitness/Fatigue/InjuryRisk/Recovery）
├── Mental           心理状态（Confidence/Focus/Morale/Pressure/Consistency）
├── Career           职业摘要（排名/冠军/大满贯/胜场/赛季）
├── Competition      当前赛事（TournamentID/Round/Seed/Opponent）
├── Statistics       累计统计（胜率/Ace/破发点/一发得分率）
├── Coach            当前教练引用
├── Finance          职业收入（奖金/赞助/旅行/教练/医疗）
├── Preferences      AI 使用（偏好场地/风险等级/训练风格）
└── Metadata         系统字段（创建时间/是否人类/是否退役）
```

---

# Key Rules

- **Player 不保存**：Match / Tournament / Ranking List / News / History / Config / Engine 数据
- **Calculated Fields 动态计算**：Overall / Current Form / Surface Rating / Power Ranking / Tournament Prediction — 禁止持久化
- **所有外部对象均以 ID 引用**，禁止复制完整对象
- **数据库索引建议**：playerId / currentRanking / nationality / age / isHuman / isRetired

---

# Read/Write Flow

- **Read**：Today 页面按需读取 Competition / Physical / Career / Coach / Statistics
- **Write**：Match Engine → Career Engine → Player Update → Database → UI Refresh
- **View 永远不能修改 Player**

---

# Future Expansion

支持 WTA / Doubles / Mixed / Junior / Legends / Online Player — 无需修改 Root Schema。

---

# Breaking Changes

playerId / Identity / Relationship Structure / Module Names / Root Layout 禁止修改。

---

# Definition of Done

✓ Player 拆分为 13 个模块 ✓ 无 God Object ✓ 数据无重复

✓ Engine 与数据分离 ✓ 支持 Offline First ✓ 支持未来 Online

---

# Final Principle

Player 不是一个对象。

Player 是一个完整职业生涯在当前时刻的快照。

所有成长、荣耀、失败，都只是这个快照不断演化的过程。

---

End of Document
