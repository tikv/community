# A Vote for YuhaoZhang00 as PD Reviewer

## Proposal

[@YuhaoZhang00](https://github.com/YuhaoZhang00) has continuously contributed to `tikv/pd` since March 2026, focusing on the resource control (RC) subsystem, TSO, and the PD election and leader-lease path. The main contributions are listed in the following:

* [Authored pull requests in PD](https://github.com/tikv/pd/pulls?q=is%3Apr+author%3AYuhaoZhang00)
* [Reviewed pull requests in PD](https://github.com/tikv/pd/pulls?q=is%3Apr+reviewed-by%3AYuhaoZhang00)
* [Authored pull requests in TiKV repositories](https://github.com/search?q=org%3Atikv+is%3Apr+author%3AYuhaoZhang00&type=pullrequests)
* [Reviewed pull requests in TiKV repositories](https://github.com/search?q=org%3Atikv+is%3Apr+reviewed-by%3AYuhaoZhang00&type=pullrequests)
* [Authored pull requests in TiDB](https://github.com/pingcap/tidb/pulls?q=is%3Apr+author%3AYuhaoZhang00)
* [Reviewed pull requests in TiDB](https://github.com/pingcap/tidb/pulls?q=is%3Apr+reviewed-by%3AYuhaoZhang00)

The main work in `tikv/pd` is listed below:

* [client/resource_group: add RC paging pre-charge with PredictedReadBytes hint](https://github.com/tikv/pd/pull/10611)
* [resource_group/controller: keep lim.last monotonic on token updates](https://github.com/tikv/pd/pull/10745)
* [client/resource_group: expose RU consumption by request source](https://github.com/tikv/pd/pull/10588)
* [server/resource_group: add allocation observability](https://github.com/tikv/pd/pull/10867)
* [client/resource_group: add client-side demand observability](https://github.com/tikv/pd/pull/10866)
* [tso, server: add debug logs for TSO sync, closure, and forwarding paths](https://github.com/tikv/pd/pull/10439)
* [server, member, election: document and test the election client pinning](https://github.com/tikv/pd/pull/11110)

His resource control work is not confined to a single repository. He drove the matching changes across the whole stack for the RC paging pre-charge feature, so that a read-bytes prediction is carried end to end:

* [store/copr: add RC paging pre-charge EMA and PredictedReadBytes hint](https://github.com/pingcap/tidb/pull/67941)
* [resourcecontrol, tikvrpc: add PredictedReadBytes hint for RC paging pre-charge](https://github.com/tikv/client-go/pull/1947)

He also reviewed the adjacent pieces of the same feature that were owned by others, such as [proto: add paging_size_bytes to coprocessor.Request](https://github.com/pingcap/kvproto/pull/1448) and [coprocessor: support paging_size_bytes for byte-budget paging](https://github.com/tikv/tikv/pull/19510).

He also identifies and reports the problems he later fixes. Among the 13 issues he filed in the TiKV organization, several became the design records for the changes above, for example [pd#10612](https://github.com/tikv/pd/issues/10612), [pd#10744](https://github.com/tikv/pd/issues/10744), and [pd#11106](https://github.com/tikv/pd/issues/11106).

Since his first contribution in March 2026, he has opened 50 pull requests (15 merged, +7,756/-480 across 105 files), filed 13 issues, and submitted 122 reviews on 63 pull requests. 97 of those reviews and 49 of those pull requests are in `tikv/pd` alone, and he submitted at least 10 reviews in every month from March to September 2026, which shows a sustained reviewing habit rather than a one-off burst.

This consistent and sustained record across the PD resource control, TSO, and election areas makes [@YuhaoZhang00](https://github.com/YuhaoZhang00) a good candidate for the PD reviewer role.

I ([@JmPotato](https://github.com/JmPotato)) hereby nominate [@YuhaoZhang00](https://github.com/YuhaoZhang00) as PD Reviewer and call for a vote.

## Deadline

The vote will be open for at least 3 days unless there is an objection or not enough votes.

## Result

Approved on September 14, 2026, with 2 binding +1 votes, 1 non-binding +1 vote, and no negative votes, after the minimum 3-day voting period.

* [rleungx](https://github.com/tikv/community/pull/239#pullrequestreview-5164071648) (binding)
* [nolouch](https://github.com/tikv/community/pull/239#pullrequestreview-5193828769) (binding)
* [bufferflies](https://github.com/tikv/community/pull/239#pullrequestreview-5162687019) (non-binding)

The vote passes under the Lazy Majority rule for a new reviewer.
