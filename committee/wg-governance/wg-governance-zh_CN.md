# TiKV Working Group 治理规范

## Working Group 是什么？

Working Group 提供一个群组，来让社区的贡献者可以针对某个问题进行一段时间的合作。因为 Working Group 通常是解决一个跨越多个 Special Interest Group（SIG）职责范围的问题，所以它通常会由来自不同 SIG 的成员或者一些其他社区贡献者组成。Working Group 通常会在问题被解决之后解散，在 Working Group 中创建的成果，或者成员，可以后续被 SIG 接收。更详细的创建或者解散程序，可以参见 [WG Lifecycle](#wg-lifecycle)

Working Group 具有以下特征：

* 不拥有对代码的所有权
* 有明确的可以衡量的目标，以及可以被交付的结果
* 是一个短期的组织，并且会在目标或者使命被完成以后被解散

## Working Group 与 Special Interest Group 的关系

被 TiKV Project 拥有的资产（例如：代码，文档，博客，规章制度等等）由 SIGs 拥有和管理。除非被 Working Group 所拥有的特殊资产，例如：

* 日历事件
* Slack 频道
* 事项进展报告

Working Group 与 SIGs 不同，但是 WG 旨在：

* 促进不同 SIG 之间的协作
* 用最小的组织，促进某些特定的问题，或者解决方案的落地实现。

Working Group 的页面上需要在 `Stakeholder SIGs` 一节中将跟本 Working Group 相关的 SIG 列出来。

## WG Lifecycle

### 创建

* 确定 WG 的组织者以及成员，确保成员都是 TiKV 的 Contributor。
* 按照 [Working Group 页面模板](working-group-template.md) 在 [wg 目录](/wg) 创建一个 `xyz-wg` 的目录（将 xyz 修改为你的 WG 名称），并且将修改好的 Working Group 页面模板作为 `README.md` 页面
* 在 [tikv/community](https://github.com/tikv/community) 提交一个 Pull Request，由 Maintainer/PMC 投票决定。再 Pull Request 被合并之后，宣布 Working Group 成立。
* [Slack: tikv-wg.slack.com](tikv-wg.slack.com) 中创建对应 Working Group 的 channel。

### 解散

* 完成使命之后， Working Group 就可以由 Tech Lead 决定解散。
* 如果 Working Group 的工作进入了停滞，那么也可以由 PMC 投票决定解散 Working Group。