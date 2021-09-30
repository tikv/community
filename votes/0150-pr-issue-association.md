# A Vote for PR Issue Association

* Discussion at https://github.com/tikv/community/pull/150
* Tracking issue https://github.com/tikv/community/issues/149

## Proposal

### Motivation

To measure software evolution, we focus on features implemented, bugs fixed, and general enhancement. Issues document these items, while a pull request focuses on the change set and whether we implement it correctly.

Normally, an issue documents a work item, and a pull request resolves it (despite cherry-picks). However, the relation between pull requests and issues is complicated in TiDB projects.

* 1 issue with 0 PRs: question, bug vanished without a reason, etc. 
* 1 issue with 1 PR: normal case. 
* 1 issue with n PRs: resolve a bug multiple times ([1](https://github.com/pingcap/tidb/issues/24679)), or resolve a complex issue in steps([2](https://github.com/pingcap/tidb/issues/27652)).
* n issues with 1 PR: trade off resolving things as a whole (due to code coupling, or we can resolve multiple bugs at the common parent level) ([3](https://github.com/pingcap/tidb/pull/27697)), duplicated issues. 
* 0 issue with 1 PR: coding without a ticket ([4](https://github.com/pingcap/tidb/pull/23022)). Even if the description is detailed or even if a design document is present, pull requests focus on the change set. It is about the implementation, not the question; if it is, we always mix discussion because the change set has a primary position. 

### Solution

Previous discussion happened on the [developer discussion forum](https://internals.tidb.io/t/topic/409).

I propose to check that a pull request must be associated with issue(s).

In details:

* A pull request MUST be associated with issue(s) in commit messages. That is, the change set by `git commit` with a message mention `ref #{issue-number}` or `close #{issue-number}` or semantic equivalent.
* A pull request SHOULD be with a description mention the issue(s) associated, so that reviewers are able to get the information directly.

For the first point, we will develop a checker to guard the condition. For the second point, the PR template has already contained such entry.

However, it's more about development practices than rules. So our committers are the effective guardians.

### Implementation Plan

@Mini256 will develop a checker based on [tichi](https://github.com/ti-community-infra/tichi) implementing rules above.

### Alternative

To ensure PR issue association, we can also check the reference in PR title or PR description. Both are discussed and rejected in the thread on the [developer discussion forum](https://internals.tidb.io/t/topic/409).

## Deadline

The vote will be open for at least 144 hours unless there is an objection or not enough votes.

We're looking for at least 2 votes from tikv-maintainers, and 2 votes from pd-maintainers.

## Result

Conclude the voting result, including approvals and vetoes, binding and non-binding.
