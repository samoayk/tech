<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>我的主页</title>
<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
  }

  /* 自动浅色 / 深色模式 */
  :root {
    --bg: #fff;
    --sidebar: #f7f7f7;
    --text: #333;
    --border: #ddd;
    --hover: #eaeaea;
  }
  @media (prefers-color-scheme: dark) {
    :root {
      --bg: #121212;
      --sidebar: #1e1e1e;
      --text: #eee;
      --border: #333;
      --hover: #2d2d2d;
    }
  }

  body {
    background: var(--bg);
    color: var(--text);
    display: flex;
    min-height: 100vh;
  }

  /* ========== 左侧导航 ========== */
  .sidebar {
    width: 190px;
    background: var(--sidebar);
    border-right: 1px solid var(--border);
    padding: 30px 15px;
    position: fixed;
    height: 100vh;
  }
  .sidebar h2 {
    font-size: 18px;
    margin-bottom: 25px;
    text-align: center;
  }
  .sidebar a {
    display: block;
    padding: 11px 14px;
    margin: 4px 0;
    color: var(--text);
    text-decoration: none;
    border-radius: 6px;
  }
  .sidebar a:hover {
    background: var(--hover);
  }

  /* ========== 右侧内容 ========== */
  .content {
    margin-left: 190px;
    padding: 40px;
    flex: 1;
  }
</style>
</head>

<body>

  <!-- 左侧导航（所有页面都用这一段） -->
  <div class="sidebar">
    <h2>导航菜单</h2>
    <a href="/">首页</a>
    <a href="/game/">游戏</a>
    <a href="/game/xxx.html">你的项目1</a>
    <a href="/game/yyy.html">你的项目2</a>
    <a href="https://github.com/samoayk" target="_blank">GitHub</a>
  </div>

  <!-- 右侧内容（每个页面放自己原来的内容） -->
  <div class="content">
    <h1>这里是页面内容</h1>
    <p>把你每个页面原来的内容放在这里即可</p>
  </div>

</body>
</html>
