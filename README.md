Spring Boot 个人博客全栈项目
基于 Spring Boot + MyBatis-Plus + Vue 前后端分离的个人博客系统，具备文章管理、分类管理、标签管理、评论、留言、用户管理等核心功能，界面简洁优雅，易于部署和扩展，适合作为个人学习、毕业设计或生产环境使用的博客平台。
项目介绍
本项目是一套前后端分离的个人博客全栈解决方案，后端采用 Spring Boot 2.x 框架，集成 MyBatis-Plus 实现高效数据操作，使用 Redis 实现缓存优化；前端基于 Vue + Element UI 构建响应式界面，支持 PC 端 / 移动端自适应。
系统分为前台博客展示端和后台管理端：
前台：文章浏览、分类 / 标签检索、评论互动、留言板、友链展示
后台：文章发布 / 编辑、分类标签管理、评论审核、用户管理、系统配置
项目结构清晰、代码规范、注释完善，开箱即用，非常适合 Spring Boot 全栈开发学习与实战。
技术栈
后端技术
核心框架：Spring Boot 2.7.x
ORM 框架：MyBatis-Plus
安全框架：Spring Security
缓存中间件：Redis
数据库：MySQL 5.7 / 8.0
工具类：Hutool、Lombok
构建工具：Maven
前端技术
核心框架：Vue 2.x
UI 组件库：Element UI
路由管理：Vue Router
状态管理：Vuex
网络请求：Axios
构建工具：Vue CLI
环境依赖
JDK 1.8+
MySQL 5.7+
Redis 5.0+
Maven 3.6+
Node.js 14.x
功能特性
前台功能
✅ 首页文章列表、热门文章、最新评论展示
✅ 文章详情页，支持 Markdown 渲染
✅ 文章分类、标签快速检索
✅ 文章评论、回复功能
✅ 留言板互动
✅ 友链展示页面
✅ 响应式布局，适配手机 / 平板 / PC
后台功能
✅ 管理员登录 / 权限控制
✅ 文章发布、编辑、删除、上下架
✅ 分类管理（增删改查）
✅ 标签管理（增删改查）
✅ 评论管理、审核、删除
✅ 留言管理
✅ 友链管理
✅ 系统基础配置
✅ 数据统计展示
项目结构
后端目录结构
plaintext
springboot-blog/
├── src/main/java/com/blog/
│   ├── config/         # 配置类（Redis、Security、跨域等）
│   ├── controller/     # 控制器层（接口定义）
│   ├── entity/         # 实体类
│   ├── mapper/         # 数据访问层
│   ├── service/        # 业务逻辑层
│   │   ├── impl/       # 业务实现类
│   ├── util/           # 工具类
│   └── BlogApplication.java  # 项目启动类
├── src/main/resources/
│   ├── application.yml # 核心配置文件
│   └── blog.sql        # 数据库脚本
├── pom.xml             # Maven 依赖配置
└── README.md
前端目录结构
plaintext
vue-blog/
├── src/
│   ├── api/            # 接口请求封装
│   ├── assets/         # 静态资源（图片、样式）
│   ├── components/     # 公共组件
│   ├── router/         # 路由配置
│   ├── store/          # 状态管理
│   ├── views/          # 页面组件
│   │   ├── front/      # 前台页面
│   │   └── admin/      # 后台管理页面
│   └── App.vue         # 根组件
└── vue.config.js       # Vue 配置文件
快速开始
一、环境准备
安装 JDK 1.8、MySQL、Redis、Maven、Node.js
启动 MySQL 和 Redis 服务
二、后端部署
克隆项目
bash
运行
git clone https://github.com/你的用户名/springboot-blog.git
cd springboot-blog
创建数据库并执行 SQL
新建数据库 blog
执行项目中 resources/blog.sql 脚本
修改配置文件
打开 application.yml，修改数据库、Redis 配置：
yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/blog?useUnicode=true&characterEncoding=utf-8&serverTimezone=Asia/Shanghai
    username: 你的数据库账号
    password: 你的数据库密码
  redis:
    host: localhost
    port: 6379
安装依赖并启动
bash
运行
mvn clean install
# 启动项目
mvn spring-boot:run
后端启动成功：默认端口 8080
三、前端部署
进入前端目录
bash
运行
cd vue-blog
安装依赖
bash
运行
npm install
启动前端项目
bash
运行
# 开发环境启动
npm run dev
前端启动成功：默认地址 http://localhost:8081
四、访问系统
前台页面：http://localhost:8081
后台管理：http://localhost:8081/admin
管理员账号：admin 密码：123456
接口文档
后端接口遵循 RESTful 规范，核心接口示例：
文章列表：GET /api/article/list
文章详情：GET /api/article/{id}
分类列表：GET /api/category/list
评论提交：POST /api/comment/save
可通过 Swagger/Knife4j 查看完整接口文档（项目已集成）。
部署说明
生产环境部署
前端打包
bash
运行
npm run build
生成 dist 静态文件，部署到 Nginx
后端打包
bash
运行
mvn clean package -DskipTests
生成 jar 包，通过 java -jar 命令启动
Nginx + 后端服务 完成生产部署
常见问题（FAQ）
Q：启动后端报数据库连接失败？
A：检查 MySQL 服务是否启动，配置文件中的账号密码是否正确。
Q：前端启动报依赖错误？
A：使用 npm install --legacy-peer-deps 安装依赖。
Q：Redis 连接失败？
A：确认 Redis 服务已启动，无密码 / 密码配置正确。
Q：页面无法访问接口？
A：检查后端是否正常启动，前端接口地址配置正确。
贡献指南
欢迎提交 Issue 和 Pull Request 一起完善项目！
Fork 本项目
创建特性分支 (git checkout -b feature/xxx)
提交修改 (git commit -m 'Add some feature')
推送到分支 (git push origin feature/xxx)
提交 Pull Request
许可证
本项目采用 MIT License 开源许可，欢迎学习和使用。
联系方式
项目地址：https://github.com/你的用户名 /springboot-vue-blog
如有问题，可提交 Issue 或联系开发者
