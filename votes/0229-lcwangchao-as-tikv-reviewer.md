# A Vote for lcwangchao as TiKV Reviewer

## Proposal

[@lcwangchao](https://github.com/lcwangchao) has been working on `tikv/tikv` for about one year, and contributed extensively to TiKV's coprocessor and transaction components, focusing on index lookup pushdown, coprocessor enhancements, transaction debugging, and other critical improvements.

The following lists the details of [@lcwangchao](https://github.com/lcwangchao)'s contributions:

- [16+ authored pull requests](https://github.com/tikv/tikv/pulls?q=is%3Apr+author%3Alcwangchao+)
- Multiple merged PRs including significant features and enhancements

Key areas of contribution include:

**Coprocessor Enhancements:**
- Implemented IndexLookUp pushdown functionality, including `BatchIndexLookUpExecutor` to perform index lookup on TiKV side (PR #18869, #18943)
- Added support for IndexLookUp in `BatchExecutorsRunner` (PR #18943)
- Added `RegionStorageAccessor` to provide store for secondary regions in cop-task (PR #18813)
- Added SQL statement tracing in TiKV slow log (PR #15514)

**Transaction Improvements:**
- Enhanced transaction error handling with MVCC collection for `CommitTsExpired` errors (PR #18442)
- Improved transaction debugging by collecting MVCC for `TxnLockNotFound` errors when commit secondary failed (PR #18426)
- Added debug info for errors when commit_role is unknown (PR #18448)

His contributions demonstrate deep understanding of TiKV's coprocessor architecture and transaction mechanisms, with a focus on performance optimization and observability improvements. The quality and scope of his work make him an excellent candidate for the TiKV reviewer role.

I hereby nominate [@lcwangchao](https://github.com/lcwangchao) as TiKV reviewer and call for a vote.

## Deadline

The vote will be open for at least 3 days unless there is an objection or not enough votes.

## Result
Approved by 1 binding votes, 2 non-binding votes.
* cfzjywxk (binding)
* ekexium (no-binding)
* MyonKeminta (no-binding)
