> **Note:**
>
> This is a **Work in Progress**. Stay tuned for more follow-up updates!

# TiKV Governance

This document describes the governance rules of the TiKV project (organization). It is meant to be followed by all the repositories in the project and TiKV contributors.

## Principles

The TiKV community adheres to the following principles:

**Open**: TiKV is open source, as advertised on our [website](https://tikv.org) or the [TiKV Organization](https://github.com/tikv) on github.

**Welcoming and respectful**: See Code of Conduct below.

**Transparent and accessible**: Work and collaboration are done in public.

**Merit**: Ideas and contributions are accepted according to their technical merit and alignment with project objectives, scope, and design principles.

## Code of Conduct

The TiKV community follows the [TiKV Code of Conduct](https://github.com/tikv/tikv/blob/master/CODE_OF_CONDUCT.md). Here are some excerpts:

> In the interest of fostering an open and welcoming environment, we as contributors and maintainers pledge to making participation in our project and our community a harassment-free experience for everyone, regardless of age, body size, disability, ethnicity, sex characteristics, gender identity and expression, level of experience, education, socio-economic status, nationality, personal appearance, race, religion, or sexual identity and orientation.

## Community Roles and Responsibilities

Refer to [Community Membership](/community-membership.md).

## Community Groups

![community organization](/media/governance/community_organization.png)

The project is comprised of and operated by the following subgroups:

- Project Management Committee (PMC)
- Developer Group
    - Maintainers
    - Special Interest Groups, SIGs
    - Working Groups, WGs

### Project Management Committee (PMC)

The PMC functions as the core management body that oversees the TiKV community. While maintainers guide the project on technical matters, the PMC is responsible for stewarding, promoting, and fostering the project. These responsibilities include ensuring the smooth running and continued growth of the project.

Members of the PMC do not have significant authority over other members of the community, although it is the PMC that votes on new Maintainers or Committers, and makes all major decisions for the future with respect to TiKV, such as project-level governance policies, management of sub-structures, security processes and so on. It also makes decisions when community consensus cannot be reached. In addition, the PMC has access to the project’s private mailing list and its archives.

Membership of the PMC is by invitation from the existing PMC members. A nomination will result in discussion and then a vote by the existing PMC members. PMC membership votes are subject to supermajority approval of the current PMC members. See [Voting](#decision-making-and-voting) for more details on the election process.

For the first formation of the committee, our maintainers nominated a group of people who had great impact or influence on the project, including some members from PingCAP who founded TiKV. New PMC members are selected based on the rules described above. The term is one year.

For a list of the current PMC members, see the [PMC Members](/committee/README.md#members).

<!--- need the link to a Guiding Principals (Missions, Values; to be added separately) page as the principals for PMC -->

### Developer Group

As the cornerstone of community development, the TiKV Developer Group consists of these roles: Maintainer, Committer, Reviewer, Active Contributor, and Contributor. Each role takes corresponding responsibilities in the community. Collectively they play an important role in the robust development of TiKV. Among these roles, the Maintainers  For more details, refer to [Community Membership](/community-membership.md).

The Developer Group operates TiKV projects in two groups: Special Interest Group (SIG) and Working Group (WG). The diagram below illustrates the definition of the SIG and WG, the internal roles of the group, and the role promotion path.

![developer group](/media/governance/developer_group.png)

### Maintainers

While the PMC is the core management group that oversees the project, Maintainers are the technical authority in the Developer Group who function as planners and designers of each project. Maintainers set technical directions and priorities for the sub-project owned by the specific SIG, and ensure its sustained health and development. They make or approve design decisions for the project - either directly or by delegating these responsibilities. Maintainers are appointed by the PMC with supermajority votes.

If a Maintainer is no longer interested or cannot perform the Maintainer duties listed above, they should volunteer to be moved to emeritus status.

See [TiKV Maintainers](https://github.com/tikv/tikv/blob/master/MAINTAINERS.md#the-tikv-maintainers) for the list of current Maintainers.

#### SIGs

The TiKV project is organized primarily into Special Interest Groups, or SIGs. Each SIG consists of members from multiple companies or organizations, with a common purpose of advancing the TiKV project for a specific topic, such as Coprocessor or Documentation. The goal of an SIG is to enable a distributed decision structure and code ownership, as well as providing focused forums for getting work done, making decisions, and onboarding new contributors. Every identifiable subpart of the project (e.g., github org, repository, subdirectory, API, test, issue, PR) is intended to be owned by the corresponding SIG.

Currently, any Contributor within a SIG is immediately eligible member of that SIG. It is our intention to properly guide or mentor community talents, and help them advance to the higher-level Reviewer, Committer within an SIG.

Each SIG must have a charter that specifies its scope (topics, code repositories, and directories), responsibilities, areas of authority, how members and roles of authority/leadership are selected/granted, how decisions are made, and how conflicts are resolved. See the [SIG charter template](/sig-governance/SIG-CHARTER-TEMPLATE.md) for details on how charters are formed and managed. SIGs should be relatively free to customize or change how they operate, within some broad guidelines and constraints imposed by this Governance and [Sig Governance](/committee/sig-governance/sig-governance.md).

A primary reason that SIGs exist is as forums for collaboration. Much work in a SIG should stay local within that SIG. However, SIGs must communicate to ensure other SIGs and community members can find notes of meetings, discussions, designs, and decisions, and periodically communicate a high-level summary of the SIG's work to the community.

SIGs are organized and operated by Tech Leads, which is a SIG internal role that oversees the health and sustained development of the SIG. Upon the initial establishment of a SIG, the maintainers will assign 2-3 Tech Leads.

#### Working Groups

A Working Group is formed by community developers who gather together to accomplish a specific goal. To achieve the goal, some WGs may span over multiple SIGs, and some WGs may only focus on something specific in a specific SIG.

Each WG has its life cycle. Once the goal is completed, the group will be disbanded. The only goal of WG operations and management is to ensure that the goals set by the group are completed at the right time. In general, the working group hold periodic meetings to summarize the current project progress and determine the plans for next steps.

WG is subject to PMC's oversight over its formation and disbanding.

See [Working Group Governance](./governance/wg-governance.md) for more information on how a WG run.

## Contributions

Anyone can contribute to the project, regardless of their skills, as there are many ways to contribute. The various ways of contributing are described in more detail in a separate document. For details, see [Contributing to TiKV](https://github.com/tikv/tikv/blob/master/CONTRIBUTING.md).

## Decision making and voting

Proposals and ideas can be submitted for agreement via a github issue or PR. Depending on the nature, decisions about the future of the project are made by the PMC or by Maintainers. As the technical authority, Maintainers set technical direction and priorities for the SIG projects, while the PMC makes other high-level decisions like establishment and operation policies of sub-projects, sub-structures, promoting new Maintainers, security processes, etc.

Major changes such as feature proposals and organization or process changes should be brought to the PMC or Maintainers’ attention through the [Request for Comments (RFC)](https://github.com/tikv/rfcs) process. For the change to happen, the RFC must earn the supermajority (2/3) votes in the corresponding group.

## Conflict resolution

In general, we prefer that technical issues and other disputes upon which consensus can't be reached are amicably worked out between the persons involved. If a dispute cannot be decided independently, depending on the nature, the PMC or Maintainers can be called in to resolve the issue by voting based on the [Principles](#principles) and [Code of Conduct](https://github.com/tikv/tikv/blob/master/CODE_OF_CONDUCT.md). The same PR can be used or a separate PR can be opened in the concerned repository for voting.

## Adding new projects

New projects can be added to the TiKV organization (normally by Tech Leads of a SIG) via GitHub issue discussion in one of the existing SIG, as long as as they adheres to the [CNCF charter](https://www.cncf.io/about/charter/) and the guidelines in this governance. Once sufficient discussions have taken place, the Maintainers will decide whether the new project should be added. The requester needs to create an corresponding RFC for the change to happen, as described in [Decision Making and Voting](#decision-making-and-voting).

## Changes in Governance

Any change in this Governance document, or similar nature of changes to other governance related documents, shall be initiated as an RFC and go through the voting process as described in [Decision Making and Voting](#decision-making-and-voting).

## Credits

The contents of this document are based on <http://oss-watch.ac.uk/resources/meritocraticgovernancemodel> by Ross Gardler and Gabriel Hanganu, and [Kubernetes Governance](https://github.com/kubernetes/community/blob/master/governance.md).
