# Scheduling SIG Bylaws

This charter follows the TiKV Community charter and system, using the role definitions and responsibilities in [SIG Governance](/GOVERNANCE.md).

## Responsibility

The main responsibility of Scheduling SIG is to work on the development of the scheduling system [pd](https://github.com/tikv/pd) through optimizing the scheduling algorithm and implementation, and organize the community Members carry out related development and maintenance. Only members of the Active Contributor or higher community can become members of the SIG and participate in relevant matters, but the decisions and projects implemented by the SIG will be made public.

## Work content

- Code
  - [pd](https://github.com/tikv/pd): Implementation of scheduling.
  - [pd_client](https://github.com/tikv/tikv/tree/master/components/pd_client): Implementation of PD client.

- Test Specification
  - Submit code to include necessary unit tests. Make sure all CIs pass before merging the code.
  - For changes that affect performance, provide the necessary performance test results.

- Design and Evolution Proposal
- Review related project code

## Other regulatory processes

- Code style, submission specifications, PR Description template, etc. please refer to [Document](https://github.com/tikv/pd/blob/master/CONTRIBUTING.md)
- Task Assignment
  - SIG Tech Lead maintains public [Member List](https://tikv.github.io/members/build/index.html?name=scheduling) and [Task List](https://github.com/tikv/pd/projects/5) Link.
  - New SIG members can freely receive tasks, or participate in the development or promotion of existing tasks, but need to communicate and synchronize with the Tech Lead or the person responsible for the corresponding task.
  - SIG members are required to maintain monthly participation in development tasks or to participate in the design and discussion of existing features or future plans. If you do not participate in development and discussion for a quarter of a year, it is considered inactive and SIG will be removed as appropriate.

- Regular sync progress, regular weekly meetings
  - Synchronize the current development progress of each project as a document every 2 weeks.
  - Slack: [#sig-scheduling](https://slack.tidb.io/invite?team=tikv-wg&channel=sig-scheduling&ref=pingcap-community)

- Organize events for online and offline members
- Additional responsibilities for Tech Leads
  - Questions from SIG members need to respond within 2 business days
  - Review design documents and code in a timely manner
  - Schedule tasks (if SIG member exits, unfinished tasks need to be reassigned)

## SIG Active Rules, Promotion Mechanism

- Assessment & Promotion System
  - Tech Leader evaluates group members on a monthly basis to determine whether members can be promoted to Active Contributor from Contributor:
    - Nominated by at least 2 TiKV Reviewers
    - PR contributions meet the following condition:
      - Combined PD-related PR totals over 8 in a year

  - Tech Leader evaluates group members on a monthly basis to determine whether members can be promoted to Reviewer from Active Contributor:
    - Nominated by at least 2 TiKV Committers
    - PR contributions meet any of the following:
      - Combined PD-related PR totals over 20
      - Finish at least one important issue

  - Tech Leader and TiKV Maintainer evaluate team members on a quarterly basis to determine whether members can be promoted to Committer from Reviewer:
    - Nominated for at least 2 TiKV Maintainers
    - PR contributions meet at least two of the following:
      - Complete two important features independently or lead
      - Fix a major bug
      - More than 20 total review PD related PRs
      - Combined PD-related PR totals over 40

- Promotion Role Rights & Obligations
  - Reviewer
    - Participate in project design decisions
    - Participate in PR review and quality control related to PD
    - Valid Approve / Request Change permissions for PD related PR

  - Committer
    - Owning the rights and obligations of Reviewer
    - Control the overall code quality of the project
    - Guide Contributor and Reviewer

- Exit
  - SIG members are removed from SIG in the following cases, but retain the corresponding Active Contributor / Reviewer / Committer status:
    - Inactive for one consecutive quarter

  - Reviewer will be revoked and revoked if one of the following conditions is met:
    - 2 or more Committers consider Reviewer insufficient or active
