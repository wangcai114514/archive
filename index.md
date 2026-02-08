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
  max-width: 1200px;
  margin: 0 auto 20px auto;
  padding: 0 20px;
  text-align: center;
}
.header-content {
  background: var(--header-bg);
  border-radius: 8px;
  padding: 10px 20px;
  display: inline-block;
}

/* ========== 5. 年份网格 ========== */
.year-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  max-width: 1200px;
  margin: 0 auto 40px auto;
  padding: 0 20px;
}

/* ========== 6. 每个年份独立样式（关键！） ========== */
.year-card {
  position: relative;
  background: var(--card-bg);
  border-radius: 8px;
  padding: 40px 20px;
  text-align: center;
  text-decoration: none;
  color: var(--text-color);
  font-size: 24px;
  font-weight: bold;
  overflow: hidden;
}
.year-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: left center;
  background-repeat: no-repeat;
  -webkit-mask: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(0,0,0,0) 70%);
  mask: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(0,0,0,0) 70%);
  opacity: 0.2;
  z-index: 1;
}
.year-card span {
  position: relative;
  z-index: 2;
}

/* 2018 */
.year-2018::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2018.jpg);
}
/* 2019 */
.year-2019::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2019.jpg);
}
/* 2020 */
.year-2020::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2020.jpg);
}
/* 2021 */
.year-2021::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2021.jpg);
}
/* 2022 */
.year-2022::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2022.jpg);
}
/* 2023 */
.year-2023::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2023.jpg);
}
/* 2024 */
.year-2024::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2024.jpg);
}
/* 2025 */
.year-2025::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2025.jpg);
}
/* 2026 */
.year-2026::before {
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/card/2026.jpg);
}

/* ========== 7. 移动端 ========== */
@media (max-width: 768px) {
  .year-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media (max-width: 480px) {
  .year-grid {
    grid-template-columns: 1fr;
  }
}

/* ========== 8. 底部 ========== */
.footer-text {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  background: var(--header-bg);
  border-radius: 8px;
  text-align: center;
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
