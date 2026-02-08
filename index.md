<style>
/* ========== 1. 全局变量：默认深色模式 ========== */
:root {
  --bg-color: #1a1a1a;
  --text-color: #f5f5f5;
  --card-bg: #2d2d2d;
  --card-hover: #3d3d3d;
  --header-bg: rgba(26, 26, 26, 0.9);
  --bg-opacity: 0.9;
  --bg-blend: multiply;
  --bg-brightness: 0.95;
  /* 深色模式卡片图片参数 */
  --card-img-opacity: 0.3;
  --card-img-brightness: 0.9;
  --card-img-contrast: 1.1;
}
.light-mode {
  --bg-color: #ffffff;
  --text-color: #333333;
  --card-bg: #f8f9fa;
  --card-hover: #e9ecef;
  --header-bg: rgba(255, 255, 255, 0.9);
  --bg-opacity: 0.3;
  --bg-blend: soft-light;
  --bg-brightness: 1.05;
  /* 浅色模式卡片图片优化（核心：让图片好看） */
  --card-img-opacity: 0.2;
  --card-img-brightness: 1.15;
  --card-img-contrast: 1.05;
}

/* ========== 2. 全局样式 ========== */
* {
  box-sizing: border-box;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
body {
  position: relative;
  color: var(--text-color);
  margin: 0;
  padding: 20px 0 80px 0;
  transition: all 0.3s ease;
  min-height: 100vh;
  -webkit-overflow-scrolling: touch;
}
body::before {
  content: "";
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/background/R-C.jpg);
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
  opacity: var(--bg-opacity);
  background-color: var(--bg-color);
  background-blend-mode: var(--bg-blend);
  filter: brightness(var(--bg-brightness)) contrast(1.05);
  z-index: -1;
}

/* ========== 3. 按钮 ========== */
.toggle-btn {
  position: fixed;
  top: 20px;
  right: 20px;
  padding: 10px 20px;
  border: none;
  border-radius: 8px;
  background: var(--card-bg);
  color: var(--text-color);
  cursor: pointer;
  z-index: 999;
}
.toggle-btn:hover {
  background: var(--card-hover);
}

/* ========== 4. 标题 ========== */
.header {
  max-width: 1400px;
  margin: 0 auto 30px auto;
  padding: 0 20px;
  text-align: center;
}
.header-content {
  background: var(--header-bg);
  border-radius: 8px;
  padding: 15px 25px;
  display: inline-block;
}

/* ========== 5. 年份网格 ========== */
.year-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
  gap: 30px;
  max-width: 1400px;
  margin: 0 auto 50px auto;
  padding: 0 20px;
}

/* ========== 6. 年份方块（无渐变+深浅模式图片优化） ========== */
.year-card {
  position: relative;
  background: var(--card-bg);
  border-radius: 12px;
  padding: 80px 30px;
  text-align: center;
  text-decoration: none;
  color: var(--text-color);
  font-size: 32px;
  font-weight: bold;
  overflow: hidden;
  transition: transform 0.3s ease;
}
/* 无渐变：完整显示图片 */
.year-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  /* 移除所有渐变蒙版：图片完整显示 */
  opacity: var(--card-img-opacity);
  /* 深浅模式差异化图片优化 */
  filter: brightness(var(--card-img-brightness)) contrast(var(--card-img-contrast));
  z-index: 1;
}
.year-card span {
  position: relative;
  z-index: 2;
  /* 文字加轻微阴影，确保深浅模式都清晰 */
  text-shadow: 0 1px 2px rgba(0,0,0,0.1);
}
.year-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 16px rgba(0,0,0,0.2);
}

/* 每个年份独立图片 */
.year-2018::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2018.jpg);
}
.year-2019::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2019.jpg);
}
.year-2020::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2020.jpg);
}
.year-2021::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2021.jpg);
}
.year-2022::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2022.jpg);
}
.year-2023::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2023.jpg);
}
.year-2024::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2024.jpg);
}
.year-2025::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2025.jpg);
}
.year-2026::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2026.jpg);
}

/* ========== 7. 移动端适配 ========== */
@media (max-width: 900px) {
  .year-grid {
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  }
  .year-card {
    padding: 70px 25px;
    font-size: 28px;
  }
}
@media (max-width: 480px) {
  .year-grid {
    grid-template-columns: 1fr;
  }
  .year-card {
    padding: 60px 20px;
    font-size: 24px;
  }
}

/* ========== 8. 底部 ========== */
.footer-text {
  max-width: 1400px;
  margin: 0 auto;
  padding: 25px;
  background: var(--header-bg);
  border-radius: 12px;
  text-align: center;
  font-size: 18px;
  line-height: 1.8;
}
</style>

<button class="toggle-btn" onclick="toggleMode()">切换浅色/深色模式</button>

<div class="header">
  <div class="header-content">
    <h1>一个人的历史档案馆</h1>
    <p>轻装前行，与过去和解的数字自留地</p>
  </div>
</div>

<div class="year-grid">
  <a href="2018/" class="year-card year-2018"><span>2018年</span></a>
  <a href="2019/" class="year-card year-2019"><span>2019年</span></a>
  <a href="2020/" class="year-card year-2020"><span>2020年</span></a>
  <a href="2021/" class="year-card year-2021"><span>2021年</span></a>
  <a href="2022/" class="year-card year-2022"><span>2022年</span></a>
  <a href="2023/" class="year-card year-2023"><span>2023年</span></a>
  <a href="2024/" class="year-card year-2024"><span>2024年</span></a>
  <a href="2025/" class="year-card year-2025"><span>2025年</span></a>
  <a href="2026/" class="year-card year-2026"><span>2026年</span></a>
</div>

<div class="footer-text">
  <h3>写在最后</h3>
  <p>这个档案馆 是我和自己的对话</p>
  <p>每一年 每一月 都是回不去的时光</p>
  <p>往前走</p>
</div>

<script>
function toggleMode() {
  document.body.classList.toggle('light-mode');
  localStorage.setItem('lightMode', document.body.classList.contains('light-mode'));
}
window.onload = function() {
  if (localStorage.getItem('lightMode') === 'true') {
    document.body.classList.add('light-mode');
  }
}
</script>
