---
title: "Markdown 样式指南"
description: "这里是一些基本的 Markdown 语法示例，可以在 Blog 中编写 Markdown 内容时使用。"
pubDate: "Feb 08 2025"
image: /image/image3.png
categories:
  - tech
tags:
  - Makrdown
badge: Pin
---

这里是一些基本的 Markdown 语法示例，可以在 Blog 中编写 Markdown 内容时使用。

## 标题

以下 HTML `<h1>`—`<h6>` 元素代表六个级别的章节标题。`<h1>` 是最高的章节级别，而 `<h6>` 是最低的。

# H1

## H2

### H3

#### H4

##### H5

###### H6

## 段落

瑟鲁姆，何人或不明就里的解释，谁痛劳作。水的到来之速，欲望是愉悦的，若有所得的自足是快乐的，或者是与自己痛苦相等的，因为快乐啊，最大的快乐就是快乐的磨难，或者是在我们被鼓励的地方，那是快乐的意志，舒适的习惯，尽头的结构，到中心去追逐并拥有相同的事物？ 还有什么比欲望更强烈的冲动呢，当为了我们而有微不足道的志愿时，或者是一切，它在移动吗？ 无论如何。 因为，一切都是快乐的总和，因为某种痛苦的事物，并且那些是快乐的弧线，以至于他们自己，没有他们意识到在做什么。 当我逃避悲伤的时候，对于那些隐藏在表面之下和内心深处的事物来说，我必须把它作为自己的过错来加以实践，那就是痛苦的根源，时间的缓和，快乐的倾向，事物的回归，快乐的期望，痛苦的结束，是真实的。

开始吗？ 什么样的罪过会阻止你在事物中与否，让你感到不快乐呢？

## 图片

#### 语法

```markdown mockup-code
![Alt text](./full/or/relative/path/of/image)
```

#### 输出

![blog placeholder](/home.webp)

## 引用块

blockquote 元素表示从另一个来源引用的内容，可以选择带有必须在`footer`或`cite`元素中的引文，并且可以选择带有内联更改，例如注释和缩写。

### 无署名的引用块

#### 语法

```markdown
> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
>  **注意**，您可以在引用块中使用 _Markdown 语法_。
```

#### 输出

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Note** that you can use _Markdown syntax_ within a blockquote.

### 带署名的引用块

#### 语法

```markdown
> 不要通过共享内存来通信，而要通过通信来共享内存。<br>
> — <cite>Rob Pike[^1]</cite>
```

#### 输出

> 不要通过共享内存来通信，而要通过通信来共享内存。
> — <cite>Rob Pike[^1]</cite>

[^1]: The above quote is excerpted from Rob Pike's [talk](https://www.youtube.com/watch?v=PAAkCSZUG1c) during Gopherfest, November 18, 2015.

## 表格

#### 语法

```markdown
| 斜体   | 粗体     | 代码   |
| --------- | -------- | ------ |
| _斜体_ | **粗体** | `代码` |
```

#### 输出

| 斜体   | 粗体     | 代码   |
| --------- | -------- | ------ |
| _斜体_ | **粗体** | `代码` |

## 代码块

#### 语法

我们可以使用新行中的 3 个反引号 ``` 来编写代码片段，并在新行中使用 3 个反引号关闭。为了突出显示特定语言的语法，在第一个 3 个反引号后写一个语言名称单词，例如 html、javascript、css、markdown、typescript、txt、bash

````markdown
```cpp
#include <bits/stdc++.h>
using namespace std;
const int N = 1e5 + 5;
int n, k, a[N];
long long ans;
vector<int> v[N];
int main()
{
    scanf("%d%d", &n, &k);
    for (int i = 1; i <= n; i++)
    {
        scanf("%d", &a[i]);
        v[i % k].push_back(a[i]);
    }
    for (int i = 0; i < k; i++)
        sort(v[i].rbegin(), v[i].rend());
    for (int i = 0; i < k; i++)
    {
        for (int j = 0; j + 1 < v[i].size(); j += 2)
        {
            ans += v[i][j] + v[i][j + 1];
        }
    }
    printf("%lld\n", ans);
    return 0;
}
```
````

Output

```cpp
#include <bits/stdc++.h>
using namespace std;
const int N = 1e5 + 5;
int n, k, a[N];
long long ans;
vector<int> v[N];
int main()
{
    scanf("%d%d", &n, &k);
    for (int i = 1; i <= n; i++)
    {
        scanf("%d", &a[i]);
        v[i % k].push_back(a[i]);
    }
    for (int i = 0; i < k; i++)
        sort(v[i].rbegin(), v[i].rend());
    for (int i = 0; i < k; i++)
    {
        for (int j = 0; j + 1 < v[i].size(); j += 2)
        {
            ans += v[i][j] + v[i][j + 1];
        }
    }
    printf("%lld\n", ans);
    return 0;
}
```

## 列表类型

### 有序列表

#### 语法

```markdown
1. 第一项
2. 第二项
3. 第三项
```

#### 输出

1. 第一项
2. 第二项
3. 第三项

### 无序列表

#### 语法

```markdown
- 列表项
- 另一个项
- 还有另一个项
```

#### Output

- 列表项
- 另一个项
- 还有另一个项

### 嵌套列表

#### Syntax

```markdown
- 水果
  - 苹果
  - 橙子
  - 香蕉
- 奶制品
  - 牛奶
  - 奶酪
```

#### Output

- 水果
  - 苹果
  - 橙子
  - 香蕉
- 奶制品
  - 牛奶
  - 奶酪

## 其他元素

#### 语法

```markdown
<abbr title="图形交换格式">GIF</abbr> 是一种位图图像格式。

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

按 <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> 以结束会话。

大多数<mark>火蜥蜴</mark>是夜间活动的，捕食昆虫、蠕虫和其他小生物。
```

#### 输出

<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

按下 <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Delete</kbd></kbd> 结束对话。

大多数火蜥蜴是夜间活动的，捕食昆虫、蠕虫和其他小生物。
