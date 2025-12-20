---
layout: post
title: Something about Palantir AIP & Foundry
---


**纸上谈兵之 Palantir AIP & Foundry**


虽然最近几乎都在写“营销类”技术文档；但是无意之中看到了``Palantir`` AIP & Foundry 产品发布会；没想到竟有如此之渊源；只好写下；


**AIP**

首先，产品发布会 -> ``Marketing`` AND ``Best Case``；

与 AGI 类似，``Anthropic CEO 达里奥・阿莫迪（Dario Amodei）明确称 AGI 是 “营销术语（marketing term）”。``，演讲稿即营销术语，如下图：

<div style="text-align: center;">
    <img src="{{ site.baseurl }}/images/posts/2025-12-20-Something-about-Palantir-AIP-%26-Foundry/Palantir-AIP-Terminal.jpg" alt="Palantir AIP Terminal" style="width: 400px;"/>
</div>

不过，关于 ``Human Agent Teaming`` ，同样是供应链，项目重名 ``Control Tower``；客户想法已经不是巧合了。

``Human Agent Teaming`` AND BPR(Business Process Reengineering)： 进行时。

<img src="{{ site.baseurl }}/images/_posts/2025-12-20-Something-about-Palantir-AIP-&-Foundry/Palantir-AIP-Human-Agent-Teaming.jpg" alt="Palantir AIP Human Agent Teaming"/>

那么，What is AIP? ``Palantir AIP(Artificial Intelligence Platform) 旨在将大语言模型带入企业，驱动运营流程自动化。``

目前，我认为 AIP 约等于 ``Foundry`` + ``LLM functions``；

“产品演示”主要是 自然语言指令 + 自定义函数 + 可视化应用流水线 + 用例目录 + 可观测性 + AI co-pilot，如下图；

“机器学习模型”即用例目录；自然语言新建仪表盘而非应用程序；``webhook``系统集成；自定义函数读取供应链邮件并从中提取出地点信息&工具调用：查询配送中心本体库的能力；AI co-pilot: Leo；

``trust``，``that trust is a core part of the concepts around human-agent teaming here.``，信任；可观测性 与 可解释性（比如：AI深度思考推理过程）；

    <img src="{{ site.baseurl }}/images/_posts/2025-12-20-Something-about-Palantir-AIP-&-Foundry/Palantir-AIP-applications.jpg" alt="Palantir AIP applications"/>

虽然“产品演示”眼花缭乱，但其与 ``Dify`` 没有本质区别。

令人印象深刻是，``Palantir`` 在 UI 煞费苦心；AI 工作流在调试、生产、应用等UI各有侧重，同时也都强调可观测性&可解释性；

此外，``data integration``；数据集成应该是其“起点”；不过这似乎属于 ``Foundry``。

    <img src="{{ site.baseurl }}/images/_posts/2025-12-20-Something-about-Palantir-AIP-&-Foundry/Palantir-AIP-data-integration.jpg" alt="Palantir AIP data integration"/>


**Foundry**

首先，AIP 基于 Foundry。

```
Palantir AIP 的数据和权限接入直接基于 Foundry 的本体（Ontology）和数据治理体系工作，所有模型调用都受统一权限和审计约束。AIP 可与 Foundry 中企业现有的数据无缝集成，能利用来自各种数据源和格式的数据，构建由大语言模型驱动的智能体和工作流。此外，AIP 的功能也已嵌入 Foundry 的核心应用程序中，以帮助用户加速工作流程。
```

那么，Foundry 与 Tableau、PowerBI、Dataphin & QuickBI && 小Q 有何差异？

似乎均具备低代码 / 无代码的数据工作流编排能力。

参考 Foundry 本体与仿真引擎 发布会；由于时间关系，使用豆包总结视频，重点如下：

```
指出企业数据管理痛点及 Foundry 的解决方案01:47：企业数据量持续增长产生海量熵值，单一供应链项目需处理大量数据表并整合多系统数据，即便数据集中也难理解，导致数据项目无明确业务成果；Foundry 的本体与仿真引擎技术保留细粒度数据治理与安全，将所有数据映射到组织专属、易懂的统一框架（本体，即组织数字孪生），为下游流程提供统一接口，也是数字资产与现实运营的双向接口。

介绍 Foundry 的模型管理与仿真引擎08:40：操作人员依赖模型预判决策影响，Foundry 本体通过映射模型连接组织，创建全系统模拟引擎，支持组织各层级用户在执行决策前理解潜在结果及副作用，构建预部署和测试运营的基础设施；所有模型在统一框架管理，关联业务目标，可查看模型活跃部署数量、健康状态及输入输出与现实实体的映射，还能监控模型性能、管理变化与部署，仿真引擎可使模型相互关联，支持复杂价值链遍历和场景模拟。

阐述 Foundry 未来发展方向22:25：一是通过案例库和模块化部署选项触达更多用户群体；二是赋能机构所有关键决策，让每位需要的用户使用 Foundry，通过新移动服务和跨组织协作功能解决疫情、气候变化等难题；三是创新 AI 在运营中的应用，利用模拟理解行动在复杂系统中的预期与意外后果。
```

结论：

Foundry 通过数据集成（SDDI）与映射工作构建统一框架 Ontology；本体；并在此基础上支持跨部门、跨职能协作 以及 提供仿真引擎与决策支持。

其未来发展方向主要是 1. use case catalog(it's much deeper than just some nice-looking applications templates.) 2. 聚焦仿真与决策。

个人理解：

Foundry 需要通过更多的行业案例来扩充模板库；其“产品演示”一直是 supply chain control tower；关于“仿真与决策”，也没有看到更深入的实践与效果。

关于 Ontology；1. 到底是什么？是否有效？为什么？； 2. 不论如何，“本体理论”至少看起来有“说服力”；之前在此类问题就没有理论化；


**其他**

- AI工具视频总结
  - 先找到 bibigpt（B站总结视频AI工具）；但应该要付费；本来在想要不要自己写一个；AV2BV等等；后来发现“豆包总结视频”；哎，通用型标准化AI工具是个人开发者&独立站的末路；
- 拼字幕；拼台词；截图拼接；


**References:**
1. [Palantir CTO Shyam在AIPCon上发布AIP](https://www.bilibili.com/video/BV1rHkyBNEo1)
2. [Palantir Foundry发布会实录](https://www.bilibili.com/video/BV1fxU4BFESU)
3. [怎么把视频中的字幕，图拼接到一张图片中?求解答！?](https://www.zhihu.com/question/357518290)
4. [截图拼接工具](https://join-screenshots.zhanghai.me/)
5. [bibigpt](https://github.com/JimmyLv/BibiGPT-v1)


