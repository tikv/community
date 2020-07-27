# Transaction Special Interest Group

> SIG Repository: https://github.com/tikv/sig-transaction (Most useful resource, contains lots of information about the SIG and transactions)

The transactions special interest group (SIG-transaction) are a group of people interested in transactions in distributed databases. We have a focus on transactions in TiKV and TiDB, but discuss academic work and other implementations too.

The SIG is in the process of starting up and currently does not have any official activity. In the near future we hope to host:

* talks on distributed transactions,
* a reading group for academic papers,
* discussion of transaction research and implementations on Slack,
* help understanding and configuring transactions in TiKV and TiDB,
* support for contributors to TiKV and related projects.

## Contributing

You can join us in #sig-transaction in the [TiKV community Slack](https://slack.tidb.io/invite?team=tikv-wg&channel=sig-transaction&ref=community-sig); come say hi! We use English or Chinese.

You can read or join our announcement [mailing list](https://groups.google.com/d/forum/tikv-sig-transaction), so you can stay up to date with what we're up to.

If you would like to join the SIG or have any questions about it, please email sig-txn@tikv.dev.

## Roles and Organization Management

- [SIG Transaction Constitution](./constitution.md).
- [SIG Transaction Constitution(zh-CN)](./constitution-zh_CN.md).

## Members

See [SIG Transaction Member List](./membership.md).

## Meetings

- Regular SIG Meeting:
  - Weekly on Fri 11am, Beijing Time starting from 2020/05/15.
  - [Meeting Notes](https://drive.google.com/drive/folders/15jTHu8Z-ha6RzF3AqcPH59FXthmlNv-Q?usp=sharing)
  - [Meeting Link](https://pingcap.zoom.us/j/5527699243)

## Contact

- Slack: [#sig-transaction](https://slack.tidb.io/invite?team=tikv-wg&channel=sig-transaction&ref=github-sig)

## Repositories, Projects and Labels

- [Transaction issues](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Acomponent%2Ftransaction),
- [sig-transaction issues](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Asig%2Ftransaction),
- [storage issues](https://github.com/tikv/tikv/issues?q=is%3Aopen+is%3Aissue+label%3Acomponent%2Fstorage) (most of these are transaction-related in some way),
- project: [Pipelined pessimistic lock](https://github.com/tikv/tikv/projects/37),
- project: [Large transactions](https://github.com/tikv/tikv/projects/36),
- project: [Green GC](https://github.com/tikv/tikv/projects/35),
- project: [Parallel commit](https://github.com/tikv/tikv/projects/34).

## Code Locations

- [kvproto](https://github.com/pingcap/kvproto) (protocol buffers which support transactions, among other things).
- [Txn module](https://github.com/tikv/tikv/tree/master/src/storage/txn).
- [MVCC module](https://github.com/tikv/tikv/tree/master/src/storage/mvcc).
