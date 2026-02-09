# 过渡动画知识

## 平滑过渡（Smooth Transition）

### 基础过渡
```css
.element {
  transition: all 0.3s ease;
}

.element:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
}
```

### 过渡时长
- **快速交互**：150ms（按钮点击、hover）
- **标准过渡**：200-300ms（卡片 hover、页面过渡）
- **慢速动画**：400-500ms（页面加载、复杂动画）

### 缓动函数
```css
/* 标准缓动 */
transition: all 0.3s ease;

/* 平滑开始和结束 */
transition: all 0.3s ease-in-out;

/* 快速开始，慢速结束 */
transition: all 0.3s ease-out;

/* 慢速开始，快速结束 */
transition: all 0.3s ease-in;

/* 自定义缓动 */
transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
```

---

## 常见过渡效果

### 颜色过渡
```css
.button {
  background: #007bff;
  transition: background 0.3s ease;
}

.button:hover {
  background: #0056b3;
}
```

### 变换过渡
```css
.card {
  transform: translateY(0);
  transition: transform 0.3s ease;
}

.card:hover {
  transform: translateY(-4px);
}
```

### 阴影过渡
```css
.card {
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
  transition: box-shadow 0.3s ease;
}

.card:hover {
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
}
```

### 透明度过渡
```css
.overlay {
  opacity: 0;
  transition: opacity 0.3s ease;
}

.overlay.show {
  opacity: 1;
}
```

---

## 组合过渡

### 多属性过渡
```css
.button {
  background: #007bff;
  transform: translateY(0);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
  transition: 
    background 0.3s ease,
    transform 0.3s ease,
    box-shadow 0.3s ease;
}

.button:hover {
  background: #0056b3;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 123, 255, 0.3);
}
```

### 延迟过渡
```css
.menu-item {
  opacity: 0;
  transform: translateY(20px);
  transition: 
    opacity 0.3s ease,
    transform 0.3s ease;
}

.menu-item:nth-child(1) { transition-delay: 0.1s; }
.menu-item:nth-child(2) { transition-delay: 0.2s; }
.menu-item:nth-child(3) { transition-delay: 0.3s; }

.menu.show .menu-item {
  opacity: 1;
  transform: translateY(0);
}
```

---

## 性能优化

### 使用 transform 和 opacity
```css
/* ✅ 性能好 - 使用 transform */
.element {
  transform: translateX(0);
  transition: transform 0.3s ease;
}

.element:hover {
  transform: translateX(100px);
}

/* ❌ 性能差 - 使用 left */
.element {
  left: 0;
  transition: left 0.3s ease;
}

.element:hover {
  left: 100px;
}
```

### 使用 will-change
```css
.animated-element {
  will-change: transform;
  transition: transform 0.3s ease;
}
```

### 尊重用户偏好
```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```
