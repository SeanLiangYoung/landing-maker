# 常用组件知识

## CTA 按钮（Call-to-Action Button）

### 基础实现
```html
<a href="#" class="cta-button">立即开始</a>
```

```css
.cta-button {
  display: inline-block;
  padding: 16px 32px;
  background: #007bff;
  color: white;
  text-decoration: none;
  border-radius: 8px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.cta-button:hover {
  background: #0056b3;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 123, 255, 0.3);
}
```

### 渐变按钮
```css
.cta-button-gradient {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.cta-button-gradient:hover {
  background: linear-gradient(135deg, #764ba2 0%, #667eea 100%);
}
```

### 次要按钮
```css
.cta-button-secondary {
  background: transparent;
  border: 2px solid #007bff;
  color: #007bff;
}

.cta-button-secondary:hover {
  background: #007bff;
  color: white;
}
```

---

## 卡片组件（Card Component）

### 基础卡片
```html
<div class="card">
  <div class="card-icon">
    <svg>...</svg>
  </div>
  <h3 class="card-title">标题</h3>
  <p class="card-description">描述内容</p>
</div>
```

```css
.card {
  padding: 32px;
  background: white;
  border-radius: 12px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
  transition: all 0.3s ease;
}

.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.12);
}

.card-icon {
  width: 48px;
  height: 48px;
  margin-bottom: 16px;
}

.card-title {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 12px;
}

.card-description {
  color: #666;
  line-height: 1.6;
}
```

### 功能卡片
```css
.feature-card {
  text-align: center;
}

.feature-card .card-icon {
  margin: 0 auto 16px;
}
```

### 定价卡片
```css
.pricing-card {
  position: relative;
  padding: 40px 32px;
}

.pricing-card.featured {
  border: 2px solid #007bff;
  transform: scale(1.05);
}

.pricing-card .price {
  font-size: 3rem;
  font-weight: 700;
  color: #007bff;
  margin: 16px 0;
}
```

---

## 导航栏（Navigation Bar）

### 基础导航栏
```html
<nav class="navbar">
  <div class="container">
    <div class="navbar-brand">Logo</div>
    <ul class="navbar-menu">
      <li><a href="#features">功能</a></li>
      <li><a href="#pricing">定价</a></li>
      <li><a href="#contact">联系我们</a></li>
    </ul>
    <a href="#" class="cta-button">开始使用</a>
  </div>
</nav>
```

```css
.navbar {
  padding: 20px 0;
  background: white;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
  position: sticky;
  top: 0;
  z-index: 1000;
}

.navbar .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.navbar-menu {
  display: flex;
  list-style: none;
  gap: 32px;
}

.navbar-menu a {
  text-decoration: none;
  color: #333;
  font-weight: 500;
  transition: color 0.3s ease;
}

.navbar-menu a:hover {
  color: #007bff;
}

@media (max-width: 768px) {
  .navbar-menu {
    display: none;
  }
}
```

---

## 页脚（Footer）

### 基础页脚
```html
<footer class="footer">
  <div class="container">
    <div class="footer-content">
      <div class="footer-section">
        <h4>产品</h4>
        <ul>
          <li><a href="#">功能</a></li>
          <li><a href="#">定价</a></li>
        </ul>
      </div>
      <div class="footer-section">
        <h4>公司</h4>
        <ul>
          <li><a href="#">关于我们</a></li>
          <li><a href="#">联系我们</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <p>&copy; 2026 Company. All rights reserved.</p>
    </div>
  </div>
</footer>
```

```css
.footer {
  background: #1a1a1a;
  color: white;
  padding: 60px 0 20px;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 40px;
  margin-bottom: 40px;
}

.footer-section h4 {
  margin-bottom: 16px;
}

.footer-section ul {
  list-style: none;
}

.footer-section ul li {
  margin-bottom: 8px;
}

.footer-section a {
  color: #ccc;
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-section a:hover {
  color: white;
}

.footer-bottom {
  text-align: center;
  padding-top: 20px;
  border-top: 1px solid #333;
  color: #999;
}
```
