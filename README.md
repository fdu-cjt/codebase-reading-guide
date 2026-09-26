# codebase-reading-guide

为希望学习项目实现的读者编写代码仓库导读，并直接在核心源码旁添加易懂、充分的教学注释。完整执行要求见 [SKILL.md](./SKILL.md)。

默认读者懂基本编程，但正在学习项目涉及的算法和框架。默认使用中文，保留代码标识符；用户指定语言或只需要导读、注释中的一项时，遵守用户要求。

## 提供什么

- **代码导读：** 代码树、必要概念、数据流全景图和阅读顺序。
- **教学注释：** 在核心函数内部解释关键变量、计算步骤、分支原因和结果用途。
- **覆盖检查：** 从入口追到实际计算，对照核心过程和函数清单检查遗漏。

核心代码需要充分讲解，复杂的几行计算可以配多行注释，不设固定注释比例或篇幅上限。普通单元测试、mock、测试初始化、简单日志和样板代码默认不展开。决定成功率、奖励和实验指标的评测逻辑仍按核心实现处理。

只修改注释和必要文档，保留原有程序行为。

## 参考的开源 skill

本次重写参考了 GitHub 社区仓库 [github/awesome-copilot](https://github.com/github/awesome-copilot) 中的两个 skill。这里说明设计思路的来源和取舍；本项目的具体指令、中文示例及仓库级覆盖要求按自身需求编写。

| 参考 skill | 借鉴内容 | 未采用的内容 |
| --- | --- | --- |
| [add-educational-comments](https://github.com/github/awesome-copilot/blob/main/skills/add-educational-comments/SKILL.md) | 将源码作为学习材料；区分一般编程基础与具体语言、框架知识；根据读者基础调整解释深度 | 固定注释行数与比例、统一编号、字符范围限制 |
| [comment-code-generate-a-tutorial](https://github.com/github/awesome-copilot/blob/main/skills/comment-code-generate-a-tutorial/SKILL.md) | 用直白语言解释代码做什么、为什么重要；结合源码注释组织讲解文档 | 自动重构、修改变量名、仅面向单个 Python 脚本的任务范围 |

