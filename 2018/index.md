<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2018年 - 我的时光档案馆</title>
    <style>
        /* 全局样式：和主页视觉统一 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            background-color: #1a1a1a;
            color: #f5f5f5;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
            line-height: 1.8;
            max-width: 800px;
            margin: 0 auto;
            padding: 40px 20px;
        }
        /* 返回按钮 */
        .back-home {
            display: inline-block;
            color: #ccc;
            text-decoration: none;
            margin-bottom: 30px;
            font-size: 16px;
        }
        .back-home:hover {
            color: #fff;
        }
        /* 年份标题 */
        h1 {
            text-align: center;
            margin-bottom: 40px;
            font-size: 32px;
        }
        /* 每月模块样式 */
        .month-section {
            background-color: #2d2d2d;
            border-radius: 12px;
            padding: 25px;
            margin-bottom: 25px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        .month-title {
            font-size: 20px;
            margin-bottom: 15px;
            color: #eee;
            border-bottom: 1px solid #444;
            padding-bottom: 8px;
        }
        /* 文字段落 */
        .month-text {
            margin-bottom: 20px;
            font-size: 16px;
        }
        /* 图片样式：自适应宽度，不超出容器 */
        .month-img {
            width: 100%;
            border-radius: 8px;
            max-height: 500px;
            object-fit: cover;
            margin-bottom: 10px;
        }
        /* 图片说明（可选） */
        .img-desc {
            color: #aaa;
            font-size: 14px;
            text-align: center;
            margin-bottom: 15px;
        }
    </style>
</head>
<body>
    <!-- 返回主页按钮 -->
    <a href="../" class="back-home">← 返回主页</a>
    
    <!-- 年份标题 -->
    <h1>2018年</h1>

    <!-- 1月模块：可直接修改文字/图片 -->
    <div class="month-section">
        <h2 class="month-title">1月</h2>
        <p class="month-text">【替换这里】写1月的故事/心情/回忆，想写多少写多少。</p>
        <!-- 图片：替换链接即可，不想加图就删掉下面3行 -->
        <img src="【替换成你的图片Raw链接】" alt="2018年1月" class="month-img">
        <p class="img-desc">【可选】图片说明，比如“1月的第一场雪”</p>
    </div>

    <!-- 2月模块 -->
    <div class="month-section">
        <h2 class="month-title">2月</h2>
        <p class="month-text">【替换这里】写2月的内容。</p>
        <!-- 不加图就删掉图片相关行 -->
        <img src="【替换成你的图片Raw链接】" alt="2018年2月" class="month-img">
        <p class="img-desc">【可选】图片说明</p>
    </div>

    <!-- 3月模块 -->
    <div class="month-section">
        <h2 class="month-title">3月</h2>
        <p class="month-text">【替换这里】写3月的内容。</p>
        <!-- 示例：不加图片的写法（直接删掉图片行即可） -->
    </div>

    <!-- 4-12月模板：复制上面的结构改月份即可 -->
    <div class="month-section">
        <h2 class="month-title">4月</h2>
        <p class="month-text">【替换这里】写4月的内容。</p>
    </div>
    <div class="month-section">
        <h2 class="month-title">5月</h2>
        <p class="month-text">【替换这里】写5月的内容。</p>
    </div>
    <div class="month-section">
        <h2 class="month-title">6月</h2>
        <p class="month-text">【替换这里】写6月的内容。</p>
    </div>
    <div class="month-section">
        <h2 class="month-title">7月</h2>
        <p class="month-text">【替换这里】写7月的内容。</p>
    </div>
    <div class="month-section">
        <h2 class="month-title">8月</h2>
        <p class="month-text">【替换这里】写8月的内容。</p>
    </div>
    <div class="month-section">
        <h2 class="month-title">9月</h2>
        <p class="month-text">【替换这里】写9月的内容。</p>
    </div>
    <div class="month-section">
        <h2 class="month-title">10月</h2>
        <p class="month-text">【替换这里】写10月的内容。</p>
    </div>
    <div class="month-section">
        <h2 class="month-title">11月</h2>
        <p class="month-text">【替换这里】写11月的内容。</p>
    </div>
    <div class="month-section">
        <h2 class="month-title">12月</h2>
        <p class="month-text">【替换这里】写12月的内容。</p>
    </div>
</body>
</html>
