# 美容院预约系统

一个现代化的美容院在线预约管理系统，基于 Next.js 14 和 Supabase 构建。

## ✨ 特性

### 🎯 用户功能
- **用户注册登录** - 安全的邮箱验证和身份认证
- **服务浏览** - 查看所有美容护理服务项目
- **在线预约** - 选择服务、时间和技师进行预约
- **预约管理** - 查看、取消和管理个人预约记录
- **状态跟踪** - 实时查看预约状态（待确认、已确认、已完成等）

### 👩‍💼 管理功能
- **预约管理** - 确认、完成或取消客户预约
- **数据统计** - 查看总预约数、收入统计等业务数据
- **客户信息** - 查看客户详细信息和预约历史
- **管理备注** - 为预约添加内部管理备注

### 🔒 安全特性
- **行级安全策略 (RLS)** - 确保用户只能访问自己的数据
- **角色权限控制** - 区分客户、员工和管理员权限
- **数据加密** - 敏感信息安全存储

## 🛠 技术栈

### 前端
- **Next.js 14** - React 全栈框架
- **TypeScript** - 类型安全的 JavaScript
- **Tailwind CSS** - 现代化的 CSS 框架
- **React Hook Form** - 表单管理
- **date-fns** - 日期处理
- **Heroicons** - 精美的图标库
- **Sonner** - 优雅的消息提示

### 后端
- **Supabase** - 开源的 Firebase 替代方案
- **PostgreSQL** - 关系型数据库
- **Row Level Security** - 行级安全策略
- **Real-time** - 实时数据同步

## 📋 数据库设计

### 核心表结构

1. **profiles** - 用户信息表
   - 扩展 Supabase Auth 用户数据
   - 支持客户、员工、管理员角色

2. **services** - 服务项目表
   - 服务名称、描述、时长、价格
   - 支持分类管理

3. **staff** - 技师信息表
   - 技师专长、工作经验
   - 可用状态管理

4. **staff_schedules** - 工作时间表
   - 技师每周工作时间安排

5. **appointments** - 预约记录表
   - 预约状态跟踪
   - 客户和管理员备注

## 🚀 快速开始

### 1. 环境准备

```bash
# 安装依赖
npm install

# 或使用 yarn
yarn install
```

### 2. Supabase 配置

1. 在 [Supabase](https://supabase.com) 创建新项目
2. 获取项目 URL 和 API Key
3. 更新 `lib/supabase.ts` 中的配置：

```typescript
export const supabase = createClientComponentClient({
  supabaseUrl: '你的_SUPABASE_URL',
  supabaseKey: '你的_SUPABASE_ANON_KEY'
})
```

### 3. 数据库初始化

数据库结构已通过 Supabase MCP 自动创建，包括：
- 所有必要的表和关系
- 行级安全策略 (RLS)
- 示例服务数据
- 自动化触发器

### 4. 启动开发服务器

```bash
# 启动开发服务器
npm run dev

# 访问应用
# 打开浏览器访问 http://localhost:3000
```

## 📱 功能截图

### 用户端界面
- **登录注册页面** - 简洁优雅的认证界面
- **服务浏览** - 卡片式服务展示，支持分类筛选
- **预约表单** - 直观的预约流程
- **个人中心** - 预约历史和状态管理

### 管理端界面
- **数据仪表板** - 关键业务指标一目了然
- **预约管理** - 批量处理客户预约
- **客户信息** - 完整的客户档案

## 🎨 设计特色

### 美容主题设计
- **粉色渐变配色** - 体现美容行业的温馨氛围
- **现代化卡片布局** - 清晰的信息层次
- **响应式设计** - 完美适配各种设备
- **优雅的动画效果** - 提升用户体验

### 用户体验优化
- **直观的操作流程** - 减少用户学习成本
- **实时状态反馈** - 及时的操作提示
- **智能表单验证** - 防止错误输入
- **无障碍设计** - 支持键盘导航和屏幕阅读器

## 🔧 部署

### Vercel 部署 (推荐)

1. 将代码推送到 GitHub
2. 在 [Vercel](https://vercel.com) 导入项目
3. 配置环境变量
4. 自动部署完成

### 其他平台
- **Netlify** - 支持静态站点部署
- **Railway** - 全栈应用部署
- **自建服务器** - Docker 容器化部署

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

### 开发规范
- 使用 TypeScript 确保类型安全
- 遵循 ESLint 和 Prettier 代码规范
- 编写清晰的提交信息
- 添加必要的测试用例

## 📄 许可证

MIT License - 查看 [LICENSE](LICENSE) 文件了解详情

## 🙏 致谢

- [Supabase](https://supabase.com) - 优秀的后端服务
- [Next.js](https://nextjs.org) - 强大的 React 框架
- [Tailwind CSS](https://tailwindcss.com) - 高效的 CSS 框架
- [Heroicons](https://heroicons.com) - 精美的图标库

---

## 📞 支持与反馈

如果您有任何问题或建议，请通过以下方式联系：

- **GitHub Issues** - 技术问题和功能建议
- **邮箱** - 商务合作和技术支持

**享受您的美容预约体验！** ✨
