# lottery-Web

前端

## 技术栈

- 框架
    - [Vue.js](https://vuejs.org/)
- 构建工具
    - [Vite](https://vitejs.dev/)
- 代码规范
    - [ESLint](https://eslint.org/)
    - [Prettier](https://prettier.io/)
- 路由
    - [Vue Router](https://router.vuejs.org/)
- 状态管理
    - [Pinia](https://pinia.vuejs.org/)
- 样式
    - [Tailwind CSS](https://tailwindcss.com/)
- HTTP 请求
    - [fetch](https://developer.mozilla.org/zh-CN/docs/Web/API/Fetch_API)
- UI 组件库
    - [daisyUI](https://daisyui.com/)
- 图标库
    - [FontAwesome](https://fontawesome.com/)
- 字体库
    - [字图 CDN](https://chinese-font.netlify.app/zh-cn/cdn) / [抖音美好体](https://chinese-font.netlify.app/zh-cn/fonts/dymh/DouyinSansBold)

## 项目结构

    ```plaintext
    .
    ├── .husky              # Git 钩子
    ├── .vscode             # VSCode 配置与扩展
    ├── config              # 项目配置文件
    ├── node_modules        # 项目依赖
    ├── public              # 静态资源
    ├── src                 # 源码
    │   ├── assets          # 静态资源
    │   ├── components      # 组件
    │   ├── pages           # 页面
    │   ├── router          # 路由
    │   ├── stores          # 状态管理
    │   ├── utils           # 工具函数
    │   ├── App.vue         # 根组件
    │   ├── main.js         # 入口文件
    │   └── styles.css      # 样式
    ├── .gitattributes      # Git 格式化提交配置
    ├── .gitignore          # Git 代码跟踪忽略规则
    ├── .npmrc              # NPM 镜像源配置
    ├── .prettierrc.cjs     # Prettier 配置
    ├── eslint.config.js    # ESLint 配置
    ├── index.html          # HTML 模板
    ├── LICENSE             # 开源协议
    ├── package.json        # 项目信息
    ├── README.md           # 项目说明
    ├── vercel.json         # Vercel 部署配置
    └── vite.config.js      # Vite 配置
    ```

## 如何运行项目

1. 前置条件

    - Node.js 22 LTS 及以上版本
    - NPM / Yarn / PNPM

2. 安装依赖

    ```bash
    pnpm i
    ```

3. 启动项目

    ```bash
    pnpm dev
    ```

4. 打包构建项目

    ```bash
    pnpm build
    ```

# lottery-Server

see [midway docs][midway] for more detail.

## 项目结构

```plaintext
midway.js-Server
├── package.json              # 定义项目的基本信息，依赖项，脚本等
├── .eslintrc.js              # ESLint 配置文件，用于定义代码风格和检查规则
├── .prettierrc.js            # Prettier 配置文件，用于定义代码格式化规则
├── .gitignore                # Git 忽略文件，列出不需要纳入版本控制的文件和目录
├── .npmrc                    # npm镜像源配置文件
├── yarnrc                    # yarn镜像源配置文件
├── bootstrap.js              # 应用启动脚本，用于初始化和启动应用，配置了链路追踪
├── jest.config.js            # Jest 测试框架的配置文件
├── src                       # 源码
│   ├── config                # 存放应用的配置文件
│   ├── controller            # 存放控制器文件，处理 HTTP 请求
│   ├── service               # 存放服务层代码，包含业务逻辑
│   ├── dao                   # 数据访问对象层，用于数据库操作
│   ├── middleware            # 存放中间件，用于处理请求和响应的中间逻辑
│   ├── filter                # 存放过滤器，用于请求和响应的预处理和后处理
│   ├── dbConnPool            # 数据库连接池配置
│   ├── dto                   # 数据传输对象，用于定义请求和响应的数据结构
│   ├── guard                 # 存放守卫，用于权限控制
│   ├── test/controller       # 存放控制器的测试代码
│   └── configuration.ts      # 应用的配置文件，用于定义全局配置
├── LICENSE                   # 开源协议
├── tsconfig.json             # TypeScript 编译器的配置文件
├── yarn.lock                 # 锁定依赖版本的文件
└── README.md                 # 项目说明
```

### 快速启动

```bash
$ yarn                               # 下载package.json里的依赖项
$ yarn run dev                       # 启动项目
$ open http://localhost:7001/      
```

### NPM脚本作用

```bash
$ yarn run start                      # 启动项目并启动链路追踪
$ yarn run dev                        # 启动项目的开发模式
$ yarn run test                       # 运行项目的测试用例
$ yarn run cov                        # 生成测试覆盖率报告
$ yarn run lint                       # 检查代码中的错误和不符合代码规范的地方
$ yarn run lint:fix                   # 自动修正代码中能够自动修复的lint错误
$ yarn run ci                         # 执行持续集成（CI）流程中的脚本
$ yarn run check                      # 检查项目环境配置
$ yarn run build                      # 构建项目，生成生产环境下的代码
```

[midway]: https://midwayjs.org
