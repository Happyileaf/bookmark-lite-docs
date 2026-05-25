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

本项目采用 Next.js 全栈开发模式，技术栈围绕 Web 页面、服务端能力、数据存储、身份认证、样式组件、测试和部署展开。

| 分类 | 技术选型 | 说明 |
|---|---|---|
| Web 框架 | Next.js | 用于构建全栈 Web 应用 |
| 开发语言 | TypeScript | 用于提供类型约束和提升可维护性 |
| UI 框架 | React | 用于构建交互式用户界面 |
| 路由模式 | Next.js App Router | 用于组织页面和布局 |
| 服务端能力 | Server Actions / Route Handlers | 用于承载 Next.js 全栈服务端能力 |
| 数据库 | PostgreSQL | 用于存储结构化业务数据 |
| ORM | Prisma | 用于数据库建模、迁移和类型安全访问 |
| 样式方案 | Tailwind CSS | 用于快速构建响应式界面 |
| UI 组件库 | shadcn/ui | 用于基础 UI 组件建设 |
| 表单处理 | React Hook Form | 用于表单状态管理 |
| 数据校验 | Zod | 用于表单和服务端数据校验 |
| 表格组件 | TanStack Table | 用于管理页表格能力 |
| 图标库 | Lucide React | 用于界面图标 |
| 包管理器 | pnpm | 用于依赖管理 |
| 单元测试 | Vitest | 用于业务逻辑和工具函数测试 |
| 组件测试 | React Testing Library | 用于 React 组件测试 |
| 端到端测试 | Playwright | 用于核心用户流程测试 |
| 代码规范 | ESLint | 用于代码质量检查 |
| 代码格式化 | Prettier | 用于统一代码格式 |
| 部署平台 | Vercel | 用于部署 Next.js 应用 |

## 3. 核心技术选型

### 3.1 Next.js

Next.js 是本项目的核心 Web 框架，用于支持全栈开发、页面渲染、服务端能力和部署集成。

### 3.2 TypeScript

TypeScript 用于提高代码类型安全性，降低业务模型、接口数据和组件属性在开发过程中的维护成本。

### 3.3 React

React 用于构建应用公开书签页、用户书签页、管理页、表单弹窗、标签选择器和批量操作等用户界面。

### 3.4 PostgreSQL

PostgreSQL 用于存储用户、书签、标签、书签标签关联关系、角色和会话等结构化数据。

### 3.5 Prisma

Prisma 用于定义数据库模型、管理数据库迁移，并在 TypeScript 中提供类型安全的数据访问能力。


### 3.6 Tailwind CSS

Tailwind CSS 用于构建响应式页面样式，适合快速实现工具型 Web 应用界面。

### 3.7 shadcn/ui

shadcn/ui 用于提供按钮、输入框、弹窗、表格、菜单、提示等基础 UI 组件。

## 4. 前端相关技术

| 技术 | 用途 |
|---|---|
| Next.js App Router | 页面、布局和路由组织 |
| React | 用户界面构建 |
| Tailwind CSS | 样式开发 |
| shadcn/ui | 基础 UI 组件 |
| Lucide React | 图标展示 |
| React Hook Form | 表单状态管理 |
| Zod | 表单校验和数据校验 |
| TanStack Table | 管理页表格展示和交互 |

## 5. 服务端相关技术

| 技术 | 用途 |
|---|---|
| Next.js Server Actions | 服务端数据变更能力 |
| Next.js Route Handlers | 服务端接口能力 |
| Prisma | 数据访问能力 |
| Zod | 服务端入参校验 |

## 6. 数据层相关技术

| 技术 | 用途 |
|---|---|
| PostgreSQL | 主业务数据库 |
| Prisma ORM | 数据模型、迁移和查询 |
| Prisma Migrate | 数据库版本迁移 |
| Prisma Studio | 本地数据查看和调试 |

## 7. 认证与权限相关技术

| 技术 | 用途 |
|---|---|
| bcrypt 或 Argon2 | 密码哈希 |
| Zod | 登录、注册等认证表单校验 |

## 8. UI 与交互相关技术

| 技术 | 用途 |
|---|---|
| Tailwind CSS | 原子化样式开发 |
| shadcn/ui | 基础交互组件 |
| Radix UI | shadcn/ui 底层无障碍组件能力 |
| Lucide React | 图标体系 |
| TanStack Table | 高密度表格和批量操作界面 |
| React Hook Form | 表单输入体验 |

## 9. 工程化相关技术

| 技术 | 用途 |
|---|---|
| pnpm | 包管理 |
| ESLint | 代码规范检查 |
| Prettier | 代码格式化 |
| TypeScript | 静态类型检查 |
| tsx | TypeScript 脚本执行 |
| dotenv | 环境变量管理 |

## 10. 测试相关技术

| 技术 | 用途 |
|---|---|
| Vitest | 单元测试 |
| React Testing Library | 组件测试 |
| Playwright | 端到端测试 |
| Testing Library Jest DOM | DOM 断言扩展 |

## 11. 部署与运行环境

| 分类 | 技术选型 |
|---|---|
| 应用部署 | Vercel |
| 数据库服务 | PostgreSQL 托管服务 |
| Node.js 运行时 | Node.js LTS |
| 环境变量管理 | Vercel Environment Variables |
| 日志 | Vercel Logs |
| 访问分析 | Vercel Analytics |

## 12. 推荐技术栈组合

### 12.1 MVP 阶段

| 分类 | 技术选型 |
|---|---|
| Web 框架 | Next.js |
| 语言 | TypeScript |
| UI | React + Tailwind CSS + shadcn/ui |
| 数据库 | PostgreSQL |
| ORM | Prisma |
| 表单 | React Hook Form + Zod |
| 表格 | TanStack Table |
| 测试 | Vitest + React Testing Library + Playwright |
| 部署 | Vercel |

### 12.2 后续可选增强

| 能力 | 可选技术 |
|---|---|
| 全文搜索 | PostgreSQL Full Text Search |
| 缓存 | Vercel KV 或 Redis |
| 文件存储 | Vercel Blob 或 S3 兼容存储 |
| 日志监控 | Sentry |
| 产品分析 | PostHog |
| 邮件服务 | Resend |

## 13. 技术栈边界

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
