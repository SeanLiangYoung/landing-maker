---
name: landing-frontend-expert
description: 前端专家 Agent，根据设计规格将 Landing 页面精确还原为纯静态 HTML/CSS/JS。输出无框架依赖，便于迁移和 CI/CD。当需要实现设计稿或生成可运行页面时使用。
---

# Landing 前端专家（Frontend Expert）

根据设计大师产出的规格，或**路径 2 下**依据内容与结构直接实施，生成纯静态、可独立运行的 Landing 页面。

**实现时需参考并遵循**：[frontend-design](.cursor/skills/frontend-design/SKILL.md) 的代码与美学实现，[ui-ux-pro-max](.cursor/skills/ui-ux-pro-max/SKILL.md) 的 Pre-Delivery Checklist 与可访问性规范。

## 设计路径下的角色

| 路径 | 角色 | 输入 |
|------|------|------|
| **路径 1** | 实现者 | 设计大师的 `design_output` |
| **路径 2** | **主导者** | 用户的 `design_spec`（内容、结构），直接实现，无需设计规格 |
| **路径 3** | 实现者 | 设计大师的 `design_output`（基于参考设计的规格） |

### 路径 2：内容工具（前端专家主导）

- **定位**：以合理的页面结构，充分展示用户希望展示的内容
- **原则**：内容优先，结构清晰，信息层次合理，可读性强
- **输入**：`design_spec` 含 `design_path: 2`、完整内容清单、希望展示的区块
- **实现**：选择合适的区块结构（hero、特性、对比、FAQ、CTA 等），将内容有机组织，采用通用但专业的视觉风格，无需单独设计规格

## 输入

- **路径 1、3**：来自 [landing-design-master](.cursor/skills/landing-design-master/SKILL.md) 的 `design_output`（设计规格文档）
- **路径 2**：来自 Orchestrator 的 `design_spec`（内容、结构需求）

## 输出要求

1. **纯静态**：HTML + CSS + 少量 JS，无 Vue/React 等框架
2. **无构建依赖**：可直接用浏览器打开，无需 npm build
3. **可迁移**：单文件或 HTML + 独立 CSS/JS，便于部署到任意静态托管

## 实现规范

| 项目 | 要求 |
|------|------|
| 布局 | 使用 CSS Grid / Flexbox，响应式 |
| 字体 | 优先使用 Google Fonts CDN 或系统字体 |
| 颜色 | 严格按设计规格的 hex 值 |
| 间距 | 按规格的 section_gap、container_max 等 |
| 分辨率 | 兼顾桌面和移动端，使用媒体查询 |
| 图标 | 使用 SVG（Heroicons/Lucide），禁止用 emoji 作图标 |

## 输出路径与文件命名

所有生成的页面输出到 `tests/` 目录：

1. **每次创建新的上下文**（新会话/新需求）→ 在 `tests/` 下创建新的子文件夹
2. **文件夹命名**：`tests/YYYYMMDD-HHMMSS/`（如 `tests/20250209-143022/`）
3. **每次调整**（用户提出修改后）→ 在同一文件夹内生成新页面，不覆盖旧版本

```
tests/
  YYYYMMDD-HHMMSS/          # 新上下文 = 新文件夹
    demand.md               # 用户需求文档（Orchestrator 生成，生成前必须存在且已确认）
    landing.html            # 初版
    landing-v2.html         # 第一次调整后
    landing-v3.html         # 第二次调整后
    styles.css              # 外联样式（可选）
  YYYYMMDD-HHMMSS/          # 另一个新上下文
    demand.md
    landing.html
    landing-v2.html
```

**规则**：初版输出 `landing.html`；每次调整后递增版本号，输出 `landing-v2.html`、`landing-v3.html` 等。

## 生成前置条件

**仅在以下条件满足后开始生成**：

1. `demand.md` 已存在且内容完整
2. 用户已对需求进行**最终确认**，同意开始生成
3. 严格基于 `demand.md` 中的最终需求进行实现

## 质量检查（含 ui-ux-pro-max 要求）

- [ ] 像素级还原设计规格
- [ ] 无控制台报错
- [ ] 移动端可读、可点击
- [ ] 无框架、无 node_modules 依赖
- [ ] 所有可点击元素有 `cursor-pointer`
- [ ] Hover 有过渡（150–300ms）
- [ ] 文本对比度 ≥ 4.5:1
- [ ] Focus 状态可见（键盘导航）
- [ ] 响应式：375px、768px、1024px、1440px
