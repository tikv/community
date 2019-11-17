> **Note**
>
> This is a **Work in Progress**. Stay tuned for more follow-up updates!

# Governace

The TiKV community is a meritocratic, consensus-based community project. Anyone with an interest in the project can join the community, contribute to the project design and participate in the decision making process. This document describes how that participation takes place and how to set about earning merit within the project community.

## Code of Conduct

The TiKV community follows the TiKV Code of Conduct. Here are some excerpts:

> In the interest of fostering an open and welcoming environment, we as contributors and maintainers pledge to making participation in our project and our community a harassment-free experience for everyone, regardless of age, body size, disability, ethnicity, sex characteristics, gender identity and expression, level of experience, education, socio-economic status, nationality, personal appearance, race, religion, or sexual identity and orientation.

## Community Roles and Responsibilities

Refer to [Community Membership](community-membership.md).

## Community Structure

![community organization](/media/governace/community_organization.png)

The project is comprised of the following types of subgroups:

- Project Management Committee, PMC
- Organizer Committee
- Developer Group
    - Special Interest Groups, SIGs
    - Working Groups, WGs

### Project Management Committee

The PMC functions as the core management team that oversees the TiKV community. It consists of those individuals identified as Maintainers on the development site. The PMC has additional responsibilities over and above those of a committer. These responsibilities ensure the smooth running of the project. PMC members are expected to review code contributions, participate in strategic planning, approve changes to the governance model and manage the copyrights within the project outputs.

Members of the PMC do not have significant authority over other members of the community, although it is the PMC that votes on new committers, and makes all major decisions for the future with respect to TiKV. It also makes decisions when community consensus cannot be reached. In addition, the PMC has access to the project’s private mailing list and its archives. This list is used for sensitive issues, such as votes for new committers and legal matters that cannot be discussed in public. It is never used for project management or planning.

Membership of the PMC is by invitation from the existing PMC members. A nomination will result in discussion and then a vote by the existing PMC members. PMC membership votes are subject to consensus approval of the current PMC members.

The current list of PMC members are:

- Max Liu(**[@goroutine](https://github.com/ngaut/)**)
- Ed Huang(**[@c4pt0r](https://github.com/c4pt0r)**)
- Dylan Cui(**[@qiuyesuifeng](https://github.com/qiuyesuifeng)**)
- Li Shen(**[@shenli](https://github.com/shenli)**)
- Siddon Tang(**[@siddontang](https://github.com/siddontang)**)
- Yin Liu(**[@iamxy](https://github.com/iamxy)**)
- Jian Zhang(**[@zz-json](https://github.com/zz-jason)**)
- Wink Yao(**[@winkyao](https://github.com/winkyao)**)

### Organizer Committee

The Organizer Committee consists of organizers in charge of event or activity operations. They are in charge of the execution of PMC’s strategies and decisions. Specifically, the members are the leaders of user groups or community event organizers across regions.

### Developer Group

As the cornerstone of community development, the TiKV Developer Group consists of these roles: Maintainer, Committer, Reviewer, Active Contributor, and Contributor. Each role takes corresponding responsibilities in the community. Collectively they play an important role in the robust development of TiDB.

The Developer Group operates TiKV projects in two function forms: Special Interest Group (SIG) and Working Group (WG). The diagram below illustrates the definition of the SIG and WG, the internal roles of the group, and the role promotion path.

![developer group](/media/governace/developer_group.png)

#### SIGs

The TiKV project is organized primarily into Special Interest Groups, or SIGs. Each SIG is comprised of members from multiple companies and organizations, with a common purpose of advancing the project with respect to a specific topic, such as Coprocessor or Documentation. Our goal is to enable a distributed decision structure and code ownership, as well as providing focused forums for getting work done, making decisions, and onboarding new contributors. Every identifiable subpart of the project (e.g., github org, repository, subdirectory, API, test, issue, PR) is intended to be owned by some SIG.

Currently SIG membership requires invitation - potential qualified members are Active Contributors in a particular module. It is our intention to properly guide or mentor community talents, and help them advance to the higher-level Reviewer, Committer and Maintainer within an SIG.

Each SIG must have a charter that specifies its scope (topics, code repos and directories), responsibilities, areas of authority, how members and roles of authority/leadership are selected/granted, how decisions are made, and how conflicts are resolved. See the SIG charter process for details on how charters are managed. SIGs should be relatively free to customize or change how they operate, within some broad guidelines and constraints imposed by cross-SIG processes.

See [sig governance](../sig-governace/sig-governace.md) for more details about current SIG operating mechanics, such as mailing lists, meeting times, etc.

#### Working Groups

A Working Group is formed by community developers who gather together to accomplish a specific goal. To achieve the goal, some WGs may span over multiple SIGs, and some WGs may only focus on something specific in a specific SIG.

Each WG has its life cycle. Once the goal is completed, the group will be disbanded. The only goal of WG operations and management is to ensure that the goals set by the group are completed at the right time. In general, the working group hold periodic meetings to summarize the current project progress and determine the plans for next steps.

## Contributions

Anyone can contribute to the project, regardless of their skills, as there are many ways to contribute. The various ways of contributing are described in more detail in a separate document. For details, see [Contributing to TiKV](https://github.com/tikv/tikv/blob/master/CONTRIBUTING.md).

## Support

All participants in the community are encouraged to provide support for new users within the project management infrastructure. This support is provided as a way of growing the community. Those seeking support should recognize that all support activity within the project is voluntary and is therefore provided as and when time allows. A user requiring guaranteed response times or results should therefore seek to purchase a support contract from a community member. However, for those willing to engage with the project on its own terms, and willing to help support other users, the community support channels are ideal.

## Decision Making Process

Decisions about the future of the project are made by the PMC. New proposals and ideas (changes of major features, organization, or processes) can be brought to the PMC’s attention through the [Request for Change (RFC)](https://github.com/tikv/rfcs)process. For the change to happen, the RFC must earn the majority votes in the PMC.

## Credits

The contents of this document are based on <http://oss-watch.ac.uk/resources/meritocraticgovernancemodel> by Ross Gardler and Gabriel Hanganu, and [Kubernetes Governance](https://github.com/kubernetes/community/blob/master/governance.md).