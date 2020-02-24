# Raft SIG 工作流

## 任务

Raft SIG 任务以 issue 的形式组织，任务都关联到 [Raft SIG](https://github.com/tikv/tikv/issues?q=is%3Aissue+is%3Aopen+label%3A%22C%3A+Raft+SIG%22) Label 中，并且会加上相应的难度 Label，这些难度划分为：

- L = Low 低难度，只需要了解 Raft 一小部分知识并使用较少代码量完成
- M = Medium 中难度，需要了解 Raft 多种知识或需要显著代码量完成
- H = High 高难度，需要完全了解 Raft 或需要非常多代码量完成
- S = Super High 超高难度，需要结合 TiKV 其他部分甚至 TiDB、系统编程等综合性知识完成

Raft SIG Tech Lead 负责维护任务列表和任务分配。每个 issue 如果有 assignee，assignee 需要负责该任务的任务分配和推进。

## 提案

Raft SIG 中任何成员均可创建 TiKV issue 并添加 Raft SIG Label，并于 SIG 中讨论。
视情况 issue 中可以附上相应的设计文档、验证代码或参考资料。Raft SIG Tech Lead 负责 review 新的 issue。当 Tech Lead 加上难度 Label 以后，这个提案就成为 Raft SIG 的正式任务。

## 设计与实现

所有代码必须包含必要的单元测试。

对于中难度及以上任务，开始代码实现之前须在 issue 中简略描述实现的方式，并在 SIG 中做适当的讨论。

高难度及以上任务须遵守以下工作流程：

* 提供设计文档。文档经过 Tech Lead 或者 SIG 中其他相关成员 review。
* 对于性能提升类任务，实现前需提供原型验证代码和简单 benchmark 验证结果，实现后提供完整 benchmark 结果。
* 对于编码量大的任务，需要拆分并创建子任务，分步完成。建议每个 PR 不超过 500 行代码，重构类代码每个 PR 不超过 1000 行。
