# 部署到 Netlify 指南

## 🚀 快速部署步骤

### 1. 准备项目文件
项目已经准备好部署，包含以下配置：
- ✅ `netlify.toml` - Netlify 配置文件
- ✅ `out/` 目录 - 静态文件输出
- ✅ 移除了服务端依赖

### 2. 上传到 GitHub (推荐)

1. **创建 GitHub 仓库**
   - 登录 GitHub
   - 创建新仓库：`beauty-salon-booking`

2. **上传代码**
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Beauty Salon Booking System"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/beauty-salon-booking.git
   git push -u origin main
   ```

### 3. 连接 Netlify

1. **登录 Netlify**
   - 访问 [netlify.com](https://netlify.com)
   - 使用 GitHub 账户登录

2. **导入项目**
   - 点击 "New site from Git"
   - 选择 GitHub
   - 选择您的 `beauty-salon-booking` 仓库

3. **配置构建设置**
   - Build command: `npm run build`
   - Publish directory: `out`
   - Node version: `18`

### 4. 环境变量配置

在 Netlify 项目设置中添加环境变量：

```
NEXT_PUBLIC_SUPABASE_URL=https://fanqjiqarlrretkhfkqk.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImZhbnFqaXFhcmxycmV0a2hma3FrIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NTczODk4NjksImV4cCI6MjA3Mjk2NTg2OX0.92XJosGjbTwMhJ0lcw6V2YzrNIZtn0MxaO_GJPbpsHg
```

### 5. 部署完成 ✅

- 自动部署完成后，您会获得一个 `.netlify.app` 域名
- 可以绑定自定义域名

---

## 📁 手动上传方式 (备选)

如果不想使用 GitHub，可以直接上传文件：

1. **打包 out 目录**
   - 将 `out/` 目录压缩为 zip 文件

2. **手动部署**
   - 在 Netlify 选择 "Deploy manually"
   - 上传 zip 文件

---

## 🔧 故障排除

### 常见问题

1. **构建失败**
   - 检查 Node.js 版本是否为 18
   - 确保所有依赖已安装

2. **页面空白**
   - 检查环境变量是否正确设置
   - 确认 Supabase 配置正确

3. **路由问题**
   - `netlify.toml` 已配置重定向规则
   - 确保文件存在

---

## 🌟 功能特色

部署后的网站包含：
- ✨ 美容院预约系统
- 📱 响应式设计
- 🔒 用户认证 (Supabase)
- 📅 预约管理
- 👩‍💼 管理员后台
- 🎨 现代化UI设计

**预览地址**: 部署后您会获得一个唯一的 `.netlify.app` 域名

祝您部署成功！🎊
