## 公式编写注意点

1. `mdnice` 的数学公式支持是基于 `MathJax 3` 最新发行版开发的，`MathJax 3` 最新发行版不支持的和 bug，`mdnice` 同样存在。遇到问题请提供代码文本和渲染结果截图。
2. 为了与 `mdnice` 其它语法兼容，不要用 `\( \)` `\[ \]`，用 `$ $` 和 `$$ $$`。
3. `Mathjax` 不是 `LaTeX` 只是部分兼容 `LaTeX`，相互转换不是 100% 兼容。公式输入不是零基础的，如果不熟悉相关语法，花几分钟浏览下[MathJax 总结](https://www.zybuluo.com/yangfch3/note/267947)或者[如何插入数学公式](https://www.yuque.com/yuque/help/math)是很有必要的。
4. 不支持 `actuarialsymbol` 宏包，临时办法定义新命令 
```tex
$\def\angln#1{\overline{#1\,}\kern-3mu\lower-3mu|}$
$\def\angld#1{\overline{#1\,}\kern-3mu\lower-1mu\small|}$
$$\angld{x}$$ 高度低的使用
$$\angln{x2323}$$ 高度正常的使用
```
5. 公式支持公众号和知乎。

6. 公式中含有 `<` 的需要在 `<` 后面加一个空格，具体原因见 Mathjax 官方文档 [html-special-characters](http://docs.mathjax.org/en/latest/input/tex/html.html#html-special-characters)。

7. 如果遇到公式粘贴到公众号中 `图片粘贴失败` 的提示，这个原因目前未知，不同公众号反应不一样，只能通过插入代码的方式解决问题，可参考如下视频

<video style="width:100%;" controls>
  <source src="https://imgkr.cn-bj.ufileos.com/3911b986-a98b-46cc-9383-5725179b6eca.mp4" type="video/mp4">
</video>