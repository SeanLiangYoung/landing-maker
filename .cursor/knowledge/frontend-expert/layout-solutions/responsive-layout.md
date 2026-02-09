# 响应式布局知识

## 响应式设计原则

### 移动端优先（Mobile First）
- **策略**：先设计移动端，再逐步增强到桌面端
- **优势**：性能更好，代码更简洁
- **实现**：使用 `min-width` 媒体查询

```css
/* 移动端基础样式 */
.container {
  padding: 20px;
}

/* 平板端 */
@media (min-width: 768px) {
  .container {
    padding: 40px;
  }
}

/* 桌面端 */
@media (min-width: 1024px) {
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 60px;
  }
}
```

### 桌面端优先（Desktop First）
- **策略**：先设计桌面端，再适配移动端
- **实现**：使用 `max-width` 媒体查询

```css
/* 桌面端基础样式 */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 60px;
}

/* 平板端 */
@media (max-width: 1024px) {
  .container {
    padding: 40px;
  }
}

/* 移动端 */
@media (max-width: 768px) {
  .container {
    padding: 20px;
  }
}
```

---

## 响应式断点

### 标准断点
```css
/* 移动端 */
@media (max-width: 575px) { }

/* 平板端（竖屏） */
@media (min-width: 576px) and (max-width: 767px) { }

/* 平板端（横屏） */
@media (min-width: 768px) and (max-width: 1023px) { }

/* 桌面端 */
@media (min-width: 1024px) { }

/* 大桌面端 */
@media (min-width: 1440px) { }
```

### 常用断点（推荐）
```css
/* 移动端 */
@media (max-width: 767px) { }

/* 平板端 */
@media (min-width: 768px) and (max-width: 1023px) { }

/* 桌面端 */
@media (min-width: 1024px) { }
```

---

## 容器最大宽度

### 标准容器宽度
- **小容器**：1140px
- **标准容器**：1200px（推荐）
- **大容器**：1280px

### 实现方式
```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

@media (max-width: 768px) {
  .container {
    padding: 0 16px;
  }
}
```

---

## 响应式网格

### CSS Grid 响应式
```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 32px;
}

/* 移动端单列 */
@media (max-width: 767px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
```

### Flexbox 响应式
```css
.flex-container {
  display: flex;
  flex-wrap: wrap;
  gap: 32px;
}

.flex-item {
  flex: 1 1 300px;
  min-width: 0;
}

/* 移动端单列 */
@media (max-width: 767px) {
  .flex-item {
    flex: 1 1 100%;
  }
}
```

---

## 响应式字体

### 流体字体（Fluid Typography）
```css
/* 使用 clamp 实现流体字体 */
h1 {
  font-size: clamp(2rem, 5vw, 3.5rem);
}

p {
  font-size: clamp(1rem, 2vw, 1.125rem);
}
```

### 媒体查询字体
```css
h1 {
  font-size: 2rem;
}

@media (min-width: 768px) {
  h1 {
    font-size: 2.5rem;
  }
}

@media (min-width: 1024px) {
  h1 {
    font-size: 3.5rem;
  }
}
```

---

## 响应式图片

### 响应式图片
```html
<img 
  src="image.jpg" 
  srcset="image-small.jpg 768w, image-medium.jpg 1024w, image-large.jpg 1920w"
  sizes="(max-width: 768px) 100vw, (max-width: 1024px) 50vw, 33vw"
  alt="Description"
>
```

### 图片容器
```css
.image-container {
  width: 100%;
  height: auto;
  overflow: hidden;
}

.image-container img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```
