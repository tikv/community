# SIG Governance

The full name of SIG is Special Interest Group. Please refer to [Community Organization](/GOVERNANCE.md#developer-group-structure). SIGs mainly aggregate a group of Active Contributors, and conducts in-depth research & contributions to one or more TiKV modules, and is promoted to Reviewer, Committer within the SIG.

## SIG Role and Organizational Governance

The SIG follows the role definitions in the [GOVERNANCE](/GOVERNANCE.md). The SIG is subject to the following rules:

- Before starting a SIG, the charter will be established in advance. Please refer [Create the SIG charter](#create-the-sig-charter) to create the charter
- Except for holidays, the regular meeting is organized at least once every two weeks.
- The assignable tasks will be graded by difficulty levels and claimed by SIG members.

Please refer to [SIG Lifecycle](#sig-lifecycle) for other issue.

## SIG Roles

### SIG Members

- Inludes all Active Contributors, Reviewers, and Committers under the SIG
- SHOULD maintain health of the SIG
- SHOULD show sustained contributions to the SIG
- SHOULD hold corresponding responsibilities in the SIG as documented in [Community Membership](/community-membership.md)
- MAY participate in decision making of the SIG

### Tech Lead

  - **Number**: 2-3. Initially assigned by Maintainers
  - **Requirement**:
    - MUST be a committer from the specific SIG
    - MUST have demonstrated deep understanding of the SIG project
  - **Term**: 1 year
  - **Election:**
      - Nominated by the Tech Leads or self-nominate
      - Gained supermajority votes of Maintainers
- **Responsibilities**
    - Creating new projects under the SIG
    - Triaging issues/tasks in the SIG
    - Mentoring members of the SIG
    - Organizing discussions and drawing conclusions for decision making within the SIG
    - Ensuring health and sustained development of the SIG and grwoth of SIG members
    - Making roadmap for the SIG
    - Organizing and participating in regular meetings

## Member Promotion Mechanism

Members of the SIG can be promoted to a higher role based on the rules defined in [Community Membership](/community-membership.md).

## Member Exit Mechanism

There are two exit situations:

- Members MAY decide to step down at anytime for personal reasons by opening the PR to modify the [`membership.md`](./membership.md) file. The PR can be merged once it gets two approvals from the higher role.

- Members of a role SHOULD be removed of the SIG if they have not communicated a leave of absence and either cannot be reached for more than 1 month or are not fulfilling their documented responsibilities for more than 1 month. Tech Leads will assess the communication and contributions monthly to update the membership list. Each change (removal) in such case should be gained supermajority approval among Maintainers + Tech Leads.

## Create the SIG Charter

1. Copy the [SIG Charter Template](SIG-CHARTER-TEMPLATE.md)
2. Modify the content in the template that needs to be defined for the specific SIG
3. Initiate a PR to [TiKV Community](https://github.com/tikv/community) with the SIG Charter, and propose the SIG Charter to [SIGs log](/sig)
4. The new SIG will be announced by the community committee after approval.

## SIG Lifecycle

### Creation

1. All SIG Technical Leads and other roles need to be at least [Active Contributor](#active_contributor) in the Community structure

2. Follow the steps above to [Create the SIG charter](#Create-the-SIG-charter)

3. Create a public and private Slack Channel in tikv-wg.slack.com to discuss the SIG operation related matters

4. Create a Zoom room for regular meetings, as well as other online discussions

5. Announce the establishment of a new SIG in the TiKV community

### Dissolution

Sometimes a SIG may need to be dismissed or merged. The SIG's dissolution rules should be defined by the specific SIG.