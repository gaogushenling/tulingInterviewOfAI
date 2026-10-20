# AI大模型直播课













# <font style="color:rgb(6, 6, 7);"> AI元年逆袭之路，           		RAGflow构建本地知识库</font>
### <font style="color:rgb(6, 6, 7);">引言 Manus智能体刷屏</font>
#### <font style="color:rgb(6, 6, 7);">AI元年，万物即可A</font>
<font style="color:rgb(6, 6, 7);">随着人工智能技术的飞速发展，我们正处在一个被称为“AI元年”的时代。在这个时期，AI技术不仅在理论上取得了突破，更在实际应用中展现出了巨大的潜力和价值。本文将探讨AI赛道的多个方面，包括AI智能体、模型私有定制化、搜广推等，并深入解析RAG技术、Embedding模型以及如何快速搭建本地知识库等关键技术。</font>

<font style="color:rgb(6, 6, 7);">简单来说 </font><font style="color:rgba(0, 0, 0, 0.87);">AI的大模型正在迅速改变我们的生活方式，万物皆可加入AI，市场缺口巨大。</font>

![1741071227514-e2641889-d39c-4249-92c2-b8c5b4b4dd55.png](./img/PV3hRSe0xhwIaUen/1741071227514-e2641889-d39c-4249-92c2-b8c5b4b4dd55-543198.png)

四大核心能力：

![1741071407774-17063c1b-a75f-4c82-998d-5460be75bce9.png](./img/PV3hRSe0xhwIaUen/1741071407774-17063c1b-a75f-4c82-998d-5460be75bce9-276887.png)

#### 为什么不直接使用网页版ds？
<font style="color:rgba(0, 0, 0, 0.87);">网页版的大模型不说</font>**<font style="color:rgba(0, 0, 0, 0.87);">响应</font>**<font style="color:rgba(0, 0, 0, 0.87);">速度，和</font>**<font style="color:rgba(0, 0, 0, 0.87);">精准</font>**<font style="color:rgba(0, 0, 0, 0.87);">度。主要基于现有的外部数据集进行训练，但缺乏完整的知识库。这种结构化不足会导致模型在实际场景中的表现下降。而且特定领域由于</font>**<font style="color:rgba(0, 0, 0, 0.87);">数据安全性</font>**<font style="color:rgba(0, 0, 0, 0.87);">，不能选择外部模型。</font>

[Deepseek Chat](https://chat.deepseek.com/)

#### 如何实现网页版ds不能实现的需求？
**<font style="color:rgba(0, 0, 0, 0.87);">本地化</font>**<font style="color:rgba(0, 0, 0, 0.87);">部署，通过</font>**<font style="color:rgba(0, 0, 0, 0.87);">RAG</font>**<font style="color:rgba(0, 0, 0, 0.87);">（Retrieval-Augmented Generation）结合文本检索和生成任务，弥补了这一短板。它能够根据上下文信息查找相关的知识，并将其整合到模型的回答中，显著提升了模型的泛化能力。</font>

[Ollama Down](https://ollama.com/) 然后小黑窗口run ，可配合chatbox客户端使用，也可配置[硅基流动](https://siliconflow.cn/zh-cn/models)满血版

#### AI赛道，如何把握机会？
##### AI 智能体
<font style="color:rgb(6, 6, 7);">AI智能体是指能够自主执行任务、做出决策并从环境中学习的系统。它们可以应用于客户服务、游戏、自动化控制等多个领域。</font>

![1740727993085-cb36be9a-8823-4444-a5b4-632fdd546cbf.png](./img/PV3hRSe0xhwIaUen/1740727993085-cb36be9a-8823-4444-a5b4-632fdd546cbf-632343.png)

##### 模型私有定制化
<font style="color:rgb(6, 6, 7);">模型私有定制化是指根据特定需求和数据集对预训练模型进行调整，以适应特定的业务场景。</font>

![1740727845138-31f8572d-c0ba-421b-ae67-4ac4f61c01f2.png](./img/PV3hRSe0xhwIaUen/1740727845138-31f8572d-c0ba-421b-ae67-4ac4f61c01f2-470030.png)

##### 搜广推
<font style="color:rgb(6, 6, 7);">即搜索、广告和推荐系统，利用AI技术提高内容的个性化和相关性，提升用户体验和商业价值。</font>



### 什么是RAG？为什么需要？原理是？
#### RAG原理
<font style="color:rgb(6, 6, 7);">RAG（Retrieval-Augmented Generation）是一种结合了检索（Retrieval）和生成（Generation）的模型架构。它首先从大规模数据集中检索相关信息，然后将这些信息作为上下文输入到生成模型中，以生成更加准确和相关的输出。</font>

![1740734563689-93d0eb34-4f28-4de6-89b3-659e4c19635e.png](./img/PV3hRSe0xhwIaUen/1740734563689-93d0eb34-4f28-4de6-89b3-659e4c19635e-494882.png)

<font style="color:rgb(6, 6, 7);">RAG技术的原理是通过检索增强生成模型的能力，使其能够利用外部知识库来生成更加丰富和准确的内容。</font>

#### <font style="color:rgba(0, 0, 0, 0.87);">技术细节：检索，增强，生成</font>
##### <font style="color:rgba(0, 0, 0, 0.87);">检索策略：</font>
    - **<font style="color:rgba(0, 0, 0, 0.87);">词袋模型</font>**<font style="color:rgba(0, 0, 0, 0.87);">：将单词和短语作为实体，存储为向量形式。</font>
    - **<font style="color:rgba(0, 0, 0, 0.87);">嵌入表（Embedding）</font>**<font style="color:rgba(0, 0, 0, 0.87);">：将单词映射到低维空间，便于检索。例如，在Word2Vec模型中，每个单词被映射到一个向量。</font>

##### <font style="color:rgba(0, 0, 0, 0.87);">生成过程：</font>
    - <font style="color:rgba(0, 0, 0, 0.87);">在生成文本时，结合检索结果获取相关信息，并将其融入生成的文本中。</font>
    - <font style="color:rgba(0, 0, 0, 0.87);">通过监督学习（Supervised Learning），在生成过程和外部知识库之间建立关联。例如，在问答系统中，生成器的目标是尽可能接近用户提供的查询。</font>

##### <font style="color:rgba(0, 0, 0, 0.87);">增强机制：</font>
    - <font style="color:rgba(0, 0, 0, 0.87);">在生成过程中，使用检索结果来调整生成参数或直接提取相关信息。这可以通过损失函数（Loss Function）来实现，使生成文本与目标数据集更相似。</font>

### RAG和模型微调的区别？微调流程是？
### <font style="color:rgb(6, 6, 7);">RAG和模型微调的区别</font>
| **<font style="color:rgb(6, 6, 7);">特性</font>** | **<font style="color:rgb(6, 6, 7);">RAG（Retrieval-Augmented Generation）</font>** | **<font style="color:rgb(6, 6, 7);">微调（Fine-tuning）</font>** |
| :--- | :--- | :--- |
| **<font style="color:rgb(6, 6, 7);">原理</font>** | <font style="color:rgb(6, 6, 7);">通过检索外部知识库中的信息，并将其作为上下文输入到生成模型中，增强生成文本的准确性和相关性</font><font style="color:rgb(6, 6, 7);">。</font> | <font style="color:rgb(6, 6, 7);">对预训练模型的参数进行针对性调整，使其适应特定任务或领域</font><font style="color:rgb(6, 6, 7);">。</font> |
| **<font style="color:rgb(6, 6, 7);">数据需求</font>** | <font style="color:rgb(6, 6, 7);">数据需求较少，主要依赖外部知识库</font><font style="color:rgb(6, 6, 7);">。</font> | <font style="color:rgb(6, 6, 7);">需要大量标注数据进行训练</font><font style="color:rgb(6, 6, 7);">。</font> |
| **<font style="color:rgb(6, 6, 7);">更新成本</font>** | <font style="color:rgb(6, 6, 7);">知识更新成本低，只需更新知识库</font><font style="color:rgb(6, 6, 7);">。</font> | <font style="color:rgb(6, 6, 7);">更新困难，需要重新微调模型</font><font style="color:rgb(6, 6, 7);">。</font> |
| **<font style="color:rgb(6, 6, 7);">推理速度</font>** | <font style="color:rgb(6, 6, 7);">推理速度较慢，需要检索和生成两个步骤</font><font style="color:rgb(6, 6, 7);">。</font> | <font style="color:rgb(6, 6, 7);">推理速度快，只需一次模型调用</font><font style="color:rgb(6, 6, 7);">。</font> |
| **<font style="color:rgb(6, 6, 7);">灵活与适应性</font>** | <font style="color:rgb(6, 6, 7);">适应性强，适合动态环境和多样化任务</font><font style="color:rgb(6, 6, 7);">。</font> | <font style="color:rgb(6, 6, 7);">适应性较差，主要适用于特定任务和稳定环境</font><font style="color:rgb(6, 6, 7);">。</font> |
| **<font style="color:rgb(6, 6, 7);">优点</font>** | <font style="color:rgb(6, 6, 7);">动态知识更新、较少的数据需求、灵活性强、可定制化</font><font style="color:rgb(6, 6, 7);">。</font> | <font style="color:rgb(6, 6, 7);">定制化能力强、一体化、高效推理</font><font style="color:rgb(6, 6, 7);">。</font> |
| **<font style="color:rgb(6, 6, 7);">缺点</font>** | <font style="color:rgb(6, 6, 7);">推理速度慢、复杂性增加、依赖外部知识库</font><font style="color:rgb(6, 6, 7);">。</font> | <font style="color:rgb(6, 6, 7);">数据需求高、更新困难、存储和计算成本高</font><font style="color:rgb(6, 6, 7);">。</font> |
| **<font style="color:rgb(6, 6, 7);">适用场景</font>** | <font style="color:rgb(6, 6, 7);">外部知识频繁更新、标注数据不足、任务复杂多样</font><font style="color:rgb(6, 6, 7);">。</font> | <font style="color:rgb(6, 6, 7);">任务和数据相对稳定、有充足标注数据、对推理速度要求高</font><font style="color:rgb(6, 6, 7);">。</font> |




<font style="color:rgb(6, 6, 7);">RAG与模型微调的主要区别在于，RAG侧重于利用外部知识库来增强模型的生成能力，而模型微调则是通过在特定数据集上进一步训练模型来调整其参数。LoRA </font><font style="color:rgba(0, 0, 0, 0.87);">微调是提升大模型性能的关键方法之一。</font>

<font style="color:rgba(0, 0, 0, 0.87);">简单直白的说就是：RAG就是给大模型投喂知识，微调就是训练优化。</font>

####  微调流程：
![1740728034504-8febe42c-6314-4171-b60b-c4235f3688dd.png](./img/PV3hRSe0xhwIaUen/1740728034504-8febe42c-6314-4171-b60b-c4235f3688dd-266129.png)

<font style="color:rgb(6, 6, 7);">微调流程通常包括以下步骤：</font>

1. <font style="color:rgb(6, 6, 7);">准备特定领域的数据集。</font>
2. <font style="color:rgb(6, 6, 7);">选择一个预训练模型。</font>
3. <font style="color:rgb(6, 6, 7);">在特定数据集上进一步训练模型，调整模型参数。</font>
4. <font style="color:rgb(6, 6, 7);">评估模型性能并进行必要的调整。</font>

### 什么是Embedding？为什么需要？
<font style="color:rgb(6, 6, 7);">Embedding（向量）是一种将高维数据转换为低维向量的技术，这些向量能够在一定程度上保留原始数据的语义信息。在自然语言处理等领域，Embedding模型能够将文本转换为向量，从而使得机器学习模型能够更好地理解和处理文本数据。</font>

<font style="color:rgb(6, 6, 7);">简而言之就是让知识库的文件能被机器看懂。可查看</font>[Ollama](https://ollama.com/search?c=embedding)可下的model除了chat模型还有embedding

#### <font style="color:rgba(0, 0, 0, 0.87);">为什么需要Embedding模型？</font>
##### <font style="color:rgba(0, 0, 0, 0.87);">高维表示：</font>
    - <font style="color:rgba(0, 0, 0, 0.87);">传统的方法如TF-IDF（ TF-Inverse Document Frequency）直接使用词的频率作为特征值，这些特征值通常非常稀疏和低维。这种表示方式在处理文本数据时可能会出现维度过载的问题。</font>

##### <font style="color:rgba(0, 0, 0, 0.87);">捕捉上下文关系：</font>
    - <font style="color:rgba(0, 0, 0, 0.87);">在自然语言处理任务中，模型需要理解一个句子中的每个词与其他词之间的关系。使用嵌入向量可以更好地捕捉这些关系，因为嵌入向量不仅包含词本身的特征，还包含了其与其他词的相似性或相关性。</font>

##### <font style="color:rgba(0, 0, 0, 0.87);">处理稀疏数据：</font>
    - <font style="color:rgba(0, 0, 0, 0.87);">嵌入向量通常可以处理更密集的数据结构，这使得模型在处理稀疏输入时表现更好。例如，在某些任务中，每个单词的嵌入向量可能都是非零的，并且可以在较高的维度上分布均匀。</font>

##### <font style="color:rgba(0, 0, 0, 0.87);">提高模型性能：</font>
    - <font style="color:rgba(0, 0, 0, 0.87);">传统的词袋模型和TF-IDF等方法在某些情况下效果不佳，因为它们忽略了一些重要的上下文信息。使用嵌入向量可以让模型更好地利用这些信息，从而提升整体模型的性能。</font>

##### <font style="color:rgba(0, 0, 0, 0.87);">与深度学习结合的效果：</font>
    - <font style="color:rgba(0, 0, 0, 0.87);">嵌入向量可以有效地整合到深度学习模型中。例如，在LSTM（长短期记忆网络）或CNN（卷积神经网络）中使用嵌入向量可以让模型更好地理解文本序列中的上下文关系，从而提高模型的预测能力。</font>

##### <font style="color:rgba(0, 0, 0, 0.87);">处理变长输入：</font>
    - <font style="color:rgba(0, 0, 0, 0.87);">传统的词袋模型和TF-IDF等方法对输入的词数量非常敏感。如果一个句子很长或者很短，可能会导致特征空间变得过大或过小，影响模型的学习效果。</font>

### 如何快速搭建本地知识库？实操！
<font style="color:rgb(6, 6, 7);">快速搭建本地知识库的步骤包括：</font>

1. <font style="color:rgb(6, 6, 7);">本地部署AI大模型。</font>
2. <font style="color:rgb(6, 6, 7);">收集和整理知识库相关数据。</font>
3. <font style="color:rgb(6, 6, 7);">选择合适的存储和检索技术。</font>
4. <font style="color:rgb(6, 6, 7);">实施数据的索引和检索机制。</font>

#### 实操：
##### 1，本地部署大模型 ollama下载安装DeepSeek
打开 [https://ollama.com/download](https://ollama.com/download)  下exe 安装

命令行：ollama run deepseek-r1:1.5b  部署ds模型

![1741157667822-9efbba3f-d848-4047-86e1-c5f1b41e3fc7.png](./img/PV3hRSe0xhwIaUen/1741157667822-9efbba3f-d848-4047-86e1-c5f1b41e3fc7-308278.png)

告别小黑窗 下载chatbox：https://chatboxai.app

设置：![1741157856479-868f9352-3a6b-45e0-a68f-4b44f0f33976.png](./img/PV3hRSe0xhwIaUen/1741157856479-868f9352-3a6b-45e0-a68f-4b44f0f33976-484842.png)

##### 2，RAG开源架构 RAGFlow镜像启动
下载RAGFlow  git ：

$ git clone [https://github.com/infiniflow/ragflow.git](https://github.com/infiniflow/ragflow.git)

修改配置（默认不带Embedding模块）本地部署Embedding

![1741158226657-8ac4b8d7-72c8-47f3-b66d-26938ff43ea8.png](./img/PV3hRSe0xhwIaUen/1741158226657-8ac4b8d7-72c8-47f3-b66d-26938ff43ea8-965268.png)

然后下载docker镜像 执行下面这个命令：

docker compose -f docker-compose.yml up -d

![1741153053321-348845e2-3cb6-4244-890c-77f7146709f6.png](./img/PV3hRSe0xhwIaUen/1741153053321-348845e2-3cb6-4244-890c-77f7146709f6-755963.png)

##### 3，配置 LLM：chat模型 和 embedding模型
（注意名称,ipconfig  IP地址不能127.0.0.1）

![1741074676677-53e0d66b-4e25-4b92-a19c-431f93a02b05.png](./img/PV3hRSe0xhwIaUen/1741074676677-53e0d66b-4e25-4b92-a19c-431f93a02b05-775640.png)![1741074586386-3d86b0bb-a4c9-49c9-9b33-d05721e65121.png](./img/PV3hRSe0xhwIaUen/1741074586386-3d86b0bb-a4c9-49c9-9b33-d05721e65121-830199.png)

##### 4，构建个人知识库：
让大模型先写一份员工规范 / 蟹堡王员工规范 上传并解析

##### 5，[RAGFlow ](http://localhost/)导入与否 问答测试的效果 对比 
（员工基本原则？怎么接待一车的沙丁鱼）

调整：设置助理，提示引擎： 不知道的答复。 模型设置token大些避免回答较短







##### 不本地部署，可以只搭建个人知识库吗？
如**DS网页版**也可上传文档，但不能形成知识库。**<font style="color:rgb(6, 6, 7);">Langchain</font>**<font style="color:rgb(6, 6, 7);">适合技术用户快速搭建知识库，也</font>可选择谷歌**浏览器插件**：<font style="color:rgb(31, 31, 31);">Page Assist - 本地 AI 模型</font>

### AI大模型学习规划，落地项目，简历优化
AI大模型学习规划

![1741151467229-67e5d2a2-539e-4539-b846-c8caa1900cd8.png](./img/PV3hRSe0xhwIaUen/1741151467229-67e5d2a2-539e-4539-b846-c8caa1900cd8-584517.png)

聊天机器人，根据信息执行相关业务操作：比如收发邮件，购票，退换票



### AI大模型就业形式，和大厂案例


+ <font style="color:rgb(6, 6, 7);">Google：利用AI技术改进搜索引擎，提高广告投放的精准度。</font>
+ <font style="color:rgb(6, 6, 7);">Amazon：通过AI技术优化物流和供应链管理，提高效率。</font>
+ <font style="color:rgb(6, 6, 7);">飞书，钉钉，腾讯等大厂皆已适配自己的ds，官网给出近百款</font>[集成案例](https://github.com/deepseek-ai/awesome-deepseek-integration/tree/main)

![1741153710143-bd4a695e-4ef8-4eac-8daa-0033a19bd5a7.png](./img/PV3hRSe0xhwIaUen/1741153710143-bd4a695e-4ef8-4eac-8daa-0033a19bd5a7-692154.png)

![1741153956275-a4213b9b-83be-4881-8e3c-d7b3968f6db7.png](./img/PV3hRSe0xhwIaUen/1741153956275-a4213b9b-83be-4881-8e3c-d7b3968f6db7-648038.png)

![1741153962613-774d15f6-7513-4a04-9edb-accb26c16cf4.png](./img/PV3hRSe0xhwIaUen/1741153962613-774d15f6-7513-4a04-9edb-accb26c16cf4-031470.png)









> 更新: 2025-04-20 22:38:49  
> 原文: <https://www.yuque.com/aaron-wecc3/dhluml/asgpo5yesx0uioag>