# 产品专家知识库变更日志

记录产品专家知识库的所有变更历史。

## 变更日志格式

每次更新知识库时，在文件顶部添加新的变更记录，格式如下：

```markdown
## [YYYY-MM-DD] - 变更类型

### 新增
- 新增知识点：[知识点名称]
  - 描述：[知识点描述]
  - 文件：[文件路径]
  - 依赖：[依赖的知识点]
  - 来源：[来源链接或说明]

### 更新
- 更新知识点：[知识点名称]
  - 变更内容：[具体变更内容]
  - 文件：[文件路径]
  - 原因：[更新原因]

### 删除
- 删除知识点：[知识点名称]
  - 原因：[删除原因]

### DAG 变更
- 新增节点：[节点ID]
- 新增边：[源节点] -> [目标节点]
- 删除节点：[节点ID]
- 删除边：[源节点] -> [目标节点]
```

---

## 变更历史

## [2026-02-09] - 新增知识点（全民简历网分析）

### 新增
- 新增知识点：功能特性卡片展示（feature-cards-display）
  - 描述：使用卡片形式展示产品功能特性，每个卡片包含图标、标题和简短描述
  - 文件：standard-content/feature-cards-display.md
  - 依赖：value-proposition
  - 来源：全民简历网 (https://www.qmjianli.com/)

- 新增知识点：用户评价展示模式（user-testimonials-display）
  - 描述：展示真实用户评价，包含用户身份、评价内容和场景描述
  - 文件：standard-content/user-testimonials-display.md
  - 依赖：social-proof
  - 来源：全民简历网 (https://www.qmjianli.com/)

- 新增知识点：数据展示建立信任（data-trust-building）
  - 描述：使用具体数据（用户数量、服务规模等）建立信任和权威性
  - 文件：standard-content/data-trust-building.md
  - 依赖：social-proof
  - 来源：全民简历网 (https://www.qmjianli.com/)

### 更新
- 更新知识点：SaaS 产品解决方案（saas-solution）
  - 变更内容：添加功能特性卡片展示、用户评价展示、数据展示建立信任作为展示方式
  - 文件：knowledge-dag.json
  - 原因：丰富 SaaS 产品解决方案的展示方式

### DAG 变更
- 新增节点：feature-cards-display、user-testimonials-display、data-trust-building
- 新增边：
  - saas-solution -> feature-cards-display (uses, 0.9)
  - saas-solution -> user-testimonials-display (uses, 0.8)
  - saas-solution -> data-trust-building (uses, 0.8)
  - feature-cards-display -> value-proposition (requires, 1.0)
  - user-testimonials-display -> social-proof (requires, 1.0)
  - data-trust-building -> social-proof (requires, 1.0)
