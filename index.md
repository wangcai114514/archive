
<style>
/* ========== 1. 全局变量：深浅模式基础色值 ========== */
:root {
  --bg-color: #ffffff;
  --text-color: #333333;
  --card-bg: #f8f9fa;
  --card-hover: #e9ecef;
  --header-bg: rgba(255, 255, 255, 0.9);
}
.dark-mode {
  --bg-color: #1a1a1a;
  --text-color: #f5f5f5;
  --card-bg: #2d2d2d;
  --card-hover: #3d3d3d;
  --header-bg: rgba(26, 26, 26, 0.9);
}

/* ========== 2. 跨系统/浏览器兼容：全局背景图核心 ========== */
* {
  box-sizing: border-box;
  /* 统一系统字体渲染（抗锯齿） */
  -webkit-font-smoothing: antialiased; /* Safari/iOS/macOS */
  -moz-osx-font-smoothing: grayscale; /* Firefox/macOS */
  font-smoothing: antialiased;
}
body {
  position: relative;
  color: var(--text-color);
  margin: 0;
  padding: 20px 0 80px 0; /* 底部文字区留空间 */
  transition: all 0.3s ease;
  min-height: 100vh; /* 强制铺满屏幕高度 */
  -webkit-overflow-scrolling: touch; /* iOS顺滑滚动 */
}
/* 伪元素承载背景图：跨系统固定效果一致 */
body::before {
  content: "";
  position: fixed; /* 所有系统固定背景一致 */
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  /* 自定义背景图链接（替换这里！） */
  background-image: url(https://raw.githubusercontent.com/wangcai114514/archive/refs/heads/main/assets/background/R-C.jpg);
  background-repeat: no-repeat;
  background-position: center center;
  /* 全浏览器兼容的背景缩放 */
  -webkit-background-size: cover; /* Safari/iOS */
  -moz-background-size: cover;    /* Firefox */
  -o-background-size: cover;      /* Opera */
  background-size: cover;
  /* 背景混合模式+跨系统色彩校准 */
  background-color: var(--bg-color);
  -webkit-background-blend-mode: overlay; /* Safari */
  background-blend-mode: overlay;
  /* 跨系统色彩统一（微调可改参数） */
  filter: brightness(0.98) contrast(1.02);
  -webkit-filter: brightness(0.98) contrast(1.02);
  /* 硬件加速：统一渲染精度 */
  transform: translateZ(0);
  -webkit-transform: translateZ(0);
  /* 层级：不遮挡内容 */
  z-index: -1;
}

/* ========== 3. 深色模式切换按钮 ========== */
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
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  z-index: 999;
  /* 兼容移动端点击 */
  -webkit-tap-highlight-color: transparent;
  tap-highlight-color: transparent;
}

/* ========== 4. 标题区域 ========== */
.header {
  max-width: 1200px;
  margin: 0 auto 20px auto;
  padding: 0 20px;
}
.header-content {
  background: var(--header-bg);
  border-radius: 8px;
  padding: 10px 20px;
  display: inline-block;
}

/* ========== 5. 年份方块布局：PC3个/手机2个（自适应） ========== */
.year-grid {
  display: grid;
  /* 自适应：PC3个/手机2个/超小屏1个 */
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  max-width: 1200px;
  margin: 0 auto 40px auto;
  padding: 0 20px;
}

/* ========== 6. 年份方块：渐变覆盖图（左到右消失） ========== */
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
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  transition: transform 0.2s;
  opacity: 0.95;
  overflow: hidden;
  /* 兼容移动端点击 */
  -webkit-tap-highlight-color: transparent;
  tap-highlight-color: transparent;
}
/* 方块渐变覆盖图（替换这里的链接！） */
.year-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: url(【你的方块渐变覆盖图链接】) no-repeat left center;
  background-size: cover;
  /* 左到右渐变消失：全浏览器兼容 */
  mask: linear-gradient(to right, rgba(0,0,0,1), rgba(0,0,0,0));
  -webkit-mask: linear-gradient(to right, rgba(0,0,0,1), rgba(0,0,0,0)); /* Safari */
  opacity: 0.2; /* 透明度可调：0.1-0.3最佳 */
  z-index: 1;
}
.year-card:hover {
  transform: translateY(-5px);
  background: var(--card-hover);
  opacity: 1;
}
/* 文字在覆盖图上层 */
.year-card span {
  position: relative;
  z-index: 2;
}

/* ========== 7. 移动端自适应兼容 ========== */
@media (max-width: 768px) { /* 手机端：一行2个 */
  .year-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  .year-card {
    padding: 30px 15px;
    font-size: 20px;
  }
}
@media (max-width: 480px) { /* 超小屏手机：一行1个 */
  .year-grid {
    grid-template-columns: 1fr;
  }
  .toggle-btn {
    padding: 8px 16px;
    font-size: 14px;
  }
}

/* ========== 8. 底部文字区：居中显示（兼容所有系统） ========== */
.footer-text {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  background: var(--header-bg);
  border-radius: 8px;
  line-height: 2; /* 舒适的行间距 */
  font-size: 16px;
  text-align: center; /* 文字居中 */
}
</style>

<!-- 深色模式切换按钮 -->
<button class="toggle-btn" onclick="toggleDarkMode()">
  切换深色/浅色模式
</button>

<!-- 标题区域 -->
<div class="header">
  <div class="header-content">
    <h1>一个人的历史档案馆</h1>
    <p>轻装前行，与过去和解的数字自留地</p>
  </div>
</div>

<!-- 年份方块 -->
<div class="year-grid">
  <a href="2018/" class="year-card"><span>📅 2018年</span></a>
  <a href="2019/" class="year-card"><span>📅 2019年</span></a>
  <a href="2020/" class="year-card"><span>📅 2020年</span></a>
  <a href="2021/" class="year-card"><span>📅 2021年</span></a>
  <a href="2022/" class="year-card"><span>📅 2022年</span></a>
  <a href="2023/" class="year-card"><span>📅 2023年</span></a>
  <a href="2024/" class="year-card"><span>📅 2024年</span></a>
  <a href="2025/" class="year-card"><span>📅 2025年</span></a>
  <a href="2026/" class="year-card"><span>📅 2026年</span></a>
</div>

<!-- 底部自定义文字区（编辑这里的内容！） -->
<div class="footer-text">
  <h3>写在最后</h3>
  <p>【替换成你想写的文字，比如：】</p>
  <p>这个档案馆，是我和自己的对话。</p>
  <p>每一个年份，每一个月，都是回不去的时光，但可以好好安放。</p>
  <p>不囤积，不内耗，和过去和解，轻装往前走。</p>
</div>

<!-- 深色模式记忆：刷新不重置（兼容所有浏览器） -->
<script>
// 兼容旧浏览器的localStorage
function toggleDarkMode() {
  const body = document.body;
  body.classList.toggle('dark-mode');
  // 保存选择到本地（跨会话生效）
  if (typeof localStorage !== 'undefined') {
    localStorage.setItem('darkMode', body.classList.contains('dark-mode'));
  }
}
// 页面加载时恢复深色模式
window.onload = function() {
  if (typeof localStorage !== 'undefined' && localStorage.getItem('darkMode') === 'true') {
    document.body.classList.add('dark-mode');
  }
}
</script>
