# A Vote for lcwangchao as TiKV Committer

## Proposal

[@lcwangchao](https://github.com/lcwangchao) has continuously contributed to TiKV team repositories (`tikv/tikv` and `tikv/client-go`), particularly in coprocessor pushdown, transaction lock resolution, `commit_ts` support, and multi-branch release maintenance. Since becoming a [TiKV Reviewer](./0229-lcwangchao-as-tikv-reviewer.md), he has continued to deliver core features, bug fixes, and code reviews across both repositories.

As of November 26, 2026, his contributions across TiKV repositories include:

* [26 merged pull requests in `tikv/tikv`](https://github.com/tikv/tikv/pulls?q=is%3Apr+is%3Amerged+author%3Alcwangchao)
* [34 merged pull requests in `tikv/client-go`](https://github.com/tikv/client-go/pulls?q=is%3Apr+is%3Amerged+author%3Alcwangchao)
* [88 reviewed pull requests across `tikv` repositories](https://github.com/search?q=org%3Atikv+is%3Apr+reviewed-by%3Alcwangchao+-author%3Alcwangchao&type=pullrequests)

Representative contributions include:

* **TiKV Coprocessor & Storage (`tikv/tikv`)**:
  * Implemented IndexLookUp pushdown and common-handle support (`#18869`, `#18943`, `#19159`, `#19160`) and fixed local lookup range boundaries and TopN handle keys (`#19173`, `#19216`).
  * Implemented returning `commit_ts` for `Get` / `BatchGet` / Coprocessor and `need_commit_ts` for `batch_get_command` (`#19230`, `#19295`, `#19301`), and fixed `Op_Lock` `commit_ts` handling and `_tidb_commit_ts` column ordering panics (`#19300`, `#19374`, `#19394`).
* **Transaction & Lock Resolution (`tikv/client-go`)**:
  * Designed and optimized async and batched lite lock resolution on the read path, including key deduplication, goroutine/memory reduction, and backoff handling (`#1940`, `#1973`, `#1981`, `#2047`, `#2075`, `#2136`).
  * Added keyspace ID propagation in gRPC metadata (`#2129`), `SetCommitWaitUntilTSOTimeout` support (`#1875`, `#1876`), `WithReturnCommitTS` checks (`#1861`, `#1864`), and snapshot runtime/scan detail observability (`#2025`, `#2140`).

I ([@ekexium](https://github.com/ekexium)) hereby nominate [@lcwangchao](https://github.com/lcwangchao) as TiKV Committer and call for a vote.

## Deadline

The vote will be open for at least 6 days and remain open if there are not enough votes. Per [TiKV Governance](../GOVERNANCE.md#approvals), approval requires consensus: at least 2 binding +1 votes from active TiKV maintainers and no binding vetoes.

## Result
