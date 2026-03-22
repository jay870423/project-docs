# AI产品展示企业官网

> 现代化AI企业官网，展示AI产品和案例，基于HTML + CSS + JavaScript开发

## 项目简介

这是一个现代化的企业官网，用于展示通过AI工具开发的产品，设计风格采用现代科技感，包含首页、关于我们、产品展示、案例展示、新闻动态、联系我们六大模块，支持响应式设计，适配移动端和PC端。

## 项目结构

```
project-docs/
├── README.md               # 项目说明文档
├── docs/
│   ├── 需求/               # 需求文档
│   ├── 设计/               # 设计文档
│   └── 测试/               # 测试文档
├── database/               # 数据库设计
└── src/
    └── website/            # 网站源代码
        ├── index.html      # 首页
        ├── css/
        │   └── style.css   # 主样式文件
        ├── js/
        │   └── main.js     # JavaScript功能
        ├── images/         # 图片资源目录
        └── pages/          # 其他页面
            ├── about.html           # 关于我们
            ├── products.html        # 产品列表
            ├── product-detail.html  # 产品详情
            ├── cases.html           # 案例列表
            ├── case-detail.html     # 案例详情
            ├── news.html            # 新闻列表
            ├── news-detail.html     # 新闻详情
            └── contact.html         # 联系我们
```

## 技术栈

- **HTML5** - 语义化标签
- **CSS3** - Flexbox/Grid 布局，响应式设计
- **JavaScript (Vanilla)** - 原生JavaScript，无框架依赖
- **Font Awesome** - 图标库
- **Google Fonts (Inter)** - 字体

## 性能特点

- 首屏加载快，总资源大小小
- 图片使用CSS渐变占位，实际使用可替换
- 所有外部资源使用CDN加速
- 纯静态网页，无需后端，加载速度快
- LCP 预计 < 1s，满足性能要求

## 本地运行

由于是纯静态HTML网站，可以直接打开运行，或者使用本地HTTP服务器：

### 方法1：直接打开

直接用浏览器打开 `src/website/index.html` 即可查看。

### 方法2：使用Python简易HTTP服务器

```bash
cd src/website
python3 -m http.server 8000
# 然后访问 http://localhost:8000
```

### 方法3：使用Node.js http-server

```bash
npm install -g http-server
cd src/website
http-server -p 8000
# 然后访问 http://localhost:8000
```

## 部署说明

### 静态网站托管（推荐）

可以直接部署到以下静态网站托管服务：

1. **Vercel** (推荐，免费可用)
   - 导入GitHub仓库
   - 构建命令留空，输出目录设置为 `src/website`
   - 自动部署

2. **Netlify**
   - 连接GitHub仓库
   - 发布目录设置为 `src/website`
   - 一键部署

3. **GitHub Pages**
   - 推送代码到GitHub
   - 在仓库设置中开启GitHub Pages
   - 源分支选择main，目录选择 `/src/website`

4. **云服务器部署**
   - 将 `src/website` 目录下所有文件上传到服务器
   - 配置Nginx/Apache指向该目录
   - 配置域名和SSL证书即可访问

### Nginx配置示例

```nginx
server {
    listen 80;
    server_name your-domain.com;
    root /path/to/project-docs/src/website;
    index index.html;
    
    location / {
        try_files $uri $uri/ /index.html;
    }
    
    # 开启gzip压缩
    gzip on;
    gzip_types text/css application/javascript image/svg+xml;
}
```

## 功能说明

### 已实现功能

- ✅ 导航栏（支持吸顶、移动端汉堡菜单）
- ✅ 首页（首屏、核心优势、精选产品、成功案例、数据展示、合作伙伴、CTA、页脚）
- ✅ 关于我们（公司简介、核心团队、发展历程、愿景使命）
- ✅ 产品展示（产品列表、分类筛选、产品详情）
- ✅ 案例展示（案例列表、分类筛选、案例详情）
- ✅ 新闻动态（新闻列表、分类筛选、新闻详情）
- ✅ 联系我们（联系信息、在线留言表单、招聘信息）
- ✅ 响应式设计（适配PC、平板、手机）
- ✅ 交互动画（滚动淡入、数字增长、卡片悬浮效果）
- ✅ 现代科技感设计风格

### 设计风格

- 主色调：科技蓝 `#165DFF`
- 辅助色：青蓝色 `#06B6D4`
- 渐变背景增加科技感
- 网格点阵背景装饰
- 圆角卡片 + 微妙阴影
- 滚动动画增加交互体验

## 浏览器兼容性

- Chrome (最新版) ✅
- Firefox (最新版) ✅
- Safari (最新版) ✅
- Edge (最新版) ✅
- 微信内置浏览器 (最新版) ✅
- 移动端浏览器 ✅

## 如何修改内容

### 修改文字内容

直接编辑对应的HTML文件，修改对应位置的文字即可。

### 修改样式

编辑 `css/style.css`，修改CSS变量即可快速更换主题色：

```css
:root {
    --primary-color: #165DFF;  /* 修改主色调 */
    --secondary-color: #06B6D4; /* 修改辅助色 */
}
```

### 添加新产品

1. 在 `pages/products.html` 中复制现有产品卡片，修改内容
2. 创建产品详情页面 `product-detail.html` 并修改内容
3. 链接对应即可

### 添加新案例/新闻

步骤类似，复制现有代码修改内容即可。

## 作者

AI Tech

## 许可证

MIT
