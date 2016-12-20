## 第一章 关于CSS 2.1规范
* 应用：任何元素都具有所有属性，但一些属性在某些元素上没有渲染效果，例如，`clear`属性只对块级元素起作用。

## 第二章 CSS 2.1简介
* `h1 { color:red; }`
	* 一条CSS规则主要由两部分组成：选择器('h1')和声明('color: red')。声明有两部分：属性名('color')和属性值('red')。
* CSS 2.1 选择器和属性允许样式表引用文档或用户代理的以下部分：
	* 文档树中的元素和它们之间的某些关系（见选择器）
	* 文档树中的元素属性和它们的属性值（见属性选择器）
	* 元素内容的某些部分（见:first-line和:first-letter伪元素）
	* 文档树中的特定状态的元素（见伪类）
	* 将渲染文档的canvas的某些部分（aspect）
	* 某些系统信息（见用户界面）

## 第三章 一致性：需求与推荐标准
* 可替换元素( replaced element )：内容超出CSS格式化模型的元素，例如图片，内嵌的文档，或者applet。例如，HTML中IMG元素的内容通常被其"src"属性指定的图片替换。可替换元素通常拥有内在尺寸（intrinsic dimensions）：内在宽度，内在高度和内在比例（intrinsic ratio）。例如，位图图片有绝对单位指定的内在宽度，内在高度（明显可以确定内在比例）。另一方面，其它文档就没有内在尺寸（例如，空白的HTML文档）
	* 内在尺寸（Intrinsic dimensions）由元素自身定义的宽度和高度，不受环境影响。CSS不定义如何拿到这些内在尺寸。CSS 2.1中，只有可替换元素有内在尺寸。
* 编写者：编写者是编写文档和相关样式表的人。编辑工具是一种用来生成样式表的用户代理
* 用户：用户是与用户代理交互的想要看，听或者其它使用文档及相关样式表的人。用户可能提供一份个人样式表作为个人偏好
* 用户代理(UA)：用户代理是解释用文档语言编写的并应用了相关符合本文档术语的样式表的文档的任何程序。用户代理可能显示文档，把它读出来，打印出来，转化为其它格式等等。HTML用户代理是支持一种或多种HTML规范的用户代理。为了与本规范的目标一致，支持XHTML但不支持HTML的用户代理不是HTML用户代理
* 根据HTML 4定义，HEAD元素将在解析期间被推断出来并作为文档树的一部分，即便源文档里没有出现"head"标签。类似的，即便源文档中没有</p>和</li>标签，解析器也知道P和LI元素结束的位置
* XHTML（和其它基于XML的语言）文档行为不同：没有元素推断，并且所有元素都要有结束标签

## 第四章 语法和基本数据类型
* 