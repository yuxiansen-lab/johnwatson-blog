# John Watson Blog - 本地部署版本

这是一个完整的静态网站部署包，包含原 John Watson 博客的所有内容、CSS 和静态资源。

## 📁 目录结构

```
johnwatson-blog-static/
├── index.html              # 主页（原始版本）
├── index-fixed.html        # 主页（修复版本，推荐使用）
├── blog/                   # 所有博客文章 HTML 文件
├── css/
│   └── main.css           # 完整的 CSS 样式文件
├── staticarchive/         # 原网站的所有静态资源
├── images/                # 图片文件
├── js/                    # JavaScript 文件
└── README.md              # 本文件
```

## 🚀 快速开始

### 方法 1：使用 Python 简单 HTTP 服务器（推荐）

```bash
cd johnwatson-blog-static
python3 -m http.server 8000
```

然后在浏览器中访问：`http://localhost:8000`

### 方法 2：使用 Node.js http-server

```bash
npm install -g http-server
cd johnwatson-blog-static
http-server
```

### 方法 3：使用 PHP 内置服务器

```bash
cd johnwatson-blog-static
php -S localhost:8000
```

### 方法 4：使用 Nginx 或 Apache

将 `johnwatson-blog-static` 目录配置为 Web 根目录。

## 📝 文件说明

### index.html vs index-fixed.html

- **index.html** - 原始网站文件，CSS 引用可能需要调整
- **index-fixed.html** - 修复版本，CSS 路径已更新为本地相对路径

**建议：** 如果 index.html 显示样式不正确，请使用 index-fixed.html

## 🎨 CSS 文件

所有 CSS 样式都已合并到 `css/main.css` 文件中，包括：
- 基础样式重置
- 布局和排版
- 颜色方案
- 响应式设计

### 修改 CSS

你可以直接编辑 `css/main.css` 文件来自定义样式：

```bash
# 使用你喜欢的编辑器打开
vim css/main.css
# 或
nano css/main.css
# 或在 IDE 中打开
```

修改后刷新浏览器即可看到效果。

## 📄 博客文章

所有 45 篇博客文章都在 `blog/` 目录中，每个文件对应一篇文章：

- `blog/11august.html` - The Sign of Three
- `blog/21july.html` - The Mayfly Man
- `blog/02july.html` - The Hollow Client
- ... 等等

## 🖼️ 静态资源

### 图片
所有图片文件都在 `images/` 目录中

### 原始资源
原网站的所有静态资源（CSS、JavaScript、图片）都在 `staticarchive/` 目录中

## 🔧 常见问题

### Q: 页面显示不正确或样式丢失？

**A:** 
1. 检查浏览器控制台是否有错误（按 F12）
2. 确保 CSS 文件路径正确
3. 尝试使用 index-fixed.html 代替 index.html
4. 清除浏览器缓存并刷新页面

### Q: 如何修改网站样式？

**A:** 编辑 `css/main.css` 文件，修改后刷新浏览器即可看到效果。

### Q: 如何添加新的文章？

**A:** 
1. 在 `blog/` 目录中创建新的 HTML 文件
2. 复制现有文章的 HTML 结构
3. 修改内容并保存
4. 在主页中添加链接

### Q: 如何部署到服务器？

**A:** 
1. 将整个 `johnwatson-blog-static` 目录上传到服务器
2. 配置 Web 服务器指向该目录
3. 确保 CSS 和其他资源路径正确

## 📊 内容统计

- 总文章数：45 篇
- 总评论数：419 条
- CSS 文件大小：22.7 KB
- 完整网站大小：约 5 MB

## 🛠️ 开发建议

### 本地开发工作流

```bash
# 1. 启动本地服务器
python3 -m http.server 8000

# 2. 在编辑器中打开项目
code .  # 如果使用 VS Code

# 3. 在浏览器中打开
# http://localhost:8000

# 4. 编辑 CSS 或 HTML 文件
# 编辑器保存后，刷新浏览器即可看到效果
```

### 推荐的编辑器

- VS Code
- Sublime Text
- Atom
- Vim / Nano

## 📦 部署清单

- [ ] 所有文件已下载
- [ ] 目录结构完整
- [ ] CSS 文件存在且可访问
- [ ] 博客文章文件存在
- [ ] 本地服务器可以启动
- [ ] 主页可以正常加载
- [ ] 样式显示正确
- [ ] 链接可以正常点击

## 🔗 相关链接

- 原网站：http://www.johnwatsonblog.co.uk/
- BBC Sherlock：http://www.bbc.co.uk/sherlock

## 📄 许可证

这个部署包包含来自原 John Watson Blog 的内容，仅供个人使用。

## 💡 提示

- 定期备份你的修改
- 在修改 CSS 前创建备份
- 使用版本控制（Git）管理你的修改
- 在测试环境中测试所有更改

---

**准备好了吗？** 运行 `python3 -m http.server 8000` 开始吧！
