# Vue 3 + Typescript + Vite

## 安装依赖
    npm install
## 启动项目
    npm dev
## 目录结构
    ├── publish/
    └── src/
        ├── assets/                    // 静态资源目录
        ├── common/                    // 通用类库目录
        ├── components/                // 公共组件目录
        ├── router/                    // 路由配置目录
        ├── store/                     // 状态管理目录
        ├── style/                     // 通用 CSS 目录
        ├── utils/                     // 工具函数目录
        ├── views/                     // 页面组件目录
        ├── App.vue
        ├── main.ts
        ├── shims-vue.d.ts
    ├── tests/                         // 单元测试目录
    ├── index.html
    ├── tsconfig.json                  // TypeScript 配置文件
    ├── vite.config.ts                 // Vite 配置文件
    └── package.json
## 集成路由工具
    npm i vue-router@4
## 提交规范
### commit message 格式规范
  * commit message 由 Header、Body、Footer 组成。
  ```
    <Header>
    
    <Body>
    
    <Footer>
  ```
### Header
  Header 部分包括三个字段 type（必需）、scope（可选）和 subject（必需）。
  ```
    <type>(<scope>): <subject>
  ```
### type
  type 用于说明 commit 的提交类型（必须是以下几种之一）。

  |值|描述|
  |:----:|:----:|
  |feat|新增一个功能|
  |fix|修复一个 Bug|
  |docs|文档变更|
  |style|代码格式（不影响功能，例如空格、分号等格式修正）|
  |refactor|代码重构|
  |perf|改善性能|
  |test|测试|
  |build|变更项目构建或外部依赖（例如 scopes: webpack、gulp、npm 等）|
  |ci|更改持续集成软件的配置文件和 package 中的 scripts 命令，例如 scopes: Travis, Circle 等|
  |chore|变更构建流程或辅助工具|
  |revert|代码回退|

### scope
  scope 用于指定本次 commit 影响的范围。scope 依据项目而定，例如在业务项目中可以依据菜单或者功能模块划分， 如果是组件库开发，则可以依据组件划分。（scope 可省略）

### subject
  subject 是本次 commit 的简洁描述，长度约定在 50 个字符以内，通常遵循以下几个规范：
  * 用动词开头，第一人称现在时表述，例如：change 代替 changed 或 changes
  * 第一个字母小写
  * 结尾不加句号（.）

### Body
  body 是对本次 commit 的详细描述，可以分成多行。（body 可省略）跟 subject 类似，用动词开头，body 应该说明修改的原因和更改前后的行为对比。

### Footer
  如果本次提交的代码是突破性的变更或关闭缺陷，则 Footer 必需，否则可以省略。
  * 突破性的变更
    当前代码与上一个版本有突破性改变，则 Footer 以 BREAKING CHANGE 开头，后面是对变动的描述、以及变动的理由。
  * 关闭缺陷
    如果当前提交是针对特定的 issue，那么可以在 Footer 部分填写需要关闭的单个 issue 或一系列 issues。
