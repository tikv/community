# Coprocessor SIG 章程

本章程遵循 TiKV Community 章程和制度，使用 [SIG Governance](/GOVERNANCE-zh_CN.md) 中的角色定义以及职责。

## 职责范围

Coprocessor SIG 聚焦 TiKV 项目 Coprocessor 模块，Coprocessor 是 TiKV 中负责处理 TiDB 的下推计算的模块。本 SIG 的主要职责是对 Coprocessor 模块进行未来发展的讨论、规划、开发和维护。仅 Active Contributor 或更高等级社区成员可成为 SIG 成员并参与到相应事项中来，但 SIG 各项实行的决策和进行的项目将公开。

## 工作内容

- 代码范围
  - Framework: 计算框架改进，包括表达式计算框架、算子执行框架等；
  - Executor: 改进现有算子、与 TiDB 协作研发新算子；
  - Function: 维护现有的 UDF / AggrFn 实现或从  TiDB port 新的 UDF / AggrFn 实现；
  - 代码位置：[tidb_query](https://github.com/tikv/tikv/tree/master/components/tidb_query) 模块。

- 测试规范
  - 代码需要通过已有集成测试，并对新的更改需要在 [copr-test](https://github.com/tikv/copr-test) 中添加新的集成测试；
  - 从 TiDB port 的函数需要同时 port 单元测试，如果 TiDB 的单元测试没有覆盖所有的分支，需要补全单元测试；
  - Expression 的集成测试需要构造使用这个 Expression 的算子进行测试。

- 设计与演进 Proposal
- Review 相关项目代码

## 其他规章流程

- 代码风格、提交规范、PR Description 模板等请参考 [文档](https://github.com/tikv/tikv/blob/master/CONTRIBUTING.md)
- 任务分配
  - SIG Tech Lead 在 https://github.com/tikv/community 维护公开的 [成员列表](https://tikv.github.io/members/build/index.html?name=coprocessor) 与 [任务列表](./workflow-zh_CN.md) 链接。
  - 新加入的 SIG 成员可有 2 周时间了解各个任务详情并认领一个任务，或参与一个现有任务的开发或推动。若未能在该时间内认领任务则会被移除 SIG。
  - SIG 成员需维持每个月参与开发任务，或参与关于现有功能或未来规划的设计与讨论。若连续一个季度不参与开发与讨论，视为不活跃状态，将会被移除 SIG。作为 acknowledgment，仍会处于成员列表的「Former Member」中。

- 定期同步进度，定期周会
  - 每 2 周以文档形式同步一次当前各个项目的开发进度。
  - 每 2 周召开一次全组进度会议，时间依据参会人员可用时间另行协商。目前没有项目正在开发的成员可选择性参加以便了解各个项目进度。若参与开发的成员不能参加，需提前请假且提前将自己的月度进度更新至文档。
  - 每次会议由一名成员进行会议记录，在会议结束 24 小时内完成会议记录并公开。会议记录由小组成员轮流执行。
  - Slack: https://tikv-wg.slack.com #copr-sig-china

- 组织线上线下成员的活动
- Tech Leads 额外承担的职责
  - SIG member 提出的问题需要在 2 个工作日给出回复
  - 及时 Review 代码
  - 定时发布任务（如果 SIG member 退出后，未完成的任务需要重新分配）


## SIG 活跃规则，晋升机制

- 考核 & 晋升制度
  - Tech Leader 以月为单位对小组成员进行考核，决定成员是否可由 Active Contributor 晋升为 Reviewer：
    - 熟悉代码库
    - 获得至少 2 位 TiKV Committer 的提名
    - PR 贡献满足以下任意一点：
      - Merge Coprocessor PR 总数超过 10 个
      - Merge Coprocessor PR 总行数超过 1000 行
      - 已完成一项难度为 Medium 或以上的任务
      - 提出设计想法并得到采纳成为可执行任务超过 3 个

  - Tech Leader 和 TiKV Maintainer 以季度为单位对小组成员进行考核，决定成员是否可由 Reviewer 晋升为 Committer：
    - 表现出良好的技术判断力
    - 获得至少 2 位 TiKV Maintainer 的提名
    - 至少完成两项难度为 Medium 的任务，或一项难度为 High 的任务
    - PR 贡献满足以下至少两点：
      - 半年内 Merge Coprocessor PR 总行数超过 1500 行
      - 有效 Review Coprocessor PR 总数超过 10 个
      - 有效 Review Coprocessor PR 总行数超过 1000 行

- 晋级角色权益 & 义务
  - Reviewer
    - 参与项目设计决策
    - 参与 Coprocessor PR Review 与质量控制
    - 对 Coprocessor 模块 PR 具有有效的 Approve / Request Change 权限

  - Committer
    - 拥有 Reviewer 具有的权益与义务
    - 整体把控项目的代码质量
    - 指导 Contributor 与 Reviewer

- 退出制度
  - SIG 成员在以下情况中会被移除 SIG，但保留相应的 Active Contributor / Reviewer / Committer 身份：
    - 作为新成员未在指定时间内认领任务
    - 连续一个季度处于不活跃状态

  - Reviewer 满足以下条件之一会被取消 Reviewer 身份且收回权限（后续重新考核后可恢复）：
    - 超过一个季度没有 review 任何 Coprocessor 相关的 PR
    - 有 2 位以上 Committer 认为 Reviewer 能力不足或活跃度不足
