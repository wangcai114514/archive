<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2024年 - 我的时光档案馆</title>
    <style>
        /* 全局样式：跟随主页深浅模式，不强制深色 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        /* 基础变量：和主页保持一致 */
        :root {
            --bg-color: #1a1a1a;
            --text-color: #f5f5f5;
            --card-bg: #2d2d2d;
            --border-color: #444;
            --link-color: #ccc;
            --link-hover: #fff;
            --desc-color: #aaa;
        }
        .light-mode {
            --bg-color: #ffffff;
            --text-color: #333333;
            --card-bg: #f8f9fa;
            --border-color: #eee;
            --link-color: #666;
            --link-hover: #000;
            --desc-color: #888;
        }
        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
            line-height: 1.8;
            max-width: 800px;
            margin: 0 auto;
            padding: 40px 20px;
            transition: all 0.3s ease;
        }
        /* 返回按钮 */
        .back-home {
            display: inline-block;
            color: var(--link-color);
            text-decoration: none;
            margin-bottom: 30px;
            font-size: 16px;
        }
        .back-home:hover {
            color: var(--link-hover);
        }
        /* 年份标题 */
        h1 {
            text-align: center;
            margin-bottom: 40px;
            font-size: 32px;
        }
        /* 每月模块样式 */
        .month-section {
            background-color: var(--card-bg);
            border-radius: 12px;
            padding: 25px;
            margin-bottom: 25px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .month-title {
            font-size: 20px;
            margin-bottom: 15px;
            color: var(--text-color);
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 8px;
        }
        /* 文字段落 */
        .month-text {
            margin-bottom: 20px;
            font-size: 16px;
        }
        /* 图片样式：自适应宽度 */
        .month-img {
            width: 100%;
            border-radius: 8px;
            max-height: 500px;
            object-fit: cover;
            margin-bottom: 10px;
        }
        /* 图片说明 */
        .img-desc {
            color: var(--desc-color);
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
    <h1>2024年</h1>

    <!-- 1月模块 -->
    <div class="month-section">
        <h2 class="month-title">1月</h2>
        <p class="month-text">【替换这里】写1月的故事/心情/回忆，想写多少写多少。</p>
        <img src="【替换成你的图片Raw链接】" alt="2024年1月" class="month-img">
        <p class="img-desc">【可选】图片说明，比如“1月的第一场雪”</p>
    </div>

    <!-- 2月模块 -->
    <div class="month-section">
        <h2 class="month-title">2月</h2>
        <p class="month-text">【替换这里】写2月的内容。</p>
        <img src="【替换成你的图片Raw链接】" alt="2024年2月" class="month-img">
        <p class="img-desc">【可选】图片说明</p>
    </div>

    <!-- 3月模块（无图示例） -->
    <div class="month-section">
        <h2 class="month-title">3月</h2>
        <p class="month-text">【替换这里】写3月的内容。</p>
    </div>

    <!-- 4月模块 -->
    <div class="month-section">
        <h2 class="month-title">4月</h2>
        <p class="month-text">【替换这里】写4月的内容。</p>
    </div>

    <!-- 5月模块 -->
    <div class="month-section">
        <h2 class="month-title">5月</h2>
        <p class="month-text">【替换这里】写5月的内容。</p>
    </div>

    <!-- 6月模块 -->
    <div class="month-section">
        <h2 class="month-title">6月</h2>
        <p class="month-text">【替换这里】写6月的内容。</p>
    </div>

    <!-- 7月模块 -->
    <div class="month-section">
        <h2 class="month-title">7月</h2>
        <p class="month-text">【替换这里】写7月的内容。</p>
    </div>

    <!-- 8月模块 -->
    <div class="month-section">
        <h2 class="month-title">8月</h2>
        <p class="month-text">【替换这里】写8月的内容。</p>
    </div>

    <!-- 9月模块 -->
    <div class="month-section">
        <h2 class="month-title">9月</h2>
        <p class="month-text">【替换这里】写9月的内容。</p>
    </div>

    <!-- 10月模块 -->
    <div class="month-section">
        <h2 class="month-title">10月</h2>
        <p class="month-text">【替换这里】写10月的内容。</p>
    </div>

    <!-- 11月模块 -->
    <div class="month-section">
        <h2 class="month-title">11月</h2>
        <p class="month-text">【替换这里】写11月的内容。</p>
    </div>

    <!-- 12月模块 -->
    <div class="month-section">
        <h2 class="month-title">12月</h2>
        <p class="month-text">【替换这里】写12月的内容。</p>
    </div>

    <!-- 同步主页的深浅模式 -->
    <script>
        // 读取主页存储的模式，同步到当前页面
        if (localStorage.getItem('lightMode') === 'true') {
            document.body.classList.add('light-mode');
        }
    </script>
</body>
</html>
