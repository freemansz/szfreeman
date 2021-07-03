<img src="https://gitee.com/ubml/ubml-standard/raw/master/res/images/ubml_logo.png" height="100" width="426">

# UBML: Unified Business Modeling Language(统一业务建模语言)

[![Build Status](https://ubml.openatom.org/ci/job/ubml-imp/badge/icon)](https://ubml.openatom.org/ci/job/ubml-imp/) [![license](https://img.shields.io/github/license/seata/seata.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

## 简介

UBML是一种基于领域特定语言（Domain-Specific Language DSL）的、用于**快速构建**应用软件的**低代码建模语言**。内容包括模型标准及其默认实现、SDK、运行时框架等组件。UBML定位于APaaS
（应用程序平台即服务）领域，是低代码开发平台（Low-Code-Development-Platform）的**核心基础**，致力于在低代码领域建立应用软件建模开发的事实标准

### 架构图

UBML架构图如下

<img src="https://gitee.com/ubml/ubml-standard/raw/master/res/images/ubml_architecture.jpg"  height="378" width="755">

### 特性
- 微内核可扩展的开放架构：模型标准与实现解耦，模型种类可以**按行业类型/应用类型持续扩展**
- 开发语言无关性：通过建模，可适配**多种技术栈实现**
- 全栈模型刻画能力：建模范围可涵盖UI、API、流程、领域服务、持久化等**全栈开发**的各个层级
- 支持Hybrid模式：开发模式上，提供**模型生成代码**与**模型动态解析**两种开发技术
- 模型工程化：视模型为源码，提供模型**生命周期管理**与**工程化管理**能力，可与主流研发工具融合，支持DevOps

### 价值
- 显著提升软件开发效率
- 最大程度减少人工编码的不规范性与出错率，促进软件开发标准化
- 降低开发门槛，促进软件开发平民化
- 丰富工业应用软件生态，赋能企业数字化创新转型

### 核心设计策略

有关UBML当前及后续的设计策略，详见 [设计策略](https://gitee.com/ubml/ubml-standard/blob/master/docs/design/design_strategy.md)。


### 历史

##### GSP
2004-2019，浪潮上一代低代码开发平台GSP采用了模型驱动的低代码开发技术，其内置的模型体系是UBML的前身
##### iGIX
2019年，浪潮基于云原生、前后端分离、领域驱动设计、跨平台等架构与设计理念，形成UBML低代码建模体系，并应用于浪潮新一代企业数字化能力平台iGIX
#### UBML
2020年，浪潮将UBML低代码建模体系从iGIX剥离，启动开源进程，旨在将UBML打造成低代码领域的标准

## 如何使用

### 快速入门
有关UBML的快速入门教程，详见 [快速入门](https://gitee.com/ubml/ubml-standard/blob/master/docs/design/overview.md)

### 新建Issue

请按照 [Issue模板](./.gitee/ISSUE_TEMPLATE/BUG_REPORT.md) 反馈您遇到的任何问题.

## 贡献
欢迎贡献者加入UBML项目！关于如何为UBML做出贡献，请参阅 [如何参与贡献](./CONTRIBUTING.md)。

## 许可证

UBML采用的开源许可证是Apache License 2.0，有关协议细节，请参阅 [LICENSE](./LICENSE) 
