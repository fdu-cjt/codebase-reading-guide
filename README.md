# codebase-reading-guide

为希望学习项目实现的读者编写代码仓库导读，并直接在核心源码旁添加易懂、充分的教学注释。完整执行要求见 [SKILL.md](./SKILL.md)。

默认读者懂基本编程，但正在学习项目涉及的算法和框架。默认使用中文，保留代码标识符；用户指定语言或只需要导读、注释中的一项时，遵守用户要求。

## 提供什么

- **代码导读：** 少分大节，每节讲充分。代码树覆盖完整主要架构，重点文件统一标 `★【重要】`；概念解释基础公式、变量、用途和对应实现。
- **分层数据流图：** 先画总图建立整体认识，再用局部图展开感知、模型计算、运动或反馈等细节，不把所有内容挤进一张图。
- **教学注释：** 重要文件和核心函数开头说明职责、输入输出；内部解释关键变量、计算步骤、分支原因和结果用途。
- **覆盖检查：** 从入口追到实际计算，对照核心过程和函数清单检查遗漏。

核心代码块注释后的总行数默认至少达到原来的 125%。例如原来 80 行，注释后至少 100 行，不是要求新增注释达到原长度的 125%。不靠空行或重复句子凑数，不因反复润色而不断增加基线；比例达标之外，还要检查解释是否准确、易懂。

普通单元测试、mock、测试初始化、简单日志和样板代码默认不展开注释。决定成功率、奖励和实验指标的评测逻辑仍按核心实现处理。写法示例见 [references/style-patterns.md](./references/style-patterns.md)。

只修改注释和必要文档，保留原有程序行为。

## 参考的开源 skill

本次重写参考了 GitHub 社区仓库 [github/awesome-copilot](https://github.com/github/awesome-copilot) 中的两个 skill。这里说明设计思路的来源和取舍；本项目的具体指令、中文示例及仓库级覆盖要求按自身需求编写。

| 参考 skill | 借鉴内容 | 未采用的内容 |
| --- | --- | --- |
| [add-educational-comments](https://github.com/github/awesome-copilot/blob/main/skills/add-educational-comments/SKILL.md) | 将源码作为学习材料；区分一般编程基础与具体语言、框架知识；根据读者基础调整解释深度 | 每处固定注释条数、统一编号、字符范围限制；本项目另按用户偏好采用核心块总长度至少 125% 的下限 |
| [comment-code-generate-a-tutorial](https://github.com/github/awesome-copilot/blob/main/skills/comment-code-generate-a-tutorial/SKILL.md) | 用直白语言解释代码做什么、为什么重要；结合源码注释组织讲解文档 | 自动重构、修改变量名、仅面向单个 Python 脚本的任务范围 |

