## 环境

- [Node.js](https://www.runoob.com/nodejs/nodejs-tutorial.html) v10.13.0
- [yarn](https://yarnpkg.com/lang/zh-hans/docs/) v1.12.3

## 组件开发流程

组件开发需要 2 个仓库，本仓库和新项目，统一使用 yarn 进行包管理和运行。

1. 初始化一个新项目
2. 在本项目下执行 `yarn link`
3. 在本项目内运行 `yarn watch`，将会自动监听 `src` 下的文件变动，自动将新代码编译到 `lib`
4. 在新项目中执行 `yarn link markdown-nice`
5. 启动新项目 `yarn start`

运行后即可在浏览器中访问`http://localhost:3000`看到页面了

发布

```shell
$ yarn publish:npm
$ npm publish
```

使用 npm 包

```shell
$ yarn unlink markdown-nice
$ yarn add markdown-nice
$ yarn start
```

## 主要开发库

- [React](https://github.com/facebook/react "React")：facebook 开源的 js 视图层框架
- [markdown-it](https://github.com/markdown-it/markdown-it "markdown-it")：markdown 转换富文本解析器
- [juice](https://github.com/Automattic/juice "juice")：将 CSS 类选择器转换为行内样式的工具
- [codemirror](https://github.com/codemirror/codemirror "codemirror")：网页代码编辑器
- [ant-design](https://github.com/ant-design/ant-design "ant-design")：React UI组件库
- [mobx](https://github.com/mobxjs/mobx "mobx")：状态管理库
- [highlight.js](https://github.com/highlightjs/highlight.js "highlight.js")：代码高亮库
- [MathJax](https://github.com/mathjax/MathJax "MathJax-node")：公式转图片库
- axios、ali-oss、qiniu-js等

## 目录结构

```shell
├── README.md                   // 项目说明
├── package.json                // 依赖包
├── main.js                     // 打包electron
└── src                         // 源代码
    ├── component               // 组件            
    ├── icon                    // 图表                 
    ├── layout                  // 布局
    ├── store                   // 状态管理
    ├── template                // 模板
    │   ├── code                // 代码样式
    │   ├── markdown            // 主题样式
    │   ├── basic.js            // 基础样式
    │   └── content.js          // 示例文章
    ├── utils                   // 通用库
    └── App.js                  // 入口
```