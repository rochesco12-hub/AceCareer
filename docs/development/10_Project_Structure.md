# Ace Career Development Bible
# 10 · Project Structure

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Project Structure 定义整个 Ace Career 的工程目录结构。

一个优秀的目录结构：不需要搜索文件，只看目录就知道代码应该写在哪里。

---

# Design Goals

✓ Feature First ✓ Engine 独立 ✓ UI 与业务分离 ✓ 模块低耦合 ✓ 多人协作 ✓ 五年以上开发

---

# Root Structure

```
AceCareer/
├── App/              应用入口（AppDelegate/Scene/Launch/DI/Environment）
├── Presentation/     UI（Views/Components/Navigation/Theme/Animation/Charts/Widgets/Watch）
├── Features/         功能模块（Today/Career/Tournament/Match/Training/Recovery/Coach/Ranking/News/Profile/Settings）
├── Engine/           核心算法（Match/Training/Recovery/Career/Ranking/Simulation/Story/Probability/Growth/Economy）
├── Repository/       数据访问（PlayerRepo/CareerRepo/RankingRepo/TournamentRepo/NewsRepo/SaveRepo/ConfigRepo）
├── Persistence/      本地存储（SwiftData/Migration/Cache/Snapshot/Backup）
├── Infrastructure/   系统层（CloudKit/Network/Notification/Calendar/AI/Analytics/Logging）
├── Shared/           公共代码（Extensions/Protocols/Utilities/Constants/CommonComponents/Helpers）
├── Config/           配置文件（Tournament/Ranking/Growth/Fatigue/Recovery/Training/Economy/AI/Narrative）
├── Resources/        资源（Localization/Fonts/Sounds/Templates）
├── Assets/           视觉资源（Images/Icons/Flags/Surface/Player/Trophies）
├── Scripts/          开发工具（GenerateConfig/Migration/Validation/Build/Export）
├── Tests/            测试（Engine/Feature/Repository/UI/Performance/Integration）
└── Documentation/    项目文档（Engine Bible/Gameplay Bible/Development Bible/Product/Design/Balance）
```

---

# Feature Template（每个 Feature 统一结构）

```
FeatureName/
├── Views/           SwiftUI 视图
├── ViewModels/      视图状态管理
├── Models/          Feature 专用模型
├── Components/      可复用子组件
├── Services/        Feature 专用服务
└── Tests/           单元测试
```

---

# Key Rules

- **PascalCase 目录命名**，禁止 `career_page` / `new folder`
- **一个文件一个类型**（Player.swift 不混放 Coach/Career）
- **Feature 独立**：Recovery 不依赖 Tournament，News 不依赖 Ranking
- **Shared Components**（PlayerCard/RankingCard/SurfaceBadge/CountryFlag）全部放 Shared
- **单目录不超过 30 个文件**，超过就继续拆
- **Design System 统一**：Color/Typography/Spacing/Radius/Animation 全局读取

---

# 依赖方向

```
Feature → Engine → Repository → Persistence
Presentation 禁止直接引用 Persistence
Engine 不引用 SwiftUI
```

---

# 编译顺序

Shared → Config → Persistence → Repository → Engine → Features → Presentation → App

---

# 未来扩展（WTA 示例）

只增加 `Features/WTA` + `Engine/WTA` + `Config/WTA`，无需修改已有结构。

---

# Definition of Done

✓ Feature First ✓ Engine 独立 ✓ UI/业务分离 ✓ Repository 唯一入口 ✓ Config 独立 ✓ Assets 分类统一 ✓ 支持长期多人协作

---

# Final Principle

一个优秀的项目结构不是为了现在方便，而是让三年后的开发者第一次打开工程就能立刻理解整个项目。

---

End of Document
