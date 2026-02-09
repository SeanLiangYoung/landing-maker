# 页面范式知识

## Hero 区块（Hero Section）

### 定义
Landing 页面的首屏展示区块，通常包含标题、副标题、CTA 按钮和视觉元素。

### 常见布局

#### 居中 Hero
```html
<section class="hero hero-centered">
  <div class="container">
    <h1>主标题</h1>
    <p class="subtitle">副标题</p>
    <a href="#" class="cta-button">行动号召</a>
  </div>
</section>
```

```css
.hero-centered {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 80vh;
  text-align: center;
  padding: 80px 20px;
}
```

#### 分屏 Hero
```html
<section class="hero hero-split">
  <div class="container">
    <div class="hero-content">
      <h1>主标题</h1>
      <p class="subtitle">副标题</p>
      <a href="#" class="cta-button">行动号召</a>
    </div>
    <div class="hero-visual">
      <img src="hero-image.jpg" alt="Hero Image">
    </div>
  </div>
</section>
```

```css
.hero-split {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
  padding: 80px 20px;
}

@media (max-width: 768px) {
  .hero-split {
    grid-template-columns: 1fr;
  }
}
```

### 设计建议
- **高度**：桌面端 80-100vh，移动端自适应
- **留白**：上下留白 80-120px
- **对齐**：居中或分屏布局
- **响应式**：移动端改为单列布局

---

## 功能展示区块（Features Section）

### 定义
展示产品核心功能的区块，通常使用网格布局。

### 常见布局

#### 2×2 网格
```css
.features-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 40px;
}

@media (max-width: 768px) {
  .features-grid {
    grid-template-columns: 1fr;
  }
}
```

#### 3 列网格
```css
.features-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
}

@media (max-width: 1024px) {
  .features-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .features-grid {
    grid-template-columns: 1fr;
  }
}
```

### 设计建议
- **间距**：卡片之间 32-40px
- **响应式**：桌面端多列，移动端单列
- **卡片**：使用统一的卡片组件

---

## 定价区块（Pricing Section）

### 定义
展示产品定价方案的区块，通常使用卡片对比布局。

### 常见布局

#### 3 列定价卡片
```css
.pricing-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
  max-width: 1200px;
  margin: 0 auto;
}

@media (max-width: 1024px) {
  .pricing-grid {
    grid-template-columns: 1fr;
    max-width: 500px;
  }
}
```

### 设计建议
- **突出推荐方案**：使用不同的样式突出推荐方案
- **对比清晰**：价格、功能对比清晰
- **CTA 按钮**：每个方案都有 CTA 按钮

---

## 案例展示区块（Testimonials Section）

### 定义
展示用户评价和成功案例的区块。

### 常见布局

#### 卡片网格
```css
.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
}

@media (max-width: 1024px) {
  .testimonials-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .testimonials-grid {
    grid-template-columns: 1fr;
  }
}
```

### 设计建议
- **真实性**：使用真实的用户评价
- **视觉元素**：头像、公司 logo、统计数据
- **布局**：卡片网格或轮播
