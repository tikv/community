# Scheduling SIG 章程

本章程遵循 TiKV Community 章程和制度，使用 [SIG Governance](/GOVERNANCE-zh_CN.md) 中的角色定义以及职责。

## 职责范围

Scheduling SIG 的主要职责是致力于调度系统 [pd](https://github.com/tikv/pd) 的发展，优化调度算法和改进工程实现，并组织社区成员进行相关开发和维护。仅 Active Contributor 或更高等级社区成员可成为 SIG 成员并参与到相应事项中来，但 SIG 各项实行的决策和进行的项目将公开。

## 工作内容

- 代码范围
  - [pd](https://github.com/tikv/pd): 调度实现。
  - [pd_client](https://github.com/tikv/tikv/tree/master/components/pd_client): PD client 的实现。

- 测试规范
  - 提交代码需包括必要的单元测试。合并代码前需保证 CI 全部通过。
  - 对于影响性能的改动，需提供必要的性能测试结果。

- 设计与演进 Proposal
- Review 相关项目代码

## 其他规章流程

- 代码风格、提交规范、PR Description 模板等请参考 [文档](https://github.com/tikv/pd/blob/master/CONTRIBUTING.md)
- 任务分配
  - SIG Tech Lead 在 https://github.com/tikv/community 维护公开的 [成员列表](./membership.md) 与 [任务列表](https://github.com/tikv/pd/projects/5) 链接。
  - 新加入的 SIG 成员可自由领取任务，或参与现有任务的开发或推动，但需与 Tech Lead 或相应任务的负责人进行沟通和同步。
  - SIG 成员需维持每个月参与开发任务，或参与关于现有功能或未来规划的设计与讨论。若连续一个季度不参与开发与讨论，视为不活跃状态，视情况将会被移除 SIG。

- 定期同步进度
  - 每 2 周以文档形式同步一次当前各个项目的开发进度。
  - Slack: [#sig-scheduling](https://slack.tidb.io/invite?team=tikv-wg&channel=sig-scheduling&ref=pingcap-community)

- 组织线上线下成员的活动
- Tech Leads 额外承担的职责
  - SIG 成员提出的问题需要在 2 个工作日给出回复
  - 及时 Review 设计文档和代码
  - 定时发布任务（如果 SIG member 退出后，未完成的任务需要重新分配）

## SIG 活跃规则，晋升机制

- 考核 & 晋升制度
  - Tech Leader 以月为单位对小组成员进行考核，决定成员是否可由 Contributor 晋升为 Active Contributor：
    - 获得至少 2 位 TiKV Reviewer 的提名
    - PR 贡献满足以下条件：
      - 一年内合并 PD 相关 PR 总数超过 8 个

  - Tech Leader 以月为单位对小组成员进行考核，决定成员是否可由 Active Contributor 晋升为 Reviewer：
    - 获得至少 2 位 TiKV Committer 的提名
    - PR 贡献满足以下任意一点：
      - 合并 PD 相关 PR 总数超过 20 个
      - 完成一个重要的 issue

  - Tech Leader 和 TiKV Maintainer 以季度为单位对小组成员进行考核，决定成员是否可由 Reviewer 晋升为 Committer：
    - 获得至少 2 位 TiKV Maintainer 的提名
    - PR 贡献满足以下至少两点：
      - 独立或领导完成两项重要 feature
      - 修复一个重大 bug
      - 有效 Review PD 相关 PR 总数超过 20 个
      - 合并 PD 相关 PR 总数超过 40 个

- 晋级角色权益 & 义务
  - Reviewer
    - 参与项目设计决策
    - 参与 PD 相关 PR Review 与质量控制
    - 对 PD 相关 PR 具有有效的 Approve / Request Change 权限

  - Committer
    - 拥有 Reviewer 具有的权益与义务
    - 整体把控项目的代码质量
    - 指导 Contributor 与 Reviewer

- 退出制度
  - SIG 成员在以下情况中会被移除 SIG，但保留相应的 Active Contributor / Reviewer / Committer 身份：
    - 连续一个季度处于不活跃状态

  - Reviewer 满足以下条件之一会被取消 Reviewer 身份且收回权限（后续重新考核后可恢复）：
    - 有 2 位以上 Committer 认为 Reviewer 能力不足或活跃度不足
