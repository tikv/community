> **Note:**
>
> This is a **Work in Progress**. Stay tuned for more follow-up updates!

# TiKV Governance

 This document describes the governance rules of the TiKV project (organization). It is meant to be followed by all the repositories in the project and the TiKV project.

<!-- TOC -->

- [TiKV Governance](#tikv-governance)
    - [Code of Conduct](#code-of-conduct)
    - [Community groups and roles](#community-groups-and-roles)
        - [Maintainer](#maintainer)
            - [How to become a Maintainer](#how-to-become-a-maintainer)
        - [SIGs](#sigs)
            - [SIG Roles](#sig-roles)
        - [Users](#users)
    - [Approving PRs](#approving-prs)
    - [Decision making and voting](#decision-making-and-voting)
        - [Proposal process](#proposal-process)
    - [Adding new projects](#adding-new-projects)

<!-- /TOC -->

## Code of Conduct

The TiKV community follows the [CNCF Code of Conduct](https://github.com/tikv/tikv/blob/master/CODE_OF_CONDUCT.md).

## Community groups and roles

The TiKV project is comprised of the following types of contributing groups:

- Maintainers
- Special Interest Groups (SIGs)
- Users

### Maintainer

Maintainers are first and foremost contributors that have shown they are committed to the long term success of a project. They are the planners and designers of the TiKV project, with the authority to merge branches into the master branch. Maintainership is about building trust with the current maintainers of the project and being a person that they can depend on to make decisions in the best interest of the project in a consistent manner.

While maintainership indicates a valued member of the community who has demonstrated a healthy respect for the project’s aims and objectives, their work must be reviewed by the community before acceptance in an official release.

A Maintainer is not allowed to merge their change without approval from another person. However, they are allowed to sidestep this rule under justifiable circumstances. For example:

- If a CI tool is broken, they may override the tool to still submit the change.
- Minor typos or fixes for broken tests.
- The change was approved through other means than the standard process.

#### How to become a Maintainer

Contributors wanting to become maintainers are expected to:

- Enable and promote successful adoptions on the user or ecosystem end
- Actively Propose features to TiKV that are later implemented with great significance to the project direction and the eco-system
- Able to promote substained collaboration within the project
- Demonstrate a deep and comprehensive understanding of TiKV's codebase, technical goals, and directions
- Handle complex problems in the code implementation process

A new Maintainer must be self-nominated or nominated by an existing Maintainer by updating [TiKV Maintainers](https://github.com/tikv/tikv/blob/master/MAINTAINERS.md#the-tikv-maintainers). This triggers a voting process that that requires supermajority votes from the current Maintainers.

If a Maintainer is no longer interested or cannot perform the Maintainer duties listed above, they should volunteer to be moved to emeritus status. In extreme cases this can also occur by a vote of the maintainers per the voting process below.

### SIGs

The TiKV project is organized primarily into Special Interest Groups, or SIGs. Each SIG consists of contributors with a common purpose of advancing the TiKV project for a specific topic, such as Coprocessor, Transaction, or Scheduling. The goal of an SIG is to enable a distributed decision structure and code ownership, as well as providing focused forums for getting work done, making decisions, and onboarding new contributors. Every identifiable subpart of the project (e.g., repository, subdirectory, API, test, issue, PR) is intended to be owned by the corresponding SIG.

Each SIG must have a charter that specifies its scope (topics, code repositories, and directories), responsibilities, areas of authority, how members and roles of authority/leadership are selected/granted, etc. See the [SIG charter template](/sig-governance/SIG-CHARTER-TEMPLATE.md) for details on how charters are formed and managed. SIGs should be relatively free to customize or change how they operate, within some broad guidelines and constraints imposed by this Governance and [Sig Governance](/committee/sig-governance/sig-governance.md).

SIGs are organized and operated by SIG Leads, which is a SIG internal role that oversees the health and sustained development of the SIG. Upon the initial establishment of a SIG, the maintainers will assign 2-3 Tech Leads.

#### SIG Roles

Within a SIG, you could find your path of contribution and growth through multiple roles - Contributor, Active Contributor, Reviewer, and Committer, each with corresponding responsiblities and requirements, as listed below:

| Role | Responsibilities | Requirements | Defined by |
| -----| ---------------- | ------------ | -------|
｜Contributor | Contribute | initial contribution (PR, issue reporting, answering questions, etc.) | 'Contributor List"|
| Active Contributor | active contributor in the community | sponsored by 2 Reviewers. Multiple contributions (8+) to the project. | `SIG member`  of the SIG |
| Reviewer | Review code contributions | Active Contributor + History of review and authorship within a SIG | `SIG member` of the SIG |
| Committer | Set directions and priorities for the sub-projects scoped to the SIG + guide Reviwers and Contributors | highly experienced and active Reviewer + major contributions to a subproject | `SIG member` of the SIG|

The roles and responsibilites above are scoped to the SIG and may vary across SIGs. See more details in the corresponding SIG charter.

### Users

Users are community members who have a need for the project. They are the most important members of the community and without them the project would have no purpose. Anyone can be a user; there are no special requirements.

The project asks its users to participate in the project and community as much as possible. User contributions enable the project team to ensure that they are satisfying the needs of those users. Common user contributions include (but are not limited to):

- evangelising about the project (e.g. a link on a website and word-of-mouth awareness raising)
- informing developers of strengths and weaknesses from a new user perspective
- providing moral support
- providing financial support

Users who continue to engage with the project and its community will often become more and more involved. Such users may find themselves becoming contributors, as described in the above section.

## Approving PRs

Unless otherwise requested by Maintainers, PRs may be merged after receiving at least two approvals from Reviewers or higer roles.

## Decision making and voting

Ideally, all project decisions are resolved by consensus via a PR or GitHub issue. If this is not possible, Maintainers may call a vote. Many of the day-to-day project maintenance can be done by a [lazy consensus](http://communitymgt.wikia.com/wiki/Lazy_consensus) model. But the following items must be called to vote:

- Enforcing a Code of Conduct violation (super majority)
- Adding or removing a maintainer/committer/SIG Leads (super majority)
- Changing the governance rules in this document (super majority)
- Licensing and intellectual property changes (including new logos, wordmarks) (simple majority)
- Adding, archiving, or removing SIG/subproject (simple majority)
- Other cases where consensus cannot be made (super majority)

For formal votes, a specific statement of what is being voted on should be added to the relevant github issue or PR, and a link to that issue or PR added to the maintainers meeting agenda document. Maintainers should indicate their yes/no vote on that issue or PR, and after a suitable period of time, the votes will be tallied and the outcome noted.

Voting must comply with the [Guiding Principles](/guiding-principles.md) and [CNCF Code of Conduct](https://github.com/tikv/tikv/blob/master/CODE_OF_CONDUCT.md).

### Proposal process

We use a [Request for Comments (RFC) process for any substantial changes to TiKV. This process involves an upfront design that will provide increased visibility to the community. If you're considering a PR that will bring in a new feature that may affect how TiKV is implemented, or may be a breaking change, then you should start with a RFC. We've got the process documented in [RFC repository](https://github.com/tikv/rfcs) and have a [template](https://github.com/tikv/rfcs/blob/master/template.md) for you to get started.

## Adding new projects

New projects can be added to the TiKV organization via GitHub issue discussion in one of the existing SIG, as long as as they adheres to the [CNCF charter](https://www.cncf.io/about/charter/) and the guidelines in this governance. Once sufficient discussions have taken place, the Maintainers will decide whether the new project should be added. The requester needs to create an corresponding RFC for the change to happen, as described in [Decision Making and Voting](#decision-making-and-voting).
