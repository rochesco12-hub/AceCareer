# Ace Career UI V2 · Phase 4 — Implementation Spec

Version: 1.0
Status: Ready for Codex
Priority: P0

---

## 一、阶段目标

建立在 Phase 1-3 已完成基础上，解决"功能完整但玩家是否真正感受到职业生涯正在发展"的问题。核心不是增加玩法，而是把已有数据、事件和结果以更有游戏感的方式呈现。

---

## 二、四大反馈等级

| Level | 示例 | 反馈方式 |
|-------|------|----------|
| 1 — 普通状态 | 训练完成/装备升级/排名小幅上升/签约普通员工 | Toast + 轻量 Haptic + 数值高亮 |
| 2 — 重要事件 | 首获积分/首进排名/首签赞助/首签教练/奖金突破 | 中型 Bottom Sheet |
| 3 — 重大里程碑 | 职业首胜/首冠/首进Top100/Top500/首胜Top10/首个ATP冠/世界第一 | 专用里程碑全屏卡片 + 写入时间轴和荣誉 |
| 4 — 历史级成就 | 大满贯冠军/年终总决赛/年终No.1/全满贯/破世界纪录 | 完整成就页 + 世界新闻 + 时间轴重点标记 |

**禁止**：粒子雨/金币爆炸/赌场式反馈

---

## 三、职业里程碑系统（CareerMilestone）

八分类：起步 / 排名 / 赛事 / 冠军 / 对手 / 商业 / 生涯 / 历史

规则：
- 基于真实游戏状态触发
- 每项只触发一次
- 记录赛季 + 周数
- 有比赛关联时记录赛事/轮次/对手/比分
- 写入存档不重复弹出

```swift
struct CareerMilestone: Codable, Identifiable {
    let id: String; let type: CareerMilestoneType
    let achievedSeason: Int; let achievedWeek: Int
    let title: String; let summary: String
    let eventID: String?; let opponentID: String?
    let rankingValue: Int?; let createdAt: Date
    var hasBeenPresented: Bool
}
```

---

## 四、生涯时间轴

**入口**：生涯 → 荣誉与纪录 → 生涯时间轴

**记录**：创建/首胜/首积分/排名突破/冠军/重伤+复出/重要签约/年终排名/奖项/退役

**不记录**：普通训练/恢复/报名/每周排名波动/普通比赛

按赛季分组 + Bottom Sheet 筛选（全部/排名/赛事/冠军/商业/伤病/赛季）

---

## 五、荣誉陈列室

**入口**：生涯 → 荣誉与纪录 → 荣誉陈列室

```
荣誉摘要 Hero（冠军总数/最高级别/大满贯数/重要奖项数）
↓
冠军分类（按级别分组：大满贯→年终→大师赛→ATP500→250→挑战赛→ITF）
↓
奖项（年度最佳/最佳新秀/复出/年终No.1/最佳进步 — 数据支持才展示）
```

同一赛事多次夺冠不重复创建大卡片。

---

## 六、世界纪录与个人纪录

**入口**：生涯 → 荣誉与纪录 → 纪录（个人/世界 Segment）

- **个人**：最高排名/最长连胜/单赛季最多冠/最佳大满贯成绩...
- **世界**：纪录名称 + 保持者 + 数值 + 赛季 + 玩家差距

**关键规则**：现实历史纪录与模拟世界纪录必须明确分开，不能把现实初始数据与模拟结果混在一起。

打破纪录时生成 Level 4 反馈 + 世界动态 + 时间轴事件。

---

## 七、赛季总结（SeasonSummary）

每个赛季结束自动生成一次，写入存档永久固定。

九部分：赛季身份页 → 年终排名 → 赛季战绩 → 赛事表现 → 最佳比赛(确定性规则) → 排名变化(趋势图) → 奖金与商业 → 训练与身体 → 赛季里程碑 → 世界背景 → 下一赛季展望

**不依赖在线 AI**，使用确定性模板系统（`SeasonPerformanceTrend` enum + 模板文案，插入真实数据）。

---

## 八、比赛周体验

```
普通周 → 比赛准备(赛事卡片升级Hero) → 比赛日(Continue→开始比赛)
→ 赛后结算 Sheet(结果/积分/奖金/体能/信心/伤病/里程碑)
→ 赛事结束总结(最终轮次/战绩/积分/奖金/最高排名对手/排名预测) → 返回普通周
```

---

## 九、排名变化反馈

- 普通 → Toast/首页状态卡
- 大幅 → 阈值规则（Top500外>100位/500内>50位/100内>10位）→ Level 2 Sheet
- 突破阶段 → Level 3 里程碑
- 下降 → 仅关键情况提醒（跌出Top100/50/10/失去No.1/积分大量到期）必须说明原因

---

## 十、关键操作反馈

签约/升级/赞助/目标完成 → 统一格式反馈 → 首份赞助/首签教练触发里程碑。

---

## 十一、世界重大事件

大满贯冠军/No.1变化/重要退役/破纪录/历史级连胜/年终排名/重大伤病/玩家里程碑 → 统一 WorldEvent 数据对象 → 同步进入世界/今日/赛季总结/球员详情/纪录页。

**相关性排序**：玩家 > 即将对手 > 所在赛事 > 排名相近竞争者 > 世界顶级 > 普通新闻。

---

## 十二、真实球员历史保护

- 现实历史基线字段（只读）：`realWorldCareerTitles / realWorldGrandSlamTitles / realWorldHighestRanking / realWorldWeeksAtNumberOne`
- 游戏新增字段（读写）：`simulationCareerTitles / simulationCareerWins`
- 不得覆盖现实数据 / 不得把现实冠军清零 / 不得把游戏首胜称为"职业首冠"

---

## 十三、新增组件（14个）

ACMilestoneCard / ACMilestonePresentation / ACTimelineRow / ACTimelineMajorCard / ACTrophySummaryCard / ACTrophyCard / ACRecordRow / ACSeasonSummaryPage / ACResultSummarySheet / ACRankingChangeView / ACEventFeedbackToast / ACAchievementBanner / ACWorldEventHero / ACStatChangeRow

---

## 十四、GameFeedbackCoordinator

统一管理：接收事件→排序→去重→决定展示方式→控制队列→标记已展示

展示优先级：比赛结果→重大伤病→里程碑→排名突破→合同升级→普通提示

**不同时弹出多个 Sheet。**

---

## 十五、文件结构

```
CareerExperience/
├── Milestones/（4 文件）
├── Timeline/（4 文件）
├── Honors/（4 文件）
├── SeasonSummary/（4 文件）
├── Feedback/（4 文件）
└── WorldEvents/（3 文件）
```

---

## 十六、动画规范

- 普通反馈 0.15-0.25s / 重要反馈 0.3-0.5s / 里程碑 ≤0.8s
- 禁止：闪烁/彩纸/粒子/金币音效/不可跳过动画/自动播放BGM
- 支持 Reduce Motion

---

## 十七、验收标准（38 项）

核心要点：
1. 不改变 Phase 1-3 页面结构
2. 里程碑不重复触发 + 包含赛季/周数
3. 时间轴不记录普通训练/报名
4. 同一赛事多冠不重复大卡片
5. 现实/模拟纪录明确分开
6. 赛季总结固定保存 + 不依赖 AI
7. 最佳比赛来自确定性规则
8. 赛后统一结算 Sheet
9. 世界新闻优先展示玩家相关
10. 真实球员保留历史冠军/纪录
11. 反馈队列不冲突
12. 旧存档正常打开 + Reduce Motion 可用

---

## 十八、实施顺序（20 步）

1. 梳理数据 → 2. 区分现实/模拟历史 → 3. WorldEvent 模型 → 4. CareerMilestone 模型 → 5. GameFeedbackCoordinator → 6. 赛后反馈 → 7. 排名变化反馈 → 8. 操作反馈 → 9. 生涯时间轴 → 10. 荣誉陈列室 → 11. 个人纪录 → 12. 世界纪录 → 13. 赛季总结生成器 → 14. 赛季总结页面 → 15. 今日世界摘要排序 → 16. 世界动态事件展示 → 17. 旧存档迁移 → 18. 验证真实球员履历 → 19. 适配 → 20. 回归测试

---

End of Document
