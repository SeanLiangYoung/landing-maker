# 前端专家知识库

前端专家 Agent 的 DAG（有向无环图）知识库，用于结构化存储和检索前端实现专业知识。

## 知识库结构

### DAG 结构说明

- **节点**：知识点/模式（如实现模式、组件库、布局解法、动效实现、兼容性方案等）
- **边**：依赖关系（如「响应式布局」依赖「CSS Grid」「媒体查询」）
- **检索方式**：支持按语义和依赖链检索

### 知识分类

1. **实现模式**：页面范式、展示模式、代码模式
2. **组件库**：常用组件、UI 组件、交互组件
3. **布局解法**：响应式布局、网格系统、Flexbox、CSS Grid
4. **动效实现**：过渡动画、交互动画、加载动画
5. **兼容性方案**：浏览器兼容、响应式断点、降级方案

## 文件结构

```
frontend-expert/
├── README.md                    # 知识库说明文档
├── knowledge-dag.json          # DAG 结构定义（节点和边）
├── implementation-patterns/    # 实现模式知识
│   ├── page-paradigms/        # 页面范式
│   ├── display-patterns/       # 展示模式
│   └── code-patterns/          # 代码模式
├── component-library/          # 组件库知识
│   ├── common-components/     # 常用组件
│   ├── ui-components/         # UI 组件
│   └── interactive-components/ # 交互组件
├── layout-solutions/          # 布局解法知识
│   ├── responsive-layout/     # 响应式布局
│   ├── grid-systems/          # 网格系统
│   └── flexbox-grid/          # Flexbox 和 Grid
├── animation-effects/         # 动效实现知识
│   ├── transitions/          # 过渡动画
│   ├── interactions/         # 交互动画
│   └── loading-animations/   # 加载动画
└── compatibility-solutions/   # 兼容性方案知识
    ├── browser-compatibility/ # 浏览器兼容
    ├── responsive-breakpoints/ # 响应式断点
    └── fallback-solutions/    # 降级方案
```

## 使用方法

前端专家 Agent 在实现时，可以：
1. 根据设计规格检索相关的实现模式
2. 根据依赖关系查找相关的技术方案
3. 参考组件库和布局解法
4. 应用动效实现和兼容性方案

## 知识库维护

- **项目复盘**：根据实际项目经验，持续优化知识库内容
- **最佳实践积累**：将优秀的实现模式纳入知识库
