# Tools SIG 章程

本章程遵循 TiKV Community 章程和制度，使用 [SIG Governance](/GOVERNANCE-zh_CN.md) 中的角色定义以及职责。

## 职责范围

Tools SIG 聚焦 TiKV 项目的周边工具，例如快速备份恢复工具 [BR](https://github.com/pingcap/br/), 数据同步工具 [CDC](https://github.com/pingcap/ticdc) 等。本 SIG 的主要职责是对这些模块进行未来发展的讨论、规划、开发和维护。仅 Active Contributor 或更高等级社区成员可成为 SIG 成员并参与到相应事项中来，但 SIG 各项实行的决策和进行的项目将公开。

## 工作内容

- 代码范围
  - [BR](https://github.com/pingcap/br): TiKV 快速备份恢复工具;
    - [components/backup](https://github.com/tikv/tikv/tree/master/components/backup): TiKV 备份数据模块;
    - [components/sst_importer](https://github.com/tikv/tikv/tree/master/components/sst_importer): TiKV 恢复数据模块;
    - [components/external_storage](https://github.com/tikv/tikv/tree/master/components/external_storage): TiKV 备份恢复数据存储模块;
  - [CDC](https://github.com/pingcap/ticdc): TiKV 同步数据工具;
    - [components/cdc](https://github.com/tikv/tikv/tree/master/components/cdc): TiKV 同步数据模块;

- 测试规范
  - 代码需要通过已有集成测试，并对新的更改需要添加新的集成测试。

- 设计与演进 Proposal
- Review 相关项目代码

## 其他规章流程

- 代码风格、提交规范、PR Description 模板等请参考 [文档](https://github.com/tikv/tikv/blob/master/CONTRIBUTING.md)
- 任务分配
  - SIG Tech Lead 在 https://github.com/tikv/community 维护公开的 [成员列表](./membership.md) 与 [任务列表](./workflow-zh_CN.md) 链接。
  - 新加入的 SIG 成员可有 2 周时间了解各个任务详情并认领一个任务，或参与一个现有任务的开发或推动。若未能在该时间内认领任务则会被移除 SIG。
  - SIG 成员需维持每个月参与开发任务，或参与关于现有功能或未来规划的设计与讨论。若连续一个季度不参与开发与讨论，视为不活跃状态，将会被移除 SIG。作为 acknowledgment，仍会处于成员列表的「Former Member」中。

- 定期同步进度，定期周会
  - 暂无定期会议。
  - Slack (English): [#sig-tools](https://tidbcommunity.slack.com/messages/sig-tools)
  - Slack (中文): [#sig-tools-zh](https://tidbcommunity.slack.com/messages/sig-tools-zh)

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
      - Merge 以上 repo PR 总数超过 10 个
      - Merge 以上 repo PR 总行数超过 1000 行
      - 已完成一项难度为 Medium 或以上的任务
      - 提出设计想法并得到采纳成为可执行任务超过 3 个

  - Tech Leader 和 TiKV Maintainer 以季度为单位对小组成员进行考核，决定成员是否可由 Reviewer 晋升为 Committer：
    - 表现出良好的技术判断力
    - 获得至少 2 位 TiKV Maintainer 的提名
    - 至少完成两项难度为 Medium 的任务，或一项难度为 High 的任务
    - PR 贡献满足以下至少两点：
      - 半年内 Merge 以上 repo PR 总行数超过 1500 行
      - 有效 Review 以上 repo PR 总数超过 10 个
      - 有效 Review 以上 repo PR 总行数超过 1000 行

- 晋级角色权益 & 义务
  - Reviewer
    - 参与项目设计决策
    - 参与 以上 repo PR Review 与质量控制
    - 对 以上 repo 模块 PR 具有有效的 Approve / Request Change 权限

  - Committer
    - 拥有 Reviewer 具有的权益与义务
    - 整体把控项目的代码质量
    - 指导 Contributor 与 Reviewer

- 退出制度
  - SIG 成员在以下情况中会被移除 SIG，但保留相应的 Active Contributor / Reviewer / Committer 身份：
    - 作为新成员未在指定时间内认领任务
    - 连续一个季度处于不活跃状态

  - Reviewer 满足以下条件之一会被取消 Reviewer 身份且收回权限（后续重新考核后可恢复）：
    - 超过一个季度没有 review 任何以上 repo 相关的 PR
    - 有 2 位以上 Committer 认为 Reviewer 能力不足或活跃度不足
