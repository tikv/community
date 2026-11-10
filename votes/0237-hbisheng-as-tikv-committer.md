# A Vote for hbisheng as TiKV Committer

## Proposal

[@hbisheng](https://github.com/hbisheng) (Bisheng Huang) has continuously contributed to `tikv/tikv`, particularly raftstore, snapshot handling, flow control, resolved-ts, and production diagnostics. Since his [nomination as TiKV Reviewer](https://github.com/tikv/community/pull/222) was merged in October 2024, he has continued to deliver fixes, investigate issues, and review other contributors' changes in these areas.

As of November 10, 2026, his contributions in `tikv/tikv` include:

* [36 authored pull requests since October 15, 2024](https://github.com/tikv/tikv/pulls?q=is%3Apr+author%3Ahbisheng+created%3A2024-10-15..2026-11-10), of which [29 have been merged](https://github.com/tikv/tikv/pulls?q=is%3Apr+is%3Amerged+author%3Ahbisheng+created%3A2024-10-15..2026-11-10).
* [27 authored issues in the same period](https://github.com/tikv/tikv/issues?q=is%3Aissue+author%3Ahbisheng+created%3A2024-10-15..2026-11-10), covering bug reports, reproductions, and improvement proposals.
* [236 distinct pull requests by other authors reviewed across his full contribution history](https://github.com/tikv/tikv/pulls?q=is%3Apr+reviewed-by%3Ahbisheng+-author%3Ahbisheng+created%3A%3C2026-11-11).

The PR counts include release backports as separate PRs. The review count excludes his own PRs and counts PRs rather than individual review submissions; it is not limited to his reviewer tenure.

### Code contributions as a reviewer

Representative merged PRs since his reviewer nomination include:

* **Raftstore and snapshot reliability:** [#17903](https://github.com/tikv/tikv/pull/17903) fixes the ordering of snapshot receive accounting and precheck resource release; [#18032](https://github.com/tikv/tikv/pull/18032) fixes missing pending peers in region heartbeats after a split; [#19936](https://github.com/tikv/tikv/pull/19936) batches store-to-peer notifications to reduce long raftstore stalls when many stores become unreachable.
* **Availability and operational readiness:** [#19613](https://github.com/tikv/tikv/pull/19613) adds disk-hang fail-fast detection, including independent probe/check workers and diagnostics; [#18237](https://github.com/tikv/tikv/pull/18237) adds the `/ready` endpoint for checking readiness after startup.
* **Flow control and region sizing:** [#18787](https://github.com/tikv/tikv/pull/18787) restores flow control after an unsafe destroy range on an empty cluster; [#19716](https://github.com/tikv/tikv/pull/19716) handles transient pending-compaction-byte spikes during RocksDB base-level transitions; [#18628](https://github.com/tikv/tikv/pull/18628) estimates Titan raw blob size using compression metrics to address region size underestimation without changing the blob index format.
* **Resolved-ts and observability:** [#20029](https://github.com/tikv/tikv/pull/20029) fixes region metadata updates overwriting cached leader state, with a regression test for stalled resolved-ts progress; [#18075](https://github.com/tikv/tikv/pull/18075) adds thread-local panic context; [#19178](https://github.com/tikv/tikv/pull/19178) improves coprocessor suspend-time and semaphore-wait observability.
* **Security maintenance:** [#20324](https://github.com/tikv/tikv/pull/20324) enables log redaction by default, and [#20353](https://github.com/tikv/tikv/pull/20353) updates `libz-sys` for a RustSec advisory.

### Issue investigation and follow-through

His issue contributions include reporting symptoms with evidence, supplying reproductions, proposing fixes, and reviewing subsequent implementations:

* **Resolved-ts memory growth:** In [#18359](https://github.com/tikv/tikv/issues/18359), he reported pending-task memory growth when the resolved-ts worker stalls and [provided a local reproduction with fault injection and workload steps](https://github.com/tikv/tikv/issues/18359#issuecomment-2785883458). He subsequently reviewed the memory-quota fix in [#19294](https://github.com/tikv/tikv/pull/19294).
* **Flow-control failures:** He reported flow control remaining disabled after unsafe destroy range in [#18728](https://github.com/tikv/tikv/issues/18728) and implemented the fix in [#18787](https://github.com/tikv/tikv/pull/18787). He also documented compaction-estimate spikes during base-level transitions in [#19667](https://github.com/tikv/tikv/issues/19667), followed by [#19716](https://github.com/tikv/tikv/pull/19716).
* **Region sizing and snapshot handling:** He supplied a compressible-data reproduction and analysis for Titan region size underestimation in [#18600](https://github.com/tikv/tikv/issues/18600), followed by [#18628](https://github.com/tikv/tikv/pull/18628). His snapshot-precheck report in [#17881](https://github.com/tikv/tikv/issues/17881) was followed by the resource-release fix in [#17903](https://github.com/tikv/tikv/pull/17903).
* **Recovery and liveness:** He reported peers stuck in busy apply after startup in [#18233](https://github.com/tikv/tikv/issues/18233) and reviewed follow-up fixes, including [#19199](https://github.com/tikv/tikv/pull/19199). He also proposed disk-hang fail-fast handling in [#19626](https://github.com/tikv/tikv/issues/19626) and bounded unreachable-store broadcasts in [#19666](https://github.com/tikv/tikv/issues/19666), then implemented [#19613](https://github.com/tikv/tikv/pull/19613) and [#19936](https://github.com/tikv/tikv/pull/19936).

### Code review contributions

Representative reviews demonstrate attention to correctness, failure handling, and regression coverage:

* In [#19798](https://github.com/tikv/tikv/pull/19798), he [identified that a Tokio timeout could panic on TiKV's non-Tokio executors](https://github.com/tikv/tikv/pull/19798#discussion_r3726908506), requested executor-appropriate tests, and [explained why snapshot acquisition must preserve the request's existing deadline](https://github.com/tikv/tikv/pull/19798#discussion_r3755067919) instead of restarting its timeout budget.
* In [#19294](https://github.com/tikv/tikv/pull/19294), he [flagged memory-quota cleanup on the task scheduling failure path](https://github.com/tikv/tikv/pull/19294#discussion_r2707090232) while reviewing the resolved-ts OOM fix.
* In [#18439](https://github.com/tikv/tikv/pull/18439), he discussed the sensitivity/false-positive trade-off in KV disk jitter detection and [identified interval validation that could otherwise allow a zero derived interval](https://github.com/tikv/tikv/pull/18439#discussion_r2099176520).

These contributions demonstrate sustained ownership of TiKV reliability and the ability to support other contributors through investigation and review.

I ([@LykxSassinator](https://github.com/LykxSassinator)) hereby nominate [@hbisheng](https://github.com/hbisheng) as TiKV Committer and call for a vote.

## Deadline

The vote will be open for at least 6 days and remain open if there are not enough votes. Per [TiKV Governance](../GOVERNANCE.md#approvals), approval requires consensus: at least 2 binding +1 votes from active TiKV maintainers and no binding vetoes.

## Result
