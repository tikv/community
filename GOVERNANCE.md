> **Note**
>
> This is a **Work in Progress**. Stay tuned for more follow-up updates!

# Governance

TiKV is a community driven project. Anyone with an interest in the project can join the community, contribute to the project design and participate in the decision making process. This document describes how that participation takes place and how to set about earning merit within the project community.

## Code of Conduct

The TiKV community follows the [TiKV Code of Conduct](https://github.com/tikv/tikv/blob/master/CODE_OF_CONDUCT.md). Here are some excerpts:

> In the interest of fostering an open and welcoming environment, we as contributors and maintainers pledge to making participation in our project and our community a harassment-free experience for everyone, regardless of age, body size, disability, ethnicity, sex characteristics, gender identity and expression, level of experience, education, socio-economic status, nationality, personal appearance, race, religion, or sexual identity and orientation.

## Community Roles and Responsibilities

Refer to [Community Membership](/community-membership.md).

## Community Structure

![community organization](/media/governance/community_organization.png)

The project is comprised of and operated by the following types of subgroups:

- Project Management Committee, PMC
- Maintainers
- Organizer Committee
- Developer Group
    - Special Interest Groups, SIGs
    - Working Groups, WGs

### Project Management Committee

The PMC functions as the core management team that oversees the TiKV community. The PMC has additional responsibilities over and above those of Maintainers. These responsibilities ensure the smooth running of the project. PMC members are expected to review code contributions, participate in strategic planning, approve changes to the governance model and manage the copyrights within the project outputs.

Members of the PMC do not have significant authority over other members of the community, although it is the PMC that votes on new Maintainers or Committers, and makes all major decisions for the future with respect to TiKV, such as project-level governance policies, management of sub-structures, security processes and so on. It also makes decisions when community consensus cannot be reached. In addition, the PMC has access to the project’s private mailing list and its archives.

Membership of the PMC is by invitation from the existing PMC members. A nomination will result in discussion and then a vote by the existing PMC members. PMC membership votes are subject to consensus approval of the current PMC members.

For the first formation of the committee our maintainers nominated a group of people who had great impact or influence on the project, including some members from PingCAP who founded TiKV. Future PMC numbers are generated based on the rules described above.

For a list of the current PMC members, see the [PMC Members](/committee/.README.md#members).

<!--- need the link to a Guiding Principals (Missions, Values; to be added separately) page as the principals for PMC -->

### Maintainers

While the PMC is the core management group that oversees the project, Maintainers are the technical authority in the Developer Group who function as planners and designers of the project. Maintainers set technical direction and priorities for the sub-project, and ensure its continued health and development. They make or approve design decisions for the project - either directly or by delegating these responsibilities. Maintainers are appointed by the PMC with anonymous votes.

### Organizer Committee

The Organizer Committee consists of organizers in charge of event or activity operations. They are in charge of the execution of PMC’s strategies and decisions. Specifically, the members are the leaders of user groups or community event organizers across regions.

### Developer Group

As the cornerstone of community development, the TiKV Developer Group consists of these roles: Maintainer, Committer, Reviewer, Active Contributor, and Contributor. Each role takes corresponding responsibilities in the community. Collectively they play an important role in the robust development of TiDB. For more deitals, refer to [Community Membership](/community-membership.md).

The Developer Group operates TiKV projects in two function forms: Special Interest Group (SIG) and Working Group (WG). The diagram below illustrates the definition of the SIG and WG, the internal roles of the group, and the role promotion path.

![developer group](/media/governance/developer_group.png)

#### SIGs

The TiKV project is organized primarily into Special Interest Groups, or SIGs. Each SIG is comprised of members from multiple companies and organizations, with a common purpose of advancing the project with respect to a specific topic, such as Coprocessor or Documentation. Our goal is to enable a distributed decision structure and code ownership, as well as providing focused forums for getting work done, making decisions, and onboarding new contributors. Every identifiable subpart of the project (e.g., github org, repository, subdirectory, API, test, issue, PR) is intended to be owned by some SIG.

Currently SIG membership requires invitation - potential qualified members are Active Contributors in a particular module. It is our intention to properly guide or mentor community talents, and help them advance to the higher-level Reviewer, Committer and Maintainer within an SIG.

Each SIG must have a charter that specifies its scope (topics, code repos and directories), responsibilities, areas of authority, how members and roles of authority/leadership are selected/granted, how decisions are made, and how conflicts are resolved. See the SIG charter process for details on how charters are managed. SIGs should be relatively free to customize or change how they operate, within some broad guidelines and constraints imposed by cross-SIG processes.

See [sig governance](/sig-governance/sig-governance.md) for more details about current SIG operating mechanics, such as mailing lists, meeting times, etc.

#### Working Groups

A Working Group is formed by community developers who gather together to accomplish a specific goal. To achieve the goal, some WGs may span over multiple SIGs, and some WGs may only focus on something specific in a specific SIG.

Each WG has its life cycle. Once the goal is completed, the group will be disbanded. The only goal of WG operations and management is to ensure that the goals set by the group are completed at the right time. In general, the working group hold periodic meetings to summarize the current project progress and determine the plans for next steps.

<!---to add Working Group governance link -->

## Contributions

Anyone can contribute to the project, regardless of their skills, as there are many ways to contribute. The various ways of contributing are described in more detail in a separate document. For details, see [Contributing to TiKV](https://github.com/tikv/tikv/blob/master/CONTRIBUTING.md).

## Support

All participants in the community are encouraged to provide support for new users within the project management infrastructure. This support is provided as a way of growing the community. Those seeking support should recognize that all support activity within the project is voluntary and is therefore provided as and when time allows. A user requiring guaranteed response times or results should therefore seek to purchase a support contract from a community member. However, for those willing to engage with the project on its own terms, and willing to help support other users, the community support channels are ideal.

## Decision Making Process

Depending on the nature, decisions about the future of the project are made by the PMC or by Maintainers. As the technical authority, Maintainers set technical direction and priorities for the sub-project, while PMC make other high-level decisions like establishment and operation policies of sub-projects, sub-structures, promoting new Maintainers, security processes, etc. New proposals and ideas (changes of major features, organization, or processes) can be brought to the PMC or Maintainers’ attention through the [Request for Comments (RFC)](https://github.com/tikv/rfcs) process. For the change to happen, the RFC must earn the majority votes in the corresponding group.

## Credits

The contents of this document are based on <http://oss-watch.ac.uk/resources/meritocraticgovernancemodel> by Ross Gardler and Gabriel Hanganu, and [Kubernetes Governance](https://github.com/kubernetes/community/blob/master/governance.md).