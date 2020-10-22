# Transaction SIG Charter

This charter follows the TiKV Community charter and system, using the role definitions and responsibilities in [SIG Governance](/ GOVERNANCE.md).

## Responsibility

The main responsibility of Transaction SIG is to discuss and plan the future development of TiKV distributed transactions, and organize community members to carry out related development and maintenance. The scope of work includes the optimization of existing transaction model and the discussion of new transaction model. Only members of the Active Contributor or higher community can become members of the SIG and participate in relevant matters, but the decisions and projects implemented by the SIG will be made public.

## Work content

- Code range
  -[storage](https://github.com/tikv/tikv/tree/master/src/storage): TiKV distributed transaction implementation;
  -[gc_worker](https://github.com/tikv/tikv/tree/master/src/server/gc_worker): expired version recovery mechanism;
  -[pessimistic lock manager](https://github.com/tikv/tikv/tree/master/src/server/lock_manager): Pessimistic lock deadlock detection.

- Test Specification
  - Submit code to include necessary unit tests. Make sure all CIs pass before merging the code.
  - For changes that affect performance, provide the necessary performance test results.

- Design and Evolution Proposal
- Review related project code

## Other regulatory processes

- Code style, submission specifications, PR Description template, etc. please refer to [Document](https://github.com/tikv/tikv/blob/master/CONTRIBUTING.md)
- Task Assignment
  - Tech Lead maintains public [Member List](https://tikv.github.io/members/build/index.html?name=transaction) and [Task List](https://github.com/tikv/tikv/projects/28) Link.
  - New SIG members can freely receive tasks, or participate in the development or promotion of existing tasks, but need to communicate and synchronize with the Tech Lead or the person responsible for the corresponding task.
  - SIG members are required to maintain monthly participation in development tasks or to participate in the design and discussion of existing features or future plans. If you do not participate in development and discussion for a quarter of a year, it is considered inactive and SIG will be removed as appropriate.

- Regular sync progress, regular weekly meetings
  - Synchronize the current development progress of each project as a document every 2 weeks.
  - A progress meeting for the entire group will be held every 2 weeks, and the time will be negotiated separately based on the available time of the participants. Members who are not currently developing a project can choose to participate in order to know the progress of each project. If members participating in the development are not able to participate, they need to take leave in advance and update their monthly progress to the document in advance.
  - Minutes of each meeting are recorded by one member, which is completed and made public within 24 hours after the meeting ends. The minutes of the meeting are performed in turn by the members of the group.
  - Slack: [tikv-wg.slack.com](https://join.slack.com/t/tikv-wg/shared_invite/enQtNTUyODE4ODU2MzI0LWVlMWMzMDkyNWE5ZjY1ODAzMWYZWYZWYZWYWJGWYG) #transaction-sig

- Organize events for online and offline members
- Additional responsibilities for Tech Leads
  - Questions from SIG members need to respond within 2 business days
  - Review design documents and code in a timely manner
  - Schedule tasks (if SIG member exits, unfinished tasks need to be reassigned)

## SIG Active Rules, Promotion Mechanism

- Assessment & Promotion System
  - Tech Lead evaluates group members on a monthly basis to determine whether members can be promoted to Reviewer from Active Contributor:
    - Familiar with the code base
    - Nominated by at least 2 Committers
    - PR contributions meet any of the following:
      - Merged transaction-related PRs totaled more than 10
      - Propose design ideas and adopt them into more than 3 tasks

  - Tech Lead and Maintainers evaluate team members on a quarterly basis to determine whether members can be promoted to Committer from Reviewer:
    - Show good technical judgment
    - Nominated by at least 2 Maintainers
    - PR contributions meet at least two of the following:
      - Complete an important feature independently or lead
      - Fix a major bug
      - The total number of PR related to valid Review Transaction exceeds 10
      - The total number of valid PR related PR rows exceeds 2000

- Promotion Role Rights & Obligations
  - Reviewer
    - Participate in project design decisions
    - Participate in transaction related PR review and quality control
    - Valid Approve / Request Change permissions for transaction related PR

  - Committer
    - Owning the rights and obligations of Reviewer
    - Control the overall code quality of the project
    - Guide Contributor and Reviewer

- Exit
  - SIG members are removed from SIG in the following cases, but retain the corresponding Active Contributor / Reviewer / Committer status:
    - Inactive for one consecutive quarter

  - Reviewer will be revoked and revoked if one of the following conditions is met:
    - No review of any transaction related PR for more than a quarter
    - 2 or more Committers consider Reviewer insufficient or active
