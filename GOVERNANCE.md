> **Note:**
>
> This is a **Work in Progress**. Stay tuned for more follow-up updates!

# TiKV Governance

 This document describes the governance rules of the TiKV project (organization). It is meant to be followed by all projects under the TiKV organization.

- [Code of Conduct](#code-of-conduct)
- [Community groups and roles](#community-groups-and-roles)
    - [Maintainer](#maintainer)
    - [SIGs](#sigs)
    - [Users](#users)
- [Approving PRs](#approving-prs)
- [Decision making and voting](#decision-making-and-voting)
    - [Proposal process](#proposal-process)
- [Adding new SIGs/projects](#adding-new-sigsprojects)

## Code of Conduct

The TiKV community follows the [CNCF Code of Conduct](https://github.com/tikv/tikv/blob/master/CODE_OF_CONDUCT.md).

## Community groups and roles

The TiKV project is comprised of the following types of contributing groups:

- Maintainers
- Special Interest Groups (SIGs)
- Users

### Maintainer

Maintainers are first and foremost contributors that have shown they are committed to the long term success of a project. They are the planners and designers of the TiKV project. Maintainership is about building trust with the current maintainers of the project and being a person that they can depend on to make decisions in the best interest of the project in a consistent manner.

While maintainership indicates a valued member of the community who has demonstrated a healthy respect for the project’s aims and objectives, their work must still be reviewed by the community before being accepted into an official release.

A Maintainer is not allowed to merge their changes without approval from another reviewer. However, they are allowed to sidestep this rule under exceptional circumstances if the changes are approved through other means than the standard process.

#### How to become a Maintainer

Contributors wanting to become maintainers are expected to:

- Enable and promote successful adoptions on the user or ecosystem end
- Actively Propose features to TiKV that are later implemented with great significance to the project direction and the eco-system
- Able to promote substained collaboration within the project
- Demonstrate a deep and comprehensive understanding of TiKV's codebase, technical goals, and directions
- Handle complex problems in the code implementation process

A new Maintainer nominated by an existing Maintainer by updating [TiKV Maintainers](https://github.com/tikv/tikv/blob/master/MAINTAINERS.md#the-tikv-maintainers). This triggers a voting process that requires supermajority votes from the current Maintainers.

If a Maintainer is no longer interested or cannot perform the Maintainer duties listed above, they should volunteer to be moved to emeritus status. In extreme cases this can also occur by a vote of the maintainers per the voting process below.

### SIGs

The TiKV project is organized primarily into Special Interest Groups, or SIGs. Each SIG consists of contributors with a common purpose of advancing the TiKV project for a specific topic, such as Coprocessor, Transaction, or Scheduling. The goal of an SIG is to enable a distributed decision structure and code ownership, as well as providing focused forums for getting work done, making decisions, and onboarding new contributors. Every identifiable subpart of the project (e.g., repository, subdirectory, API, test, issue, PR) is intended to be owned by the corresponding SIG.

Each SIG must have a charter that specifies its scope (topics, code repositories, and directories), responsibilities, areas of authority, how members and roles of authority/leadership are selected/granted, etc. See the [SIG charter template](/sig-governance/SIG-CHARTER-TEMPLATE.md) for details on how charters are formed and managed. SIGs should be relatively free to customize or change how they operate, within some broad guidelines and constraints imposed by this Governance and [Sig Governance](/committee/sig-governance/sig-governance.md).

SIGs are organized and operated by SIG Leads, which is a SIG internal role that oversees the health and sustained development of the SIG. Upon the initial establishment of a SIG, the maintainers will assign 2-3 SIG Leads.

#### Community roles in SIGs

Within a SIG, you could find your path of contribution and growth through multiple roles - Contributor, Active Contributor, Reviewer, and Committer, each with corresponding responsiblities and requirements, as listed below:

| Role | Responsibilities | Requirements | Defined by |
| -----| ---------------- | ------------ | ------- |
Contributor | contribute | initial contribution (PR, issue reporting, answering questions, etc.) | `SIG member` of the SIG |
| Active Contributor | active contributor in the community | sponsored by 2 Reviewers + Continuous contributions (8 or more) to the project. | `SIG member` of the SIG |
| Reviewer | review code contributions | Active Contributor + History of review and authorship within a SIG | `SIG member` of the SIG |
| Committer | set directions and priorities for the sub-projects scoped to the SIG | highly experienced and active Reviewer + major contributions to a subproject | `SIG member` of the SIG|

The roles and responsibilities above are scoped to the SIG and may vary across SIGs. See the corresponding SIG charter for more details on the promotion path.

### Users

Users are community members who have a need for the project. They are the most important members of the community and without them the project would have no purpose. Anyone can be a user; there are no special requirements.

The project asks its users to participate in the project and community as much as possible. User contributions enable the project team to ensure that they are satisfying the needs of those users. Common user contributions include (but are not limited to):

- evangelising the project (e.g. a link on a website and word-of-mouth awareness raising)
- informing developers of strengths and weaknesses from a user's perspective
- providing financial support to facilitate collaboration in testing, development, etc.

Users who continue to engage with the project and its community will often become more and more involved. Such users may find themselves becoming contributors, as described in the [SIG roles](#sig-roles) section.

## Approving PRs

PRs may be merged only after receiving at least two approvals (LGTMs) from Reviewers, more previliged roles from the relevant SIGs, or even Maintainers.

## Decision making and voting

Ideally, all project decisions are resolved by consensus via a PR or GitHub issue. Any of the day-to-day project maintenance can be done by a [lazy consensus](http://communitymgt.wikia.com/wiki/Lazy_consensus) model. Cross-SIG or community-level decisions must be brought to broader awareness via community meetings, slack channels, etc.

In general, we prefer that technical issues and maintainer membership are amicably worked out between the persons involved. If a dispute cannot be decided independently, the Maintainers can be called in to resolve the issue by voting. For voting, a specific statement of what is being voted on should be added to the relevant github issue or PR, and a link to that issue or PR added to the maintainers meeting agenda document. Maintainers should indicate their yes/no vote on that issue or PR, and after a suitable period of time, the votes will be tallied and the outcome noted.

Decision making must comply with the [Guiding Principles](/guiding-principles.md) and [CNCF Code of Conduct](https://github.com/tikv/tikv/blob/master/CODE_OF_CONDUCT.md).

### Proposal process

We use a [Request for Comments (RFC) process for any substantial changes to TiKV. This process involves an upfront design that will provide increased visibility to the community. If you're considering a PR that will bring in a new feature that may affect how TiKV is implemented, or may be a breaking change, then you should start with a RFC. The process is documented in [RFC repository](https://github.com/tikv/rfcs) and have a [template](https://github.com/tikv/rfcs/blob/master/template.md) for you to get started. However, it is suggested that you bring this proposal for initial SIG discussions before you submit the RFC, which makes the process more smooth and efficient.

## Adding new SIGs/projects

New SIGs or sub-projects can be added to the TiKV organization via [RFC process](#proposal-process), as long as as they adhere to the [CNCF charter](https://www.cncf.io/about/charter/) and the guidelines in this document. Once sufficient discussions have taken place under the RFC PR, the Maintainers will call a vote to decide whether the new SIG/project should be added.

