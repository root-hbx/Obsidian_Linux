刚刚我们说了文字是很常见的一种表达方式，用`txt`文件就可以在计算机中方便的呈现文字；我们也说了格式是可以增强文本的表现力的，比如用`Word`给这些文字添加格式。

`Markdown`其实是一种写作风格/方式，我们用这种风格/方式写出来的**纯文本文件**（和`.txt`是一样的）叫做**markdown文件**，一般以`.md`作为文件后缀（而不是`.txt`）。

`.md`文件虽然是纯文本，但其中用一些特殊的字符（如`* # [] () …`）给纯文本带来格式（这与`html`文件是相似的，也可以将`markdown`看作是**简单的html**）。这些格式通过某种方式进行渲染（注：渲染：指将计算机中的某些数据呈现在屏幕上）你就可以看到它们代表的格式了！
## 1. HEADERS 标题
`1`～`6`个 '#' 号加一个空格再加上标题的名称
```markdown
## 一级标题
### 二级标题
……
###### 六级标题
```
## 2. EMPHASIS 加粗和斜体
```markdown
*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_
```

语句两边各加一个 \* 形成斜体：
*This text will be italic*

语句两边各加一个 \_ 形成斜体：
_This will also be italic_

语句两边各加一个 \*\* 形成斜体：
**This text will be bold**

语句两边各加一个 \_\_ 形成斜体：
__This will also be bold__

语句符号中 \_ 与 \* 的混搭：
_You **can** combine them_
## 3. LISTS 列表
### 3.1 Unordered 无序列表
```markdown
* Item 1       --- 一级列表
* Item 2       --- 一级列表
    * Item 2a  --- 二级列表
    * Item 2b  --- 二级列表
```

这里可以缩进的！

enter后自动平移到同级下一列表；tab后自动跳转同下一级新启列表！

* Item 1
* Item 2
	* Item 2_a
	* Item 2_b
### 3.2 Ordered 有序列表
```markdown
1. Item 1
1. Item 2
1. Item 3
    1. Item 3a
    1. Item 3b
```

这里可以缩进的！

缩进会重新编号，或者变成小标题（如`1.1` `2.1.3`这样）

1. task 1
2. task 2
3. task 3
	1. task 3_1
	2. task3_2
### 3.3 Task Lists 任务列表
```markdown
- [x] this is a complete item
- [ ] this is an incomplete item
```

鼠标点击后就会“自动打勾” <=> 在 \[ \] 内加上 'x'

- [x] this is a complete item
- [ ] this is an incomplete item
## 4. LINKS 链接
`[Text](url)`：中括号，后面小括号。小括号里面放链接，中括号里面放说明（必须）；不需要说明的话，可以直接写链接

直接写链接会直接被转换为可以点击的链接；也可以在两侧加上`<`和`>`

```markdown
[GitHub Official Site](https://github.com)

https://github.com

<https://github.com>
```
1. \[Your Description]( the Url of Website)
> [GitHub Official Site](https://github.com/)

2. 直接写链接会自动转换成可点击的网址
> https://github.com

3. 间接写链接：在两侧加上`<`和`>`
> [https://github.com](https://github.com/)
## 5. IMAGES 图片
`![Text](url)`：感叹号，中括号，小括号。

小括号里面放图片链接，中括号里面放图片说明（不必须；写了的话会在图片下方或某处显示说明，当因为某种原因图片无法加载的时候，显示时也会用说明替代图片）

![GitHub Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)
## 6. CODEING 代码
### 6.1 INLINE CODE 行内代码
直接用\`...\`表述即可
### 6.2 CODE BLOCK 代码块
用一对三个反撇 \`\`\` 包裹，在最开始三个反撇后可以加代码的语言名称或简写以在渲染时获得高亮支持！

一般支持的代码高亮会有很多，比如：`shell`、`bash`、`c`、`cpp`、`java`、`objectivec`、`python`、`swift`、`yaml`、`html`、`xml`等

```cpp
#include<iostream>
#include<algorithm>
using namespace std;
int main()
{
    int a;
    cin >> a;
    cout << a <<endl;
	return 0;
}
```
## 7. QUATE 引用
我习惯于用它来在文章开头写一下文档的更新日期等前置事项：

```markdown
As Tim Cook said:

> Fearlessness means taking the frst step, 
> even if you don't know where it will take you.
```

As Tim Cook said:

> Fearlessness means taking the frst step, 
> even if you don't know where it will take you.
## 8. TABLES 表格
```markdown
|hbx|cqy|wlr|
|:---:|:---:|:---:|
|1|2|3|
|4|5|6|
```

| hbx | cqy | wlr |
| :--: | :--: | ---- |
| 1 | 2 | 3 |
| 4 | 5 | 6 |
注意：
- |:---:| 表示：框内文本内容居中对齐
- 表格代码文本与钱文内容至少需要空一个行
## 9. Enter 换行
有的时候你在`markdown`明明换行了，可是上传到`GitHub`上面一看，文字都粘在一起了。这是为什么呢？

英文在分段的时候，不像我们写文章段前空两格，他们会直接在两段之间多空一行。一般的回车只是用来方便阅读，不然一行的内容太长了。

如果你不希望这种方式生效，可以在一行后面加两个空格；但这样很麻烦，还是多加回车吧；最好在每种语法前后都空行，这样也能有效减少语法不被识别的情况（PS：多于2个的连续回车markdown会将它们当作一个回车）
## 10. 推荐的Markdown支持平台
### 10.1 obsidian
[参考](https://csdiy.wiki/%E5%BF%85%E5%AD%A6%E5%B7%A5%E5%85%B7/workflow/)
工作流的骨架围绕 `单个知识点多参考源，勤于提问给多个知识点之间建立联系` 的底层核心逻辑建立。我们写论文其实就是遵循这个底层逻辑的。论文一般会有脚注去解释一些关键字，并且论文末尾会有多个参考的来源，但是我们平时写笔记会随意得多，因此需要更灵活的方式。

平时写代码习惯在 IDE 里一键跳转，把相关的函数和实现很好地联系在了一起。你也许会想，如果笔记也能像代码那样可以跳转就好了。现在市面上 `双链笔记软件` 就可以很好地解决这一痛点，例如 Roam Research、Logseq、Notion 和 Obsidian。Roam Research 和 Logseq 都是基于大纲结构的笔记软件，而 `大纲结构` 是劝退我使用这两款软件的原因。一是 `大纲结构` 做笔记容易使文章纵向篇幅太长，二是如果嵌套结构过多会占横向的篇幅。Notion 页面打开慢，弃之。最终我选择了 Obsidian，原因如下：

- Obsidian 基于本地，打开速度快，且可存放很多电子书。我的笔记本是 32g 内存的华硕天选一代，拿来跑 Obsidian 可以快到飞起
- Obsidian 基于 Markdown。这也是一个优势，如果笔记软件写的笔记格式是自家的编码格式，那么不方便其他第三方拓展，也不方便将笔记用其他软件打开，比如 qq 音乐下载歌曲有自己的格式，其他播放器播放不了，这挺恶心人的
- Obsidian 有丰富的插件生态，并且这个生态既大又活跃，即插件数量多，且热门插件的 star 多，开发者会反馈用户 issue，版本会持续迭代。借助这些插件，可以使 Osidian 达到 `all in one` 的效果，即各类知识来源可以统一整合于一处

=> [obsidian_官网](https://obsidian.md/)
### 10.2 Markdown All in One
安装插件`Markdown All in One`，会支持不少快捷操作。

`VS Code`作为编辑器之神，写`markdown`肯定没问题！直接新建`markdown文件`就可以编辑了！

一般来说，软件开发的项目中，代码都是和`markdown文件`在一起的，以后如果有一些需要在`VS Code`打开的项目，使用`VS Code`编写`README.md`或者其他的`markdown文件`也是很方便的一个选择。
## Appendix1 文字编辑技巧
**仅限MacOS：**

〇 双击选中一个词：这里词指一个中文的词语或者一个英文的单词

〇 三击选中一行

〇 ⌥左右：以词为单位移动光标

〇 ⌘上下左右：移动光标到行首/行未/文头/文末

〇 按住⇧：文字选中；⇧上下左右 / ⇧⌥左右 / ⌘⇧上下左右

〇 按住⌥：矩形区域选中

〇 ⌥⌫、⌘⌫；fn⌫：删除词、删除到行首；向后删除 delete；⌘X也是一种删除的方式
## Appendix 2 LaTeX & Markdown
注意一下，反斜线还有行内代码可以用来输入可能会被当作`markdown`语法的符号：比如你想在markdown中输入一个星号`*`，可能你一不小心就发现星号被markdown渲染成了格式。这时你可以用行内代码包裹，`*`，或者用反斜线`\*`，这样markdown就不会把这些符号当成格式了。

如果我们只是写简单的`Markdown`文稿，上面的这些语法已经完全够用了。

不过既然能用符号表示格式，那么能不能添加更多的语法进来呢？


