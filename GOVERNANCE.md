# TiKV Governance

This document defines governance policies of the TiKV project. It is meant to be followed by all projects under the TiKV organization.

## Roles and Responsibilities

### Steering Committee

Steering committee members demonstrate a strong commitment to the project with views in the interest of the broader TiKV project.

Responsibilities include:

* Own the overall direction of the TiKV project.
* Speaking on behalf of the project.
* Maintaining guidelines of the project.
* Nominating new committee members.

Membership of steering committee is by invitation only and must be approved by a consensus of the steering committee. A committee member is considered emeritus by their own declaration. An emeritus member may request reinstatement to the steering committee, which will be sufficient to restore him or her to active committee member.

Membership of steering committee can be revoked by a consensus vote of the steering committee other than the member in question.

The current list of steering committee members is as below, in alphabetical order on last name.

| Name                                     | Represents    | GitHub                                                  |
| ---------------------------------------- | ------------- | :------------------------------------------------------ |
| Fu Chen <cfworking1990@gmail.com>        | Yidian Zixun  | [fredchenbj](https://github.com/fredchenbj)             |
| Daobing Li <lidaobing@gmail.com>         | JD Cloud & AI | [lidaobing](https://github.com/lidaobing)               |
| Jay Li <jay@pingcap.com>                 | PingCAP       | [BusyJay](https://github.com/BusyJay)                   |
| Xiaoguang Sun <sunxiaoguang@pingcap.com> | PingCAP       | [sunxiaoguang](https://github.com/sunxiaoguang)         |
| Siddon Tang <tl@pingcap.com>             | PingCAP       | [siddontang](https://github.com/siddontang)             |
| Wink Yao <wink@pingcap.com>              | PingCAP       | [winkyao](https://github.com/winkyao)                   |
| Jinpeng Zhang <zhangjinpeng@pingcap.com> | PingCAP       | [zhangjinpeng1987](https://github.com/zhangjinpeng1987) |
| Dongxu Huang <huang@pingcap.cn>          | PingCAP       | [c4pt0r](https://github.com/c4pt0r)                     |

### Teams

Teams are persistent open groups that focus on a part of the TiKV project. A team has its reviewer, committer and maintainer, and owns one or more repositories. Team level decision making comes from its maintainers.

The current list of teams is under the [teams](teams/README.md) directory.

#### Reviewers

Reviewers are individuals who actively make contribution and are willing to participate in the code review of new contributions. We identify reviewers from active contributors. The committers should explicitly solicit reviews from reviewers. High-quality code reviews prevent technical debt for long-term and are crucial to the success of the project. A pull request to the project has to be reviewed by at least one reviewer in order to be merged.

Review access is by invitation only and must be approved by consensus of the maintainers. A reviewer is considered emeritus by their own declaration. An emeritus reviewer may request reinstatement of review access from the maintainers, which will be sufficient to restore him or her to active reviewer status.

Review access can be revoked by consensus by the maintainers (except the reviewer in question if they are also a maintainer).

#### Committers

Committers are individuals who are granted the write access to the repositories belong to the team. A committer is usually responsible for a certain area or several areas of the code where they oversee the code review process. The area of contribution can take all forms, including code contributions and code reviews, documents, education, and outreach. Committers are essential for a high quality and healthy project.

Commit access is by invitation only and must be approved by consensus of the maintainers. A committer is considered emeritus by their own declaration. An emeritus committer may request reinstatement of commit access from the maintainers, which will be sufficient to restore him or her to active committer status.

Commit access can be revoked by consensus by the maintainers (except the committer in question if they are also a maintainer).

#### Maintainers

The maintainers consist group of active committers that moderate the discussion, manage the project release, and proposes new committers or maintainers. Potential candidates are usually proposed via an internal discussion among maintainers, followed by a consensus approval, i.e. a concrete number of approvals, and no vetoes. Any veto must be accompanied by reasoning. Maintainers should serve the community by upholding the community practices and guidelines TiKV a better community for everyone. Maintainers  should nominate new reviewer, committers and maintainers, and should also strive to only nominate new candidates outside of their own organization.

Membership of the maintainers is by invitation only and must be approved by a consensus of the maintainers. A maintainer is considered emeritus by their own declaration. An emeritus member may request reinstatement to the maintainers, which will be sufficient to restore him or her to active maintainers.

Membership of the maintainers can be revoked by a consensus vote of all the maintainers other than the member in question.

### Infrastructure

The Infrastructure team, known as Infra, provides and manages all infrastructure and services for the TiKV project. This infrastructure includes the various machines and their operating systems, discussion forum, and GitHub settings. Infra is responsible for systems administration and security, and supports existing teams at the TiKV project. Infra works hard to provide services and setup for each new team.

Infra does not participant in the project or team decision making process, but help on applying the decision.

Membership of Infra is by invitation only and must be approved by a consensus of the steering committee. A team member is considered emeritus by their own declaration. An emeritus member may request reinstatement to Infra, which will be sufficient to restore him or her to active Infra member.

Membership of Infra can be revoked by a consensus vote of the steering committee (except the member in question if they are also a committee member).

The current list of Infra members is as below, in alphabetical order on last name.

| Name                                  | GitHub                                           |
| ------------------------------------- | :----------------------------------------------- |
| Zili Chen <wander4096@gmail.com>      | [tisonkun](https://github.com/tisonkun)          |
| Zhiyuan Liang <minianter@foxmail.com> | [Mini256](https://github.com/Mini256)            |
| Xiang Zhang <angwerzx@126.com>        | [zhangyangyu](https://github.com/zhangyangyu)    |
| Qiang Zhou <zhouqiang.cl@gmail.com>   | [zhouqiang-cl](https://github.com/zhouqiang-cl/) |

## Decision Making

Within the TiKV project, different types of decisions require different forms of approval. For example, the previous section describes several decisions which require 'consensus' approval. This section defines how voting is performed, the types of approvals, and which types of decision require which type of approval.

### Voting

Decisions regarding the project are made by votes on [the primary project community repository](https://github.com/tikv/community). Votes are clearly indicated by a pull request adding an entry under [votes](votes/README.md) folder. Votes may contain multiple items for approval and these should be clearly separated. Voting is carried out by replying to the vote pull request. Voting may take three flavors

* **+1**: 'Yes,' 'Agree,' or 'the action should be performed.'
* **0**: Neutral about the proposed action (or mildly negative but not enough so to want to block it).
* **-1**: This is a negative vote. On issues where consensus is required, this vote counts as a veto. All vetoes must contain an explanation of why the veto is appropriate. Vetoes with no explanation are void. It may also be appropriate for a -1 vote to include an alternative course of action.

All participants in the TiKV project are encouraged to show their agreement with or against a particular action by voting. For team decisions, only the votes of active team maintainers are binding. For project decisions, only the votes of active steering committee members are binding. Non-binding votes are still useful for those with binding votes to understand the perception of an action in the wider TiKV community.

Voting can also be applied to changes already made to the TiKV codebase. These typically take the form of a veto (-1) in reply to the commit message sent when the commit is made. Note that this should be a rare occurrence. All efforts should be made to discuss issues when they are still patches before the code is committed.

Only active (i.e. non-emeritus) maintainers and steering committee members have binding votes.

### Approvals

These are the types of approvals that can be sought. Different actions require different types of approvals.

* **Consensus**: Consensus requires 2 binding +1 votes and no binding vetoes.
* **Lazy Majority**: A lazy majority vote requires 2 binding +1 votes and more binding +1 votes than -1 votes.
* **2/3 Majority**: Some actions require a 2/3 majority to pass. Such actions typically affect the foundation of the project (e.g. adopting a new codebase). The higher threshold is designed to ensure such changes are strongly supported. To pass this vote requires at least 2/3 of binding vote holders to vote +1.

> In order to address the case of insufficient active binding voters to reach 2/3 majority, one can follow the process below to exclude a binding vote from the counting of this particular voting thread. 
> 
> 1. Wait until the minimum length of the voting passes.
> 2. Publicly reach out via mentioned to the remaining binding voters in the voting pull request for at least 2 attempts with at least 7 days between two attempts.
> 3. If the binding voter being contacted still failed to respond after all the attempts, the binding voter will be considered as inactive for the purpose of this particular voting.

### Vetoes

A valid, binding veto cannot be overruled. If a veto is cast, it must be accompanied by a valid reason explaining the reasons for the veto. The validity of a veto, if challenged, can be confirmed by anyone who has a binding vote. This does not necessarily signify agreement with the veto - merely that the veto is valid.

If you disagree with a valid veto, you must lobby the person casting the veto to withdraw their veto. If a veto is not withdrawn, the action that has been vetoed must be reversed in a timely manner.

### Actions

Steering committee is permitted to take over team level decision making from the team maintainers, e.g., new maintainer or maintainer removal by consensus. However, it is a safety valve and the committee should avoid actually doing that.

| Actions                  | Description                                                                                                                                                                                                                                         | Approval      | Binding Voters           | Minimum Length (days) |
| :----------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------ | :----------------------- | :-------------------- |
| New Reviewer             | When a new reviewer is proposed for the team.                                                                                                                                                                                                       | Lazy Majority | Active maintainers       | 3                     |
| New Committer            | When a new committer is proposed for the team.                                                                                                                                                                                                      | Consensus     | Active maintainers       | 6                     |
| New Maintainer           | When a new maintainer is proposed for the team.                                                                                                                                                                                                     | Consensus     | Active maintainers       | 6                     |
| New Infra Member         | When a new member of the infrastructure team is proposed.                                                                                                                                                                                           | Consensus     | Active committee members | 3                     |
| New Committee Member     | When a new member of the steering committee is proposed. Note: such actions will also be referred to the CNCF by the steering committee.                                                                                                            | Consensus     | Active committee members | 6                     |
| Reviewer Removal         | When removal of review privileges is sought.                                                                                                                                                                                                        | Consensus     | Active maintainers       | 6                     |
| Committer Removal        | When removal of commit privileges is sought.                                                                                                                                                                                                        | Consensus     | Active maintainers       | 6                     |
| Maintainer Removal       | When removal of maintain privileges is sought. Note: such actions will also be referred to the CNCF by the steering committee.                                                                                                                      | Consensus     | Active maintainers       | 6                     |
| Infra Member Removal     | When removal of the infrastructure team membership is sought.                                                                                                                                                                                       | Consensus     | Active committee members | 6                     |
| Committee Member Removal | When removal of committee membership is sought.                                                                                                                                                                                                     | Consensus     | Active committee members | 6                     |
| Adoption of New Codebase | Adoption of large existing external codebase. This refers to contributions big enough that potentially change the shape and direction of the project with massive restructuring and future maintenance commitment, or potentially build a new team. | 2/3 majority  | Active committee members | 6                     |
| Modifying Governance     | Modifying this document                                                                                                                                                                                                                             | 2/3 majority  | Active committee members | 6                     |
