## 安装

```shell
$ yarn add markdown-nice
```

或者

```shell
$ npm install markdown-nice --save
```

若 npm install 过慢，建议使用 yarn 作为包管理工具。

其中的 mathjax 包下载速度可能比较慢，如果不需要公式支持，可以在 package.json 中删除 mathjax 部分

```shell
$ yarn remove mathjax
```

## React 示例

```javascript
import React from "react";
import MarkdownNice from "markdown-nice";

// 编辑器默认的内容
const defaultText = `编辑器默认的内容`;
// 标题，是一个字符串
const defaultTitle = "Markdown Nice";

// 自定义图床参数
const useImageHosting = {
  name: "自定义图床名称",
  url: "自定义图床URL"
  isSmmsOpen: true,
  isQiniuyunOpen: true,
  isAliyunOpen: true,
};

function App() {
  return (
    <MarkdownNice
      defaultTitle={defaultTitle}
      defaultText={defaultText}
      onTextChange={t => console.log("text => ", t)}
      useImageHosting={useImageHosting}
    />
  );
}

export default App;
```

其中 defaultTitle 属性不添加则左上角不显示，defaultText 属性不添加则默认每次从 localStorage 中获取值。

## React ref 使用示例

```javascript
import React from "react";
import MarkdownNice from "markdown-nice";

function App() {
  return (
    <MarkdownNice
      ref={mdnice => {
        mdnice.getWechatHtml(); // 获取微信公众号可用的富文本
        mdnice.getZhihuHtml(); // 获取知乎可用的富文本
      }}
    />
  );
}

export default App;
```

## Vue 使用示例

当前组件没有正式支持 Vue，可以参考[这里](https://github.com/ElyhG/vuera)来在 Vue 中引入组件

## API

|属性|说明|类型|默认值|
|---|---|---|---|
|defaultTitle|默认标题|string|-|
|defaultText|编辑器默认文字|string|-|
|onTextChange|编辑器文字变化的回调|function(text)|-|
|useImageHosting|图床配置|object|见下方|

### useImageHosting

类型

```
useImageHosting: {
  url: string;
  name: string;
  isSmmsOpen: boolean;
  isQiniuyunOpen: boolean;
  isAliyunOpen: boolean;
}
```

默认值

```
useImageHosting: {
  url: "",
  name: "",
  isSmmsOpen: true,
  isQiniuyunOpen: true,
  isAliyunOpen: true,
}
```

其中自定义图床 url 请参考[自定义图床接口](https://docs.mdnice.com/#/custom-image-hosting)