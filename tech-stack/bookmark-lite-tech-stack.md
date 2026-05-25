# 书签管理 Web 应用技术栈文档

## 1. 文档信息

| 项目 | 内容 |
|---|---|
| 产品名称 | 书签管理 Web 应用 |
| 文档类型 | 技术栈文档 |
| 文档版本 | v1.0 |
| 关联 PRD | prd/bookmark-lite-prd.md |
| 技术方向 | Next.js 全栈开发 |

## 2. 技术栈总览

本项目采用 Next.js 全栈开发模式，技术栈围绕 Web 页面、服务端能力、数据存储、身份认证、权限控制、导入导出、安全、测试和部署展开。

| 分类 | 技术选型 | 说明 |
|---|---|---|
| Web 框架 | Next.js | 用于构建全栈 Web 应用 |
| 开发语言 | TypeScript | 用于提供类型约束和提升可维护性 |
| UI 框架 | React | 用于构建交互式用户界面 |
| 路由模式 | Next.js App Router | 用于组织页面和布局 |
| 服务端能力 | Server Actions / Route Handlers | 用于承载 Next.js 全栈服务端能力 |
| 数据库 | PostgreSQL | 用于存储结构化业务数据 |
| ORM | Prisma | 用于数据库建模、迁移和类型安全访问 |
| 认证方案 | Auth.js（NextAuth） | 用于邮箱密码登录、会话管理和认证上下文获取 |
| 鉴权方案 | Next.js Middleware + 服务端权限守卫 | 用于 RBAC 与数据范围鉴权 |
| 密码安全 | Argon2id（优先）或 bcrypt | 用于密码哈希存储 |
| 传输安全 | HTTPS/TLS | 用于保障登录和密码修改过程的传输加密 |
| 文件解析 | csv-parse / fast-csv + cheerio | 用于 CSV/JSON/HTML（浏览器书签）导入导出解析 |
| 样式方案 | Tailwind CSS | 用于快速构建响应式界面 |
| UI 组件库 | shadcn/ui | 用于基础 UI 组件建设 |
| 表单处理 | React Hook Form | 用于表单状态管理 |
| 端到端测试 | Playwright | 用于核心用户流程测试 |
| 代码规范 | ESLint | 用于代码质量检查 |
| 代码格式化 | Prettier | 用于统一代码格式 |
| 日志与观测 | Pino + Vercel Logs + Vercel Analytics | 用于运行日志、访问统计与基础观测 |
| 定时任务 | Vercel Cron（或等价调度能力） | 用于回收站保留期、审计日志保留期清理任务 |
| 部署平台 | Vercel | 用于部署 Next.js 应用 |

## 3. 核心技术选型

### 3.4 PostgreSQL

PostgreSQL 用于存储用户、书签、标签、书签标签关联关系、角色、会话、审计日志等结构化数据。

### 3.5 Prisma

Prisma 用于定义数据库模型、管理数据库迁移，并在 TypeScript 中提供类型安全的数据访问能力。

### 3.6 Auth.js

Auth.js 用于承载登录态与会话管理能力，支持在服务端按统一方式读取当前用户身份，便于和 RBAC 及数据范围校验结合。

### 3.7 Tailwind CSS + shadcn/ui

Tailwind CSS 用于快速构建响应式页面样式，shadcn/ui 用于提供按钮、输入框、弹窗、表格、菜单、提示等基础 UI 组件。

## 4. 前端相关技术

|---|---|
| Next.js Server Actions | 服务端数据变更能力 |
| Next.js Route Handlers | 服务端接口能力 |
| Next.js Middleware | 登录态检查、路由级访问控制 |
| Auth.js | 认证与会话获取 |
| Prisma | 数据访问能力 |
| Zod | 服务端入参校验 |
| Pino | 结构化日志输出 |

## 6. 数据层相关技术

| Prisma ORM | 数据模型、迁移和查询 |
| Prisma Migrate | 数据库版本迁移 |
| Prisma Studio | 本地数据查看和调试 |
| PostgreSQL 索引（BTREE/GIN） | 支持 URL 去重、标签筛选、关键词检索和排序性能 |

## 7. 认证与权限相关技术

| 技术 | 用途 |
|---|---|
| Auth.js（Credentials Provider） | 邮箱密码登录、会话管理、退出登录 |
| Argon2id（优先）或 bcrypt | 密码哈希与校验 |
| Next.js Middleware | 未登录跳转、基础路由拦截 |
| 服务端权限守卫（Route Handler / Action 层） | RBAC + 数据范围最终鉴权（后端强制） |
| Zod | 登录、注册、修改密码等入参校验 |
| HTTPS/TLS | 登录与密码相关请求传输加密 |
| 速率限制（基于 Redis 或等价方案） | 登录与高风险接口防刷、防爆破 |

## 8. 导入导出与文件处理相关技术

| 技术 | 用途 |
|---|---|
| csv-parse 或 fast-csv | CSV 解析与生成 |
| 原生 JSON 处理 | JSON 导入导出 |
| cheerio | 浏览器书签 HTML 解析 |
| Zod | 导入数据结构校验与错误归类 |

## 9. 审计、日志与统计相关技术

| 技术 | 用途 |
|---|---|
| PostgreSQL 审计日志表 | 记录越权请求和关键管理操作 |
| Pino | 应用结构化日志 |
| Vercel Logs | 运行日志查看 |
| Vercel Analytics | 访问与基础行为统计 |
| Vercel Cron（或等价调度能力） | 按保留期清理回收站与审计日志 |

## 10. UI 与交互相关技术

| 技术 | 用途 |
|---|---|
| Tailwind CSS | 原子化样式开发 |
| shadcn/ui | 基础交互组件 |
| Radix UI | shadcn/ui 底层无障碍组件能力 |
| TanStack Table | 高密度表格和批量操作界面 |
| React Hook Form | 表单输入体验 |

## 11. 工程化相关技术

| 技术 | 用途 |
|---|---|
| tsx | TypeScript 脚本执行 |
| dotenv | 环境变量管理 |

## 12. 测试相关技术

| 技术 | 用途 |
|---|---|
| Playwright | 端到端测试 |
| Testing Library Jest DOM | DOM 断言扩展 |

## 13. 部署与运行环境

| 分类 | 技术选型 |
|---|---|
| 环境变量管理 | Vercel Environment Variables |
| 日志 | Vercel Logs |
| 访问分析 | Vercel Analytics |
| 定时任务 | Vercel Cron |

## 14. 技术栈边界

本技术栈文档仅描述技术选型，不展开具体实现方案。

不包含内容：

- 页面路由设计细节。
- 数据库表结构细节。
- API 设计细节。
- 权限校验流程细节。
- 组件拆分方案。
- 文件目录结构方案。
- 部署流水线细节。
- 具体业务实现逻辑。
