# 一个人的历史档案馆
> 轻装前行，与过去和解的数字自留地

<style>
/* 适配1920*1080 PC端：一行3个大方块 */
.year-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  max-width: 1200px;
  margin: 40px auto;
  padding: 0 20px;
}
/* 每个年份方块样式：大方块、居中、点击友好 */
.year-card {
  background: #f8f9fa;
  border-radius: 8px;
  padding: 40px 20px;
  text-align: center;
  text-decoration: none;
  color: #333;
  font-size: 24px;
  font-weight: bold;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  transition: transform 0.2s;
}
.year-card:hover {
  transform: translateY(-5px);
  background: #e9ecef;
}
/* 手机端自适应：一行2个（小于768px时） */
@media (max-width: 768px) {
  .year-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  .year-card {
    padding: 30px 15px;
    font-size: 20px;
  }
}
/* 超小手机（比如小屏安卓）：一行1个 */
@media (max-width: 480px) {
  .year-grid {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="year-grid">
  <a href="2018/" class="year-card"> 2018年</a>
  <a href="2019/" class="year-card"> 2019年</a>
  <a href="2020/" class="year-card"> 2020年</a>
  <a href="2021/" class="year-card"> 2021年</a>
  <a href="2022/" class="year-card"> 2022年</a>
  <a href="2023/" class="year-card"> 2023年</a>
  <a href="2024/" class="year-card"> 2024年</a>
  <a href="2025/" class="year-card"> 2025年</a>
  <a href="2026/" class="year-card"> 2026年</a>
</div>

> 归档原则：只存文字和小图，大文件仅记录，不囤积、不内耗
> 访问说明：这是我的私人数字自留地，仅用于梳理回忆、完成心理交割。
