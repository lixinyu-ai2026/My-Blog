# Spring Boot 个人博客全栈项目
基于 Spring Boot + Vue 前后端分离架构开发的个人博客系统，包含前台博客展示与后台管理功能，界面简洁、功能完整，适合学习、毕业设计或个人使用。

## 项目简介
本项目是一套**完整的前后端分离个人博客全栈项目**，后端使用 Spring Boot + MyBatis-Plus + MySQL + Redis，前端使用 Vue2 + Element UI。

系统包含两大模块：
- **前台用户端**：文章浏览、分类、标签、评论、留言、友链
- **后台管理端**：文章管理、分类管理、标签管理、评论管理、留言管理、用户管理

项目代码规范、结构清晰、注释完善，开箱即用。

## 技术栈
### 后端
- Spring Boot 2.7.x
- Spring Security
- MyBatis-Plus
- MySQL 5.7 / 8.0
- Redis
- Maven
- Hutool / Lombok

### 前端
- Vue 2.x
- Element UI
- Vue Router
- Vuex
- Axios

## 功能清单
### 前台功能
- 首页文章列表展示
- 文章详情 Markdown 渲染
- 分类、标签检索文章
- 文章评论与回复
- 留言板功能
- 友情链接展示
- 响应式适配移动端/PC端

### 后台功能
- 管理员登录认证
- 文章发布、编辑、删除
- 分类管理（增删改查）
- 标签管理（增删改查）
- 评论审核与管理
- 留言管理
- 友情链接管理
- 数据统计展示

## 快速启动
### 1. 环境准备
- JDK 1.8+
- MySQL 5.7+
- Redis 5.0+
- Maven 3.6+
- Node.js 14.x

### 2. 后端启动
1. 创建数据库 `blog`，执行 `resources/blog.sql`
2. 修改 `application.yml` 中的数据库和 Redis 配置
3. 启动后端服务（默认端口 8080）

### 3. 前端启动
```bash
# 安装依赖
npm install

# 启动项目
npm run dev
```
前端访问地址：`http://localhost:8081`

### 4. 登录信息
- 后台地址：`http://localhost:8081/admin`
- 账号：`admin`
- 密码：`123456`

## 项目结构
### 后端
```
src/main/java/com/blog/
├── config/        # 配置类
├── controller/    # 接口控制器
├── entity/        # 实体类
├── mapper/        # 数据访问
├── service/       # 业务逻辑
└── util/          # 工具类
```

### 前端
```
src/
├── api/           # 接口请求
├── assets/        # 静态资源
├── components/    # 公共组件
├── router/        # 路由
├── store/         # 状态管理
└── views/         # 页面（前台+后台）
```

## 部署说明
- 前端打包：`npm run build`
- 后端打包：`mvn package -DskipTests`
- 生产环境：Nginx + Spring Boot Jar 部署

## 常见问题
- **数据库连接失败**：检查 MySQL 服务、账号密码
- **前端依赖报错**：使用 `npm install --legacy-peer-deps`
- **Redis 连接失败**：确认 Redis 服务启动
- **接口请求失败**：检查后端是否启动

## 许可证
MIT License


