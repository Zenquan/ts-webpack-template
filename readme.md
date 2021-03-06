# ts-webpack-template

## 背景

>现在随着typescript的完善发展，许多的适用于大项目的功能特性体现出来了，所以学习typescript对于一个有追求的前端er来说是非常有必要的。

我相信你有100个选择typescript的理由，也有100个拒绝的理由。

就我个人选择使用的情况有以下：
- 1.面向接口编程，当你根据后端给你返回的数据结构定义好数据结构，后续在开发前端时候也能提前预知会有什么问题出现， 后续接口字段修改也便于维护。

- 2.类型系统。大大减少重构过程中引入意外错误的机会。


那么就要搭建一下typescript的环境，有两个方案：
- 1.使用webstrom立即编译的功能，但是webstrom的注册码老是失效，还涉及到软件版权的问题，还是算了。
- 2.使用webpack热更新的功能结合typescript和ts-loader来搭建实时编译的环境。

## 特性

- 1.TypeScript：面向接口、类型检查；
- 2.高度可扩展：自定义webpack配置；
- 3.TDD、覆盖率测试的webpack环境: 测试驱动开发、测试覆盖率；
- 4.vuepress文档工具，主题可配置。

## 使用

### 下载并安装依赖
```bash
git clone https://github.com.cnpmjs.org/Zenquan/ts-webpack-template.git
cd ts-webpack-template
npm install
or 
yarn 
```
### 启动
```bash
npm run start
```
### 打包
```bash
npm run build
```

### 目录

```bash
|-- build目录下
  |--build.js // 打包生产配置
  |--loaders.js // loader安装后配置
  |--optimization.js // 优化配置
  |--plugin.js // plugin安装后配置
  |--start.js // 本地开发配置
  |--utils.js // 工具，e.g. 处理路径的函数
  |--webpack.config.js // webpack公共配置

|-- docs 文档目录
  |-- .vuepress 文档

|--src目录
  |-- lib
    |--index.ts // 轮子入口
    |--math.ts
    |--xxx.ts // 其他

|-- deploy.sh用于发布工具文档上github // deploy.sh "feat:增加文档功能" "feat:增加文档功能"
|-- package.json //"docThemeConfig": {} //配置vuepress文档主题
|-- zen.config.js // 自定义配置
```

## 日志

- 2019.01.19 初始化项目，完成简单的ts开发热更新、打包编译
- 2020.06.07 重写webpackts开发热更新、打包编译的配置
- 2020.06.21 webpack配置分层，做到更好的扩展
- 2020.06.22 加入mocha+chai TDD测试驱动开发方式、jest测试覆盖率
- 2020.06.26 提供zen.config.js覆盖build中的配置
- 2020.06.27 把zen.config.js的loader提取后放入build/loaders.js中
- 2020.06.27 把zen.config.js的plugin提取后放入build/plugins.js中
- 2020.06.27 把zen.config.js的optimization提取后放入build/optimization.js中
- 2020.06.29 增加文档功能
- 2020.06.30 优化更新ts-webpack-template文档
- [ ] 加入eslint
- [ ] 根据代码的规范注释生成文档
- [ ] 利用babel-import-plugins来实现按需引入
- [ ] 代码生层次压缩
