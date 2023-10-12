# PineCone的LangChain手册

## 第一章 LangChain介绍

大语言模型（LLM）随着2020年OpenAI GPT-3的发布进入世界舞台。从那之后，他们的人气稳步提升。

直到2022年底。之后对LLM和更广泛的生成式AI的兴趣激增，原因可能是LLM不断取得重大进展。

我们看到了谷歌有知觉的LaMDA对话机器人。第一个高性能和开源的LLM（BLOOM）发布了。OpenAI发布了他们下一代文本嵌入模型和GPT-3.5的后续模型。

在这么多LLM领域的巨大飞跃之后，OpenAI发布了ChatGPT，将LLM推到聚光灯之下。

LangChain在差不多同一时间出现。它的创建者，Harrison Chase，在2022年10月底做了第一次提交。

虽然现在这个库还处于其早期阶段，但它已经封装了用于构建基于LLM核心的不可思议的特性。本文中我们将介绍这个库，让我们从LangChain提供的最直观的组件，LLM，开始。

### LangChain

在其内核，LangChain是围绕LLM构建的框架。我们可将其用于对话机器人，生成式问答，总结和更多用途。

这个库最核心的思想是，我们可以“链接(chain)”不同组件，用以创建围绕LLM的更加高级的应用。Chain由来此多个模块的多个组件组成：

* 提示语模板(PromptTemplate)：不同类型提示语的模板，如聊天机器人型模板，ELI5问答模板等
* 大语言模型(LLM)：如GPT-3, BLOOM等
* 代理（Agent）：代理使用LLM决定采用什么动作（Action）。可以使用如web搜索或计算器这样的工具（Tool），所有这些打包到一个操作的逻辑循环中。
* 记忆（Memory）：短期记忆，长期记忆等。

#### 1. 第一个提示语模板
现在，我们从提示语模板和大语言模型的基础开始。我们将探索两个大语言模型选项：Hugging Face Hub的模型和OpenAI的模型。

输入大模型的提示语经常结构化为不同方式，用以获取不同结果。对于问答类型，我们拿到用户的输入，重新格式化为不同问答风格，如通常的问答，列表式问答，甚或对给定问题的答案的总结。

从一个简单的问答式提示语模板开始。先安装langchain库：

```sh
pip install langchain
```

然后导入PromptTemplate类：

```python
from langchain import PromptTemplate

template = """Question: {question}

Answer: """

prompt = PromptTemplate(template=template, input_variables=['question'])

question = "Which NFL team won the Super Bowl in the 2010 season?"

```

应用这个模板后，得到如下问题：

```
Question: Which NFL team won the Super Bowl in the 2010 season?
Answer:
```

#### 2. HuggingFaceHub大语言模型



## 第二章 提示语工程

## 第三章 对话机器人的记忆

## 第四章 使用本地知识库

## 第五章 使用对话代理加强LLM

## 第六章 为LLM代理构建工具

