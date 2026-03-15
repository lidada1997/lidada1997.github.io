# 个人作品集网站

> 李大大的技术作品集

## 快速部署到GitHub Pages

### 方法1：直接复制到GitHub仓库（最简单）

1. **在GitHub创建仓库**
   - 仓库名必须是：`lidada1997.github.io`（你的用户名）
   - 设置为Public

2. **上传文件**
   - 将以下文件上传到仓库根目录：
     - `_config.yml`
     - `index.md`
     - `projects.md`
     - `about.md`
     - `Gemfile`

3. **启用GitHub Pages**
   - 进入仓库 Settings → Pages
   - Source选择：Deploy from a branch
   - Branch选择：main / root
   - 点击Save

4. **访问网站**
   - 等待1-2分钟部署
   - 访问：`https://lidada1997.github.io`

---

### 方法2：本地预览后部署

```bash
# 1. 安装Ruby环境（如果没有）
# Ubuntu/Debian
sudo apt-get install ruby-full build-essential

# macOS
brew install ruby

# Windows: 下载安装 https://rubyinstaller.org/

# 2. 安装Bundler
gem install bundler

# 3. 安装依赖
cd your-portfolio
bundle install

# 4. 本地预览
bundle exec jekyll serve

# 访问 http://localhost:4000

# 5. 部署到GitHub
git init
git add .
git commit -m "初始化个人网站"
git remote add origin https://github.com/lidada1997/lidada1997.github.io.git
git push -u origin main
```

---

## 自定义域名（可选）

如果你有自己的域名：

1. 在仓库根目录创建 `CNAME` 文件
2. 写入你的域名，例如：`www.yourname.com`
3. 在域名服务商处添加CNAME记录指向 `lidada1997.github.io`

---

## 修改内容

### 更新个人信息

编辑 `_config.yml`：
```yaml
title: 你的名字
description: 你的描述
author: 你的用户名
email: 你的邮箱
```

### 添加新项目

编辑 `projects.md`，在对应位置添加：
```markdown
### 新项目名称 🎯

**项目简介**

- 功能1
- 功能2

**技术栈：** 列出技术

[📂 GitHub](GitHub地址)
```

### 添加新页面

1. 创建 `newpage.md`
2. 在 `_config.yml` 的 `header_pages` 中添加
3. 提交推送

---

## 项目文件结构

```
your-portfolio/
├── _config.yml      # 配置文件
├── index.md         # 首页
├── projects.md      # 项目页
├── about.md         # 关于页
├── Gemfile          # Ruby依赖
└── README.md        # 说明文档
```

---

## 技术栈

- Jekyll - 静态网站生成器
- GitHub Pages - 免费托管
- Markdown - 内容编写

---

*部署完成后，访问 https://lidada1997.github.io 查看你的作品集！*
