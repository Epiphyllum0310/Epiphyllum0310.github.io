---
title: template
date: 2026-03-18 21:30:00
tags:
  - 模板
  - Markdown
  - Hexo
categories:
  - 博客写作
math: true
---

> 这是一篇可复用的博客模板，覆盖常见写作元素：标题、目录层级、列表、表格、图片、代码、公式、引用、脚注、网页嵌入、视频嵌入、折叠块等。以后写新文章时，直接复制本篇修改即可。

---

# 一、文章简介

这里写本文简介。

例如：

本文用于演示在 Hexo + Fluid 博客中如何组织一篇完整文章，并展示常见博客排版要素，方便后续直接作为写作模板复用。

---

# 二、基础文本排版

这是普通正文段落。

你可以使用**加粗**、*斜体*、~~删除线~~、`行内代码`。

也可以插入链接：

- [Hexo 官方文档](https://hexo.io/docs/)
- [Fluid 主题文档](https://hexo.fluid-dev.com/docs/)

---

# 三、列表

## 3.1 无序列表

- 第一项
- 第二项
- 第三项
  - 子项 A
  - 子项 B

## 3.2 有序列表

1. 第一步
2. 第二步
3. 第三步

## 3.3 待办列表

- [x] 已完成内容
- [ ] 未完成内容
- [ ] 后续补充内容

---

# 四、引用块

> 这是一个引用块。
>
> 适合用于：
> - 摘要
> - 提醒
> - 结论
> - 重要定义

> **示例：**
> “复杂问题的表达方式，往往决定后续分析效率。”

---

# 五、分割线

下面是一条分割线：

---

# 六、表格

## 6.1 普通表格

| 项目 | 说明     | 备注     |
| ---- | -------- | -------- |
| 标题 | 文章名   | 必填     |
| 日期 | 发布时间 | 建议保留 |
| 标签 | 用于检索 | 可多个   |
| 分类 | 用于归档 | 建议填写 |

## 6.2 对比表格

| 方法   | 优点       | 缺点     | 适用场景   |
| ------ | ---------- | -------- | ---------- |
| 方法 A | 简单直接   | 精度一般 | 快速验证   |
| 方法 B | 精度较高   | 实现复杂 | 正式分析   |
| 方法 C | 可解释性强 | 速度较慢 | 小规模研究 |

---

# 七、图片

## 7.1 单张图片

把图片放在：

```text
source/img/
```

例如图片路径为：

```text
source/img/example-figure.png
```

插入方式：

![示例图片](/img/example-figure.png)

## 7.2 带图注图片

![算法流程图](/img/example-flowchart.png)

*图 1：算法流程示意图。*

## 7.3 使用 HTML 控制图片大小

<img src="/img/example-figure.png" alt="示例图片" width="500" />

---

# 八、代码块

## 8.1 Python 示例

```python
import numpy as np

def gaussian(x, mu=0.0, sigma=1.0):
    return np.exp(-(x - mu)**2 / (2 * sigma**2))

x = np.linspace(-5, 5, 1000)
y = gaussian(x)

print(y[:5])
```

## 8.2 C 示例

```c
#include <stdio.h>

int main() {
    printf("Hello, world!\n");
    return 0;
}
```

## 8.3 Bash / 命令行

```bash
hexo clean
hexo generate
hexo server
```

## 8.4 JSON 示例

```json
{
  "title": "example",
  "author": "Epiphyllum",
  "tags": ["blog", "template"]
}
```

---

# 九、数学公式

这是一个行内公式：$E = mc^2$。

这是另一个例子：$\int_a^b f(x)\,\mathrm{d}x$。

## 9.1 独立公式

$$
E = mc^2
$$

$$
\frac{\partial u}{\partial t} = D \frac{\partial^2 u}{\partial x^2}
$$

## 9.2 多行公式

$$
\begin{aligned}
a^2 + b^2 &= c^2 \\\\
e^{i\theta} &= \cos\theta + i\sin\theta
\end{aligned}
$$

## 9.3 常见科研写法

$$
\mathcal{L} = \sum_{n=1}^{N} \left| y_n - \hat{y}_n \right|^2
$$

$$
A(\tau) = \int \mu_X(t)\,\mu_X(t+\tau)\,\mathrm{d}t
$$

---

# 十、提示块

> **提示**
>
> 这里可以放注意事项、参数说明、使用建议等。

> **警告**
>
> 如果图片路径写错，网页会显示空白图或裂图。

> **结论**
>
> 对于重复使用的文章结构，建议长期保留一份模板文件。

---

# 十一、脚注

这是一个带脚注的例子[^1]。

[^1]: 这里是脚注内容，可用于补充解释、参考说明等。

---

# 十二、网页嵌入（iframe）

> 注意：部分网站禁止被 iframe 嵌入，因此不一定都能正常显示。

下面是一个网页嵌入示例：

```html
<iframe
  src="https://example.com"
  width="100%"
  height="400"
  style="border:1px solid #ccc; border-radius:8px;"
  loading="lazy">
</iframe>
```

实际写入正文时可直接这样放：

<iframe
  src="https://example.com"
  width="100%"
  height="400"
  style="border:1px solid #ccc; border-radius:8px;"
  loading="lazy">
</iframe>

---

# 十三、视频嵌入

## 13.1 本地视频

如果你有本地视频文件：

```text
source/video/demo.mp4
```

可以这样写：

```html
<video width="100%" controls>
  <source src="/video/demo.mp4" type="video/mp4">
  您的浏览器不支持 video 标签。
</video>
```

## 13.2 外部视频嵌入

```html
<iframe
  width="100%"
  height="450"
  src="https://www.youtube.com/embed/dQw4w9WgXcQ"
  title="YouTube video player"
  frameborder="0"
  allowfullscreen>
</iframe>
```

---

# 十四、折叠块

<details>
  <summary>点击展开更多内容</summary>

这里可以放补充推导、额外说明、参考资料或长代码段。

例如：

- 推导细节 1
- 推导细节 2
- 推导细节 3

</details>

---

# 十五、文章结构建议

一篇技术博客通常可以按下面结构组织：

1. 问题背景
2. 方法介绍
3. 推导或实验过程
4. 结果展示
5. 分析讨论
6. 总结与展望

---

# 十六、正式技术博客示例段落

## 16.1 研究背景

在很多问题中，我们需要从观测数据中恢复潜在结构。对于这类任务，一个常见思路是先建立数学模型，再通过数值计算分析其行为。

## 16.2 模型表达

考虑如下目标函数：

$$
J(\theta) = \sum_{i=1}^{N} \left( y_i - f(x_i;\theta) \right)^2
$$

其中，$\theta$ 为待估参数，$f(x_i;\theta)$ 为模型输出。

## 16.3 数值实现

```python
import numpy as np

def loss(theta, x, y):
    y_pred = theta[0] * x + theta[1]
    return np.sum((y - y_pred)**2)

x = np.array([1, 2, 3, 4])
y = np.array([2.1, 4.2, 5.9, 8.1])

theta = np.array([2.0, 0.1])
print(loss(theta, x, y))
```

## 16.4 结果展示

| 参数       | 数值 |
| ---------- | ---: |
| 斜率       |  2.0 |
| 截距       |  0.1 |
| 损失函数值 | 0.07 |

## 16.5 结果分析

从结果可见，当前模型已经较好拟合数据趋势，但仍可进一步优化参数估计方式，提高泛化能力。

---

# 十七、总结

本文给出了一篇适合长期复用的博客模板，涵盖了：

- 基础文本
- 列表
- 表格
- 图片
- 代码
- 公式
- 引用
- 脚注
- iframe 嵌入
- 视频嵌入
- 折叠块

后续写文章时，可以直接复制本文件，并只修改：

1. Front-matter
2. 标题
3. 正文内容
4. 图片路径
5. 代码与公式

---

# 十八、可直接复用的最简写作骨架

如果你只想快速开写，可以直接复制下面这一小段：

```markdown
---
title: 文章标题
date: 2026-03-18 21:30:00
tags:
  - 标签1
  - 标签2
categories:
  - 分类名
math: true
---

# 一、问题背景

这里写背景。

# 二、方法

这里写方法。

# 三、结果

这里写结果。

# 四、总结

这里写总结。
```