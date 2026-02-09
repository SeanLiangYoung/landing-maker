# 浏览器兼容性知识

## 可访问性（Accessibility）

### 语义化 HTML
```html
<!-- ✅ 使用语义化标签 -->
<header>
  <nav>
    <ul>
      <li><a href="#features">功能</a></li>
    </ul>
  </nav>
</header>

<main>
  <section id="features">
    <h2>功能特性</h2>
  </section>
</main>

<footer>
  <p>&copy; 2026 Company</p>
</footer>
```

### ARIA 标签
```html
<!-- 按钮 -->
<button aria-label="关闭菜单">×</button>

<!-- 图片 -->
<img src="image.jpg" alt="产品截图" aria-describedby="image-description">

<!-- 表单 -->
<label for="email">邮箱</label>
<input type="email" id="email" aria-required="true">
```

### 键盘导航
```css
/* 焦点样式 */
a:focus,
button:focus {
  outline: 2px solid #007bff;
  outline-offset: 2px;
}

/* 跳过链接 */
.skip-link {
  position: absolute;
  top: -40px;
  left: 0;
  background: #007bff;
  color: white;
  padding: 8px;
  text-decoration: none;
}

.skip-link:focus {
  top: 0;
}
```

---

## 色彩对比度

### WCAG 标准
- **AA 标准**：文本对比度 ≥ 4.5:1，大文本对比度 ≥ 3:1
- **AAA 标准**：文本对比度 ≥ 7:1，大文本对比度 ≥ 4.5:1

### 检查工具
```css
/* 确保足够的对比度 */
.text-primary {
  color: #333; /* 深色文字 */
  background: #fff; /* 白色背景 */
  /* 对比度: 12.63:1 ✅ */
}

.text-secondary {
  color: #666; /* 中灰色文字 */
  background: #fff; /* 白色背景 */
  /* 对比度: 7.0:1 ✅ */
}
```

### 降级方案
```css
/* 如果对比度不足，提供降级方案 */
.button {
  background: #f0f0f0;
  color: #333;
  border: 2px solid #333; /* 增加边框提升对比度 */
}
```

---

## 浏览器前缀

### CSS 属性前缀
```css
/* Flexbox */
.container {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
}

/* Grid */
.grid {
  display: -ms-grid;
  display: grid;
}

/* Transform */
.element {
  -webkit-transform: translateX(100px);
  transform: translateX(100px);
}
```

### 使用 Autoprefixer
推荐使用构建工具自动添加前缀，而不是手动添加。

---

## 降级方案

### CSS Grid 降级
```css
/* 使用 Flexbox 作为 Grid 的降级方案 */
.grid {
  display: flex;
  flex-wrap: wrap;
  gap: 32px;
}

@supports (display: grid) {
  .grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }
}
```

### 自定义属性降级
```css
/* 使用固定值作为降级 */
.button {
  background: #007bff; /* 降级值 */
}

@supports (--css: variables) {
  .button {
    background: var(--primary-color);
  }
}
```

---

## 响应式图片

### srcset 和 sizes
```html
<img 
  src="image-small.jpg"
  srcset="
    image-small.jpg 768w,
    image-medium.jpg 1024w,
    image-large.jpg 1920w
  "
  sizes="(max-width: 768px) 100vw, (max-width: 1024px) 50vw, 33vw"
  alt="描述"
>
```

### picture 元素
```html
<picture>
  <source media="(max-width: 768px)" srcset="image-mobile.jpg">
  <source media="(max-width: 1024px)" srcset="image-tablet.jpg">
  <img src="image-desktop.jpg" alt="描述">
</picture>
```

---

## 性能优化

### 图片优化
- 使用 WebP 格式（提供降级）
- 使用适当的图片尺寸
- 使用懒加载

### 字体优化
```css
/* 使用 font-display: swap */
@font-face {
  font-family: 'Custom Font';
  src: url('font.woff2') format('woff2');
  font-display: swap;
}
```

### 减少重排和重绘
- 使用 `transform` 和 `opacity` 进行动画
- 避免频繁修改 DOM
- 使用 `will-change` 提示浏览器
