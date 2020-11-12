# Coprocessor SIG Charter

This charter follows the TiKV Community Charter, using the role definitions and responsibilities in [SIG Governance](/GOVERNANCE.md).

## Scope

Coprocessor SIG focuses on the Coprocessor module of the TiKV project, which is the module in TiKV that handles TiDB's pushdown calculations. The primary responsibility of this SIG is to discuss, plan, develop, and maintain the future development of the Coprocessor module. Only Active Contributors or higher-level community members can become members of the SIG and participate in SIG activities. However, the decisions and projects undertaken by the Coprocessor SIG will be made public.

## Routine Work

- Code
  - Framework: Framework improvements, including expression calculation frameworks, executor execution frameworks, etc.
  - Executor: Improve existing executors and collaborate with TiDB to develop new executors.
  - Function: Maintain an existing or port a new built-in function / aggregate function implementation from TiDB.
  - Location: [tidb_query](https://github.com/tikv/tikv/tree/master/components/tidb_query).

- Test
  - The code needs to pass existing integration tests, and new changes need to be added to [copr-test](https://github.com/tikv/copr-test) to add new integration tests.
  - The function ported from the TiDB needs unit tests.
  - Expression's integration test requires a test that uses this expression.

- Design proposals
- Review code

## Other

- For code style, submission specification, PR description template, etc, please refer to [Documentation](https://github.com/tikv/tikv/blob/master/CONTRIBUTING.md)

- Task Assignment
  - SIG Tech Lead maintains a public [Member List](https://pingcap.com/developer/sig/coprocessor) and [Task List](./workflow-zh_CN.md) at https://github.com/tikv/community.
  - New SIG members have 2 weeks to learn about tasks and claim a task, or participate in the development of an existing task. If the task is not claimed within this time, the member will be removed from SIG.
  - SIG members are required to engage development each month, or participate in the design or discussion of existing features or future design. If a member does not participate in code development or future discussion for one quarter, he / she will be considered inactive and will be removed from the SIG. However as an acknowledgment, the name will be stay in the "Former Member" of the member list.

- Regularly synchronize
  - Synchronize the development progress of current projects every 2 weeks.
  - A full group progress meeting will be held every 2 weeks, depending on the available time of the participants. Members who are currently not developing a project are also eligible to participate in order to know the progress of each project. If members are unable to participate, he / she must apply for leave in advance and update the progress document.
  - A meeting is recorded by one member each time. Meeting notes are completed and made public within 24 hours of the end of the meeting. The meeting notes are recorded by the team members in turn.
  - Slack: https://tikv-wg.slack.com #copr-sig-china

- Organize offline activities

- Tech Leads additional responsibilities
  - Questions from SIG member need to be answered within 2 business days
  - Review code timely
  - Publish tasks (unfinished tasks need to be reassigned if SIG member exits)

## Promtion

- Assessment & Promotion
  - Tech Leaders evaluate team members on a monthly basis to determine whether they can be promoted from Active Contributor to Reviewer, based on the following aspects:
    - Familiar with the code base
    - Nominated by at least 2 TiKV Committers
    - PR contributions meet any of the following:
      - More than 10 merged Coprocessor PRs
      - Merged Coprocessor PRs involve more than 1000 lines of code
      - Finished at least one task with a difficulty of Medium or above
      - Presented design ideas and adopted them in more than 3 executable tasks

  - Tech Leaders and TiKV Maintainers evaluate team members on a quarterly basis to determine whether they can be promoted from Reviewer to Committer, based on the following aspects:
    - Exhibited good technical judgment
    - Nominated by at least 2 TiKV Maintainers
    - Complete at least two tasks of Medium difficulty level or one of High difficulty level
    - The PR contribution meets at least two points:
      - Merged Coprocessor PRs involve more than 1500 lines of code within half a year
      - Valid Coprocessor PR reviews total over 10
      - Valid Coprocessor PR reviews involve over 1000 lines of code

- Rights and Obligations
  - Reviewer
    - Participate in project design decisions
    - Participate in Coprocessor PR reviews and the quality control process
    - Approval / Request Change permissions on PRs of the Coprocessor module

  - Committer
    - Inherit the rights and obligations of Reviewer
    - Ensure overall code quality of the project
    - Guide contributors and reviewers

- Quit
  - Coprocessor SIG members will be removed from the SIG in the following cases (corresponding Active Contributor / Reviewer / Committer roles will be retained):
    - As a new member, not claimed any task within the specified time
    - Inactive for one quarter

  - Reviewer role will be withdrawn in any of the following cases (can be recovered after re-assessment):
    - No reviews for more than one quarter for Coprocessor related PRs
    - More than 2 committers agree that the reviewer is not capable or active enough
