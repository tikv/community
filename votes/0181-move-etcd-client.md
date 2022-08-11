# A Vote for moving `etcd-client` to tikv org

## Proposal

The package `backup-stream` in TiKV relies the `etcd-v3/etcd-client` for reading / putting metadata of PiTR backups. 

For solving the issue [#13251](https://github.com/tikv/tikv/issues/13251), we forked the repository to [here](https://github.com/yujuncen/etcd-client) and applied some patches.

We may need to maintain the repository for a long time because:
- The origin author has upgraded `tokio` and some other requirements to newer version, we cannot upgrade this library directly without upgrading them.
- We may need to develop a `grpc-rs` backend (as an alternative of `tonic`) for this client so we don't need to compile both `tonic` and `grpc-rs` at the same time.

I hereby start a vote for moving the repository https://github.com/yujuncen/etcd-client (Maybe already have been moved to https://github.com/pingcap/etcd-client) to the tikv community.

## Deadline

The vote will be open for at least 6 days unless there is an objection or not enough votes.

## Result

Approved by: