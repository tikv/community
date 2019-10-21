# SIG Governance
SIG 全称 Special Interest Group。SIG 在社区架构中的位置请见：[社区架构 & 角色](/GOVERNACE-zh_CN.md#community_organization)。SIG 主要聚集一批 Active Contributor，对某一个或多个 TiKV 的模块深入研究 & 贡献，在 SIG 内部一步步晋升为 Reviewer，Committer。 

## SIG 角色以及组织治理

SIG 遵循 [社区治理规范](/GOVERNACE-zh_CN.md) 中的角色定义。SIG 需要遵守以下规则：

* 在开始一个 SIG 之前，需要提前确立好章程，创建章程请参考：创建 SIG 章程步骤。
* 定期组织会议，至少每双周组织一次，除非法定节假日，并且产出会议记录
* 确立 SIG 可分配任务以及难易程度，由 SIG 成员认领

其他请参见：[SIG 生命周期](#sig_lifetime)

## 角色

<h3 id="active_contributor">Active Contributor</h3>

* 区别于社区的 Active Contributor， 指被推举进入本 SIG 的 Active Contributor。
* 需要保持 SIG 中至少一个模块的活跃度
* 需要持续保持至少一个模块的贡献
* 可以参与 SIG 内 Proposal 的提议以及讨论

### Reviewer

参见 [Reviewer 定义](/community-membership-zh_CN.md#reviwer)

### Committer

参见 [Committer 定义](/community-membership-zh_CN.md#committer)

### Tech Lead

* 数量 2 - 3 名
* 负责组织 SIG 内部成员的培训，学习
* 对 SIG 内部产生的 Proposal 需要组织讨论以及作出决策
* 负责 SIG 的活跃以及产出
* 需要带领 SIG 产生更多的 Revewer，Commiter 
* 需要对 SIG 的任务执行分配，跟进进度
* 需要参与委员会组织的定期会议
* 每年需要为 SIG 制定 roadmap
* 周进度会议至少需要一名 Tech Lead 在线参与讨论

## 成员晋升机制

SIG 的成员可以晋升到更高的角色，规则由各 SIG 自行制定。每一次晋升需由更高一级角色或以上角色的两位成员提名。

## 成员退出机制

SIG 的成员在一段时间的不活跃之后，该成员会暂时请出 SIG。退出机制，由各 SIG 自行制定。

## 组织治理

* SIG 需要 bi-weekly 组织一次会议
* 应由 Tech Lead 发起除非被委任给了其他的成员

<h3 id="step_to_create_sig_charter">创建 SIG 章程步骤</h3>

1. 复制 [SIG 章程模板](SIG-CHARTER-zh_CN.md)
2. 修改模板中需要为新 SIG 定义的内容
3. 向 [TiKV Community](https://github.com/tikv/community) 发起 Pull Request，将相应的 SIG 章程提交到 [SIGs 目录](/SIGs)
4. PR 被批准合并之后，会由社区委员会公布新的 SIG

<h2 id="sig_lifetime">SIG 生命周期</h2>

### 创建

1. 确保所有的 SIG Technical Leads，和其他角色至少是 [Active Contributor](#active_contributor)。
3. 遵从 [创建 SIG 章程步骤](#step_to_create_sig_charter) 创建一个 SIG 的章程
4. 联系社区委员会，在 tikv-wg.slack.com 建立相应 Slack Channel，用以讨论 SIG 相关事项
5. 创建一个 Zoom 房间用于定期会议，以及其他线上讨论
6. 在 TiKV Community 中宣布成立新的 SIG

### 解散

有时候，SIG 可能是需要被解散或者被合并的。SIG 的解散规则应该在各自的章程中定义。
