# A Vote for wfxr as TiKV Committer

## Proposal

[@wfxr](https://github.com/wfxr) has continuously contributed to TiKV team repositories (`tikv/client-go`, `tikv/tikv`, and `tikv/pd`), particularly in transaction shared-lock support, API v2 codec handling, GC cleanup, observability, and release/toolchain maintenance. Since becoming a [TiKV Reviewer](./0234-wfxr-as-tikv-reviewer.md), he has actively maintained `tikv/client-go` across `master` and release branches and reviewed PRs across the `tikv` organization.

As of November 26, 2026, his contributions across TiKV repositories include:

* [19 merged pull requests in `tikv/client-go`](https://github.com/tikv/client-go/pulls?q=is%3Apr+is%3Amerged+author%3Awfxr)
* [2 merged pull requests in `tikv/tikv`](https://github.com/tikv/tikv/pulls?q=is%3Apr+is%3Amerged+author%3Awfxr)
* [37 reviewed pull requests across `tikv` repositories](https://github.com/search?q=org%3Atikv+is%3Apr+reviewed-by%3Awfxr+-author%3Awfxr&type=pullrequests)

Representative contributions include:

* **Shared-lock & Transaction / GC (`tikv/client-go`, `tikv/tikv`)**:
  * Implemented shared lock upgrades in `txnkv` ([`tikv/client-go#2014`](https://github.com/tikv/client-go/pull/2014)), fixed empty-primary warnings for shared-lock wrappers ([`#2071`](https://github.com/tikv/client-go/pull/2071), [`#2072`](https://github.com/tikv/client-go/pull/2072)), and checked shared-lock ownership before reporting mismatch in TiKV ([`tikv/tikv#20118`](https://github.com/tikv/tikv/pull/20118)).
  * Completed API v2 key-bearing command coverage and fixed lock key re-encoding ([`tikv/client-go#1987`](https://github.com/tikv/client-go/pull/1987), [`#1997`](https://github.com/tikv/client-go/pull/1997)), removed the standalone GC API ([`#2161`](https://github.com/tikv/client-go/pull/2161)), attached context to lock wait info requests ([`#2006`](https://github.com/tikv/client-go/pull/2006), [`#2009`](https://github.com/tikv/client-go/pull/2009)), and enriched write RPC `scan_detail` ([`tikv/tikv#19325`](https://github.com/tikv/tikv/pull/19325)).
* **Release & CI Maintenance (`tikv/client-go`)**:
  * Maintained Go toolchain upgrades and CI workflows across `master`, `tidb-8.5`, `release-nextgen-202609`, and patch release branches ([`#2089`](https://github.com/tikv/client-go/pull/2089), [`#2121`](https://github.com/tikv/client-go/pull/2121), [`#2122`](https://github.com/tikv/client-go/pull/2122), [`#2124`](https://github.com/tikv/client-go/pull/2124), [`#2125`](https://github.com/tikv/client-go/pull/2125), [`#2154`](https://github.com/tikv/client-go/pull/2154), [`#2155`](https://github.com/tikv/client-go/pull/2155)).

I ([@ekexium](https://github.com/ekexium)) hereby nominate [@wfxr](https://github.com/wfxr) as TiKV Committer and call for a vote.

## Deadline

The vote will be open for at least 6 days and remain open if there are not enough votes. Per [TiKV Governance](../GOVERNANCE.md#approvals), approval requires consensus: at least 2 binding +1 votes from active TiKV maintainers and no binding vetoes.

## Result
