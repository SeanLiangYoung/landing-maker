# 知识库更新建议

**分析时间**：2026-02-09  
**来源**：全民简历网 (https://www.qmjianli.com/)

---

## 一、产品知识库建议

### 1.1 新增知识点

#### 1.1.1 SaaS 服务平台价值主张模式

**节点 ID**：`saas-service-platform-value-proposition`

**分类**：`standard-content.value-propositions`

**描述**：SaaS 服务平台的价值主张表达模式，强调服务规模、效率和专业性

**特点**：
- 使用数据支撑（用户数量、服务规模）
- 强调核心功能（模板、快速制作）
- 简洁有力的表达方式

**示例**：
- "海量简历模板·10分钟制作简历·服务超1000万用户"
- "专业简历制作服务平台"

**依赖关系**：
- 依赖：`value-proposition`
- 被依赖：`saas-solution`

**应用场景**：SaaS 服务平台、B2C 服务产品

---

#### 1.1.2 功能特性卡片展示模式

**节点 ID**：`feature-cards-display`

**分类**：`standard-content.feature-descriptions`

**描述**：使用卡片形式展示产品功能特性，每个卡片包含图标、标题和简短描述

**特点**：
- 图标 + 标题 + 描述的结构
- 4-6 个核心功能展示
- 视觉清晰，易于理解

**示例**：
- 自动排版：输入内容，自动排版生成简历
- 风格定制：支持调色盘，万种皮肤随心换
- 隐私安全：简历加密，零骚扰
- 云端保存：电脑、手机随时编辑下载

**依赖关系**：
- 依赖：`value-proposition`
- 被依赖：`saas-solution`

**应用场景**：产品功能展示、特性说明

---

#### 1.1.3 用户评价展示模式

**节点 ID**：`user-testimonials-display`

**分类**：`standard-content.social-proof`

**描述**：展示真实用户评价，包含用户身份、评价内容和场景描述

**特点**：
- 用户身份（职业、身份）
- 具体评价内容
- 场景化描述
- 真实性（部分信息隐藏）

**示例**：
- 刘**，平面设计师："以前做简历总是自己设计制作，费时费力，自从用了全民简历网..."
- 1953*****78，人工智能专业应届生："作为应届生，我对简历制作一窍不通..."

**依赖关系**：
- 依赖：`social-proof`
- 被依赖：`saas-solution`

**应用场景**：社会证明、建立信任、用户评价展示

---

#### 1.1.4 数据展示建立信任模式

**节点 ID**：`data-trust-building`

**分类**：`standard-content.social-proof`

**描述**：使用具体数据（用户数量、服务规模等）建立信任和权威性

**特点**：
- 使用具体数字（1000 万用户）
- 强调服务规模
- 建立权威性

**示例**：
- "1000 万职场精英的共同选择"
- "累计 10,195,975 位用户在使用全民简历"

**依赖关系**：
- 依赖：`social-proof`
- 被依赖：`saas-solution`

**应用场景**：建立信任、展示权威性、数据证明

---

### 1.2 更新知识点

#### 1.2.1 更新 `saas-solution`

**更新内容**：
- 添加"功能特性卡片展示"作为展示方式
- 添加"用户评价展示"作为社会证明方式
- 添加"数据展示建立信任"作为信任建立方式

---

## 二、设计知识库建议

### 2.1 新增知识点

#### 2.1.1 功能特性卡片布局

**节点 ID**：`feature-cards-layout`

**分类**：`layout-patterns.layout-types`

**描述**：使用网格布局展示功能特性卡片，每个卡片包含图标、标题和描述

**特点**：
- 网格布局（2×2 或 3×2）
- 卡片内边距：32-40px
- 图标 + 标题 + 描述的结构
- 一致的视觉风格

**依赖关系**：
- 依赖：`card-layout`、`grid-system`
- 被依赖：`professional-trustworthy`

**应用场景**：产品功能展示、特性说明

---

#### 2.1.2 模板展示网格布局

**节点 ID**：`template-grid-layout`

**分类**：`layout-patterns.layout-types`

**描述**：使用网格布局展示模板/案例，每个模板以卡片形式展示预览图

**特点**：
- 网格布局（3×4 或 4×3）
- 卡片包含预览图和 CTA 按钮
- 一致的卡片尺寸
- 响应式适配

**依赖关系**：
- 依赖：`card-layout`、`grid-system`
- 被依赖：`professional-trustworthy`

**应用场景**：模板展示、案例展示、产品展示

---

#### 2.1.3 用户评价卡片布局

**节点 ID**：`testimonials-cards-layout`

**分类**：`layout-patterns.layout-types`

**描述**：使用卡片布局展示用户评价，每个卡片包含用户信息、评价内容和场景描述

**特点**：
- 卡片布局（2×3 或 3×2）
- 用户头像/身份 + 评价内容
- 场景化描述
- 真实性展示

**依赖关系**：
- 依赖：`card-layout`、`consistent-spacing`
- 被依赖：`professional-trustworthy`

**应用场景**：用户评价展示、社会证明

---

### 2.2 更新知识点

#### 2.2.1 更新 `professional-trustworthy`

**更新内容**：
- 添加"功能特性卡片布局"作为功能展示方式
- 添加"模板展示网格布局"作为内容展示方式
- 添加"用户评价卡片布局"作为社会证明展示方式

---

## 三、前端知识库建议

### 3.1 新增知识点

#### 3.1.1 功能特性卡片组件

**节点 ID**：`feature-cards-component`

**分类**：`component-library.common-components`

**描述**：功能特性卡片组件，包含图标、标题和描述

**实现特点**：
- 使用 Flexbox 或 Grid 布局
- 图标使用 SVG 或图标字体
- 响应式设计
- 悬停效果

**代码模式**：
```html
<div class="feature-card">
  <div class="feature-icon">...</div>
  <h4 class="feature-title">标题</h4>
  <p class="feature-description">描述</p>
</div>
```

**依赖关系**：
- 依赖：`card-component`、`responsive-layout`
- 被依赖：`feature-grid`

**应用场景**：产品功能展示、特性说明

---

#### 3.1.2 模板展示网格组件

**节点 ID**：`template-grid-component`

**分类**：`component-library.common-components`

**描述**：模板展示网格组件，使用网格布局展示模板卡片

**实现特点**：
- 使用 CSS Grid 实现网格布局
- 响应式设计（移动端 1 列，平板 2 列，桌面 3-4 列）
- 卡片包含预览图和 CTA 按钮
- 懒加载优化

**代码模式**：
```html
<div class="template-grid">
  <div class="template-card">
    <img src="preview.jpg" alt="模板预览">
    <a href="#" class="cta-button">立即使用</a>
  </div>
  ...
</div>
```

**依赖关系**：
- 依赖：`css-grid`、`card-component`、`responsive-layout`
- 被依赖：`feature-grid`

**应用场景**：模板展示、案例展示、产品展示

---

#### 3.1.3 用户评价卡片组件

**节点 ID**：`testimonials-cards-component`

**分类**：`component-library.common-components`

**描述**：用户评价卡片组件，展示用户评价和身份信息

**实现特点**：
- 使用卡片布局
- 用户头像/身份 + 评价内容
- 响应式设计
- 可能的滚动动画

**代码模式**：
```html
<div class="testimonial-card">
  <div class="user-info">
    <span class="user-name">刘**</span>
    <span class="user-title">平面设计师</span>
  </div>
  <p class="testimonial-content">评价内容...</p>
</div>
```

**依赖关系**：
- 依赖：`card-component`、`responsive-layout`
- 被依赖：`feature-grid`

**应用场景**：用户评价展示、社会证明

---

### 3.2 更新知识点

#### 3.2.1 更新 `feature-grid`

**更新内容**：
- 添加"功能特性卡片组件"作为实现方式
- 添加"模板展示网格组件"作为内容展示方式
- 添加"用户评价卡片组件"作为社会证明展示方式

---

## 四、DAG 节点变更总结

### 4.1 产品知识库

**新增节点**：4 个
- `saas-service-platform-value-proposition`
- `feature-cards-display`
- `user-testimonials-display`
- `data-trust-building`

**新增边**：8 条
- 各节点与 `saas-solution` 的连接
- 各节点与基础节点的依赖关系

### 4.2 设计知识库

**新增节点**：3 个
- `feature-cards-layout`
- `template-grid-layout`
- `testimonials-cards-layout`

**新增边**：6 条
- 各节点与 `professional-trustworthy` 的连接
- 各节点与基础节点的依赖关系

### 4.3 前端知识库

**新增节点**：3 个
- `feature-cards-component`
- `template-grid-component`
- `testimonials-cards-component`

**新增边**：6 条
- 各节点与 `feature-grid` 的连接
- 各节点与基础节点的依赖关系

---

## 五、知识文件建议

### 5.1 产品知识库

**新建文件**：
- `standard-content/saas-service-platform-value-proposition.md`
- `standard-content/feature-cards-display.md`
- `standard-content/user-testimonials-display.md`
- `standard-content/data-trust-building.md`

### 5.2 设计知识库

**新建文件**：
- `layout-patterns/feature-cards-layout.md`
- `layout-patterns/template-grid-layout.md`
- `layout-patterns/testimonials-cards-layout.md`

### 5.3 前端知识库

**新建文件**：
- `component-library/feature-cards-component.md`
- `component-library/template-grid-component.md`
- `component-library/testimonials-cards-component.md`

---

## 六、入库建议

**建议入库优先级**：
1. **高优先级**：功能特性卡片相关知识点（产品、设计、前端）
2. **中优先级**：用户评价展示相关知识点
3. **低优先级**：数据展示建立信任模式

**入库顺序**：
1. 先入库基础节点（功能特性卡片）
2. 再入库依赖节点（模板展示、用户评价）
3. 最后更新现有节点（saas-solution、professional-trustworthy、feature-grid）
