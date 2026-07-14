# Ace Career UI V2 · Phase 1 — Implementation Spec

Version: 1.0
Status: Ready for Codex
Priority: P0

---

## 一、阶段目标

本阶段完成：

1. 重构「今日」首页的信息层级与操作逻辑
2. 建立全局统一的 Header、Section、Card、Button 组件
3. 优化「继续下一周」的固定操作区
4. 减少重复信息与无效按钮
5. 保留现有功能和数据逻辑，只调整 UI 结构、组件和交互入口

**本阶段不要修改：** 周推进逻辑、训练/恢复计算、赛事报名规则、比赛预测、世界模拟、存档结构、玩家属性、真实球员数据。

---

## 二、统一设计基础

### 1. 页面背景

- 页面背景：`Color(.systemGroupedBackground)` 或项目现有浅灰背景
- 卡片背景：白色或 `secondarySystemGroupedBackground`
- 主文字：接近黑色
- 次级文字：系统灰色
- 强调色：继续使用当前绿色
- 不新增蓝色/紫色/橙色等独立主题色

### 2. 间距规范

```swift
页面左右边距：16pt（大屏幕不扩大）
Section 垂直间距：24pt
卡片垂直间距：12pt
卡片内部标准 Padding：16pt
小型紧凑卡片：12pt
```

### 3. 圆角三档

```swift
smallRadius  = 10  // 标签、状态 Badge
mediumRadius = 16  // 普通卡片、按钮
largeRadius  = 22  // Hero Card、Bottom Sheet
```

### 4. 边框与阴影

```swift
borderColor   = Color.primary.opacity(0.06)
borderWidth   = 1
shadowOpacity = 0.04
shadowRadius  = 8
shadowY       = 2
```

---

## 三、统一组件

### 1. ACPageHeader

- **dashboard** 样式（仅今日）：赛季 / 周数 / 当前巡回赛层级 / 当前世界排名
- **compact** 样式（普通页面）：标题 + 可选副标题 + 可选右侧按钮

```swift
enum ACPageHeaderStyle { case dashboard, compact }
struct ACPageHeader: View {
    let style: ACPageHeaderStyle
    let title: String
    let subtitle: String?
    let trailingContent: AnyView?
}
```

### 2. ACSectionHeader

```swift
struct ACSectionHeader: View {
    let eyebrow: String?   // 小号加粗绿色/次级色
    let title: String      // Headline
    let subtitle: String?  // Caption / Footnote
}
```

### 3. ACCard

所有首页内容卡片统一容器。统一处理背景/圆角/描边/阴影/内边距/点击态。支持 `isInteractive`（按下缩放至 0.985 + 透明度轻微变化）。

```swift
struct ACCard<Content: View>: View { let content: Content }
```

### 4. ACPrimaryButton

- 高度 54pt / 圆角 16pt / 背景深色或当前主绿色
- 支持 Loading、Disabled

```swift
struct ACPrimaryButton: View {
    let title: String; let icon: String?
    let isLoading: Bool; let isDisabled: Bool
    let action: () -> Void
}
```

### 5. ACSecondaryButton

- 高度 40~44pt / 白底或浅灰底 / 描边
- 不与主按钮竞争视觉优先级

### 6. ACStatusBadge

用于 ITF/ATP/硬地/已报名/待处理/轻度疲劳/状态良好。所有 Badge 统一组件。

### 7. ACMetricItem

结构：数值/状态 → 名称 → 可选趋势。支持进度条和文本状态两种形式。

---

## 四、今日首页布局

严格顺序：

```
Dashboard Header
↓
下一站赛事
↓
本周计划
↓
状态概览
↓
待处理事项（无可隐藏）
↓
世界摘要
↓
底部固定 Continue
```

---

## 五、各模块要点

### Dashboard Header
```
2026 赛季 · 第 28 周                    NR
职业巡回赛                         世界排名
```
- 高度明显低于当前版本
- 排名是辅助状态
- 不出现大空白

### 下一站赛事卡片
赛事名称 / 城市国家 / 级别 Badge / 场地 Badge / 倒计时 / 报名状态 → 点击进入对应流程。**删除首页"报名赛事"快捷按钮。**

### 本周计划卡片
已用/总时间槽 + 摘要 + 未安排提醒 → 点击进入训练恢复安排。**删除"安排训练/开始恢复"独立按钮。**

### 状态概览卡片
体能 / 疲劳 / 信心 / 近期状态 → 2×2 Grid 一张大卡片。不分别套白卡片。

### 待处理事项
紧凑列表卡片（最多首页 3 项，超量显示"查看全部 N 项"）。

### 世界摘要
最多 2~3 条重要动态。**不显示完整新闻 Feed。**

---

## 六、Continue 固定操作区

- 固定在底部 Tab Bar 上方（半透明/Material/分隔线/按钮）
- 文案：默认"继续下一周"，关键事件时动态调整
- 前置校验：
  - 无阻塞 → 直接推进 Loading
  - 普通提醒 → 确认 Sheet
  - 必须处理 → 按钮变为"完成本周安排"，跳转对应模块
- 处理 Tab Bar 高度 / Home Indicator / 键盘 / 小屏 / Dynamic Type

---

## 七、滚动与布局

```swift
ScrollView + LazyVStack
.padding(.bottom, continueBarHeight + 24)
```

不写死屏幕高度。

---

## 八、动画与反馈

- 允许：卡片按压缩放 / Section 淡入 / 数字过渡 / Continue Loading / Sheet 弹出
- 禁止：弹跳/旋转/粒子/连续卡片动画/自动轮播
- 周推进成功后：轻量 `.success` Haptic

---

## 九、无障碍与适配

支持：Dynamic Type / VoiceOver / Dark Mode / iPhone SE / 大屏 / 中文长文本 / NR/四位数排名/五位数积分。

不通过固定 Frame 压缩文字。

---

## 十、组件文件结构

```
DesignSystem/
├── ACTokens.swift, ACColors.swift, ACTypography.swift, ACSpacing.swift
├── ACCard.swift, ACPageHeader.swift, ACSectionHeader.swift
├── ACPrimaryButton.swift, ACSecondaryButton.swift
├── ACStatusBadge.swift, ACMetricItem.swift, ACContinueBar.swift

Today/
├── TodayDashboardView.swift, TodayDashboardViewModel.swift
├── NextEventCard.swift, WeeklyPlanCard.swift, PlayerStatusCard.swift
├── PendingActionsCard.swift, WorldSummaryCard.swift
```

---

## 十一、数据兼容

新增 `TodayDashboardViewModel` 只负责聚合展示，不复制业务计算。实际训练/报名/推进仍调用原有 Service。

---

## 十二、验收标准

1. 首页不再出现四个独立快捷按钮
2. 卡片顺序明确（下一站→计划→状态→待办→世界）
3. Continue 固定底部不随滚动消失
4. Continue 不遮挡 Tab Bar 或内容
5. Header 高度明显降低
6. 所有卡片使用统一组件
7. 无多套圆角/边距/按钮样式
8. 训练/恢复/报名/预测功能正常可进入
9. 周推进逻辑与改版前一致
10. 小屏无横向溢出
11. 无数据模块正确隐藏
12. Light/Dark Mode 基础显示正常
13. 无重复业务逻辑
14. 不修改已有存档字段
15. 编译通过，无 SwiftUI Preview/Runtime 警告

---

## 十三、实施顺序

1. Design Token → 2. 基础组件 → 3. Dashboard Header → 4. 下一站赛事卡片 → 5. 本周计划卡片 → 6. 状态概览卡片 → 7. 待处理事项 → 8. 世界摘要 → 9. 固定 Continue Bar → 10. 接回现有业务逻辑 → 11. 删除旧快捷操作栏 → 12. 适配小屏/Dark Mode → 13. 回归测试

完成 Phase 1 验收后再开始 Phase 2。

---

End of Document
