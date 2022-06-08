# New Pull Request Requirement and Commit Message style

Author: @zhangyangyu @Mini256

## Motivation

Currently for `tikv` and `pd` repositories, when a pull request is merged, the final commit message consists of an one-line subject, which is the pull request title, and body. The body rule is complex and messy. When a pull request has multiple commits, the bot uses the GitHub squashed commit message as the final commit message body. And due to the DCO requirement, every commit in the pull request needs to have a DCO signature. The signatures of each commit are also extracted into the final commit message body. A common final commit message now is like:

```
rsmeter: add pubsub datasink  (#11719)

* rsmeter: add pubsub datasink
close #11691

Signed-off-by: Zhenchi <zhongzc_arch@outlook.com>

* fix build

Signed-off-by: Zhenchi <zhongzc_arch@outlook.com>

* Update components/resource_metering/src/reporter/pubsub.rs

Signed-off-by: Zhenchi <zhongzc_arch@outlook.com>

Co-authored-by: Wenxuan <hi@breeswish.org>

* fix build

Signed-off-by: Zhenchi <zhongzc_arch@outlook.com>

Co-authored-by: Wenxuan <hi@breeswish.org>
```

When the pull request contains only one commit, unfortunately, the one-line subject of the commit is lost, since the final commit message uses the pull request title as one-line subject. Only the commit message body remains. An example of this kind is like, note the subject is the pull request title, not the original commit message subject:

```
config: validate online configurable thread pools (tikv#11159) (#11714)

ref #11159

Signed-off-by: Wenbo Zhang <ethercflow@gmail.com>

Co-authored-by: Ti Chi Robot <ti-community-prow-bot@tidb.io>
```

After the [pull request and issue association rule](https://github.com/tikv/community/blob/master/votes/0150-pr-issue-association.md) is applied, the bot will check whether there is a relevant issue number in the final commit body. But due to the commit message rule for one commit pull request, a final commit message like the following example will occur. The necessary issue number is lost since it's in the one-line subject of the only commit.

```
cdc: load uninlined value more effectively (#11615)

Signed-off-by: qupeng <qupeng@pingcap.com>
```

So the current commit messages of `tikv` and `pd` are usually messy and merely contain useful information. There are a lot of useless and duplicate messages like "format code", "address comments", "add unit tests". And contributors seem to lack the motivation to write good commit messages, since even if they did, the information is berried with other useless messages:

```
raftstore: destroy uninitialized peer can make it possible to recreate old peer (#11457)

* add issue test

Signed-off-by: p4tr1ck <patricknicholas@foxmail.com>

* raftstore: prevent creating staled peer

For an uninitialized peer, both epoch and peer list are empty, so
a message target to a staled peer which override by an uninitialized
peer will be create again. This PR will save the current peer into
peer list if this region is uninitialized.

close #10533

Signed-off-by: p4tr1ck <patricknicholas@foxmail.com>

* address comments

Signed-off-by: p4tr1ck <patricknicholas@foxmail.com>

* address  comments

Signed-off-by: p4tr1ck <patricknicholas@foxmail.com>

* fix test

Signed-off-by: p4tr1ck <patricknicholas@foxmail.com>

* address comment

Signed-off-by: p4tr1ck <patricknicholas@foxmail.com>

* fix test

Signed-off-by: p4tr1ck <patricknicholas@foxmail.com>

Co-authored-by: Ti Chi Robot <ti-community-prow-bot@tidb.io>
```

Almost all the popular open source projects seek for and require writing good commit messages, not leaving TiKV projects. There are some discussions in [tidb forum](https://internals.tidb.io/t/topic/409). Current situations come from the limitations of the tide bot we use. But with the great work of @Mini256, the limitations are gone and we could move forward. I'd like to propose a new pull request requirement and commit message style.

## Solution

The whole solution could be divided into two main parts.

1. Refactor the pull request and issue association rule. 

Currently the bot checks whether there is the required issue number reference in any of the commits. So to fulfill the requirement, contributors need to add the required issue information in at least one of the pull request commit messages. We'd like to drop this rule and apply a new one. 

After this proposal, the bot will check whether there is relevant issue number(s) in the PR body, by `Issue Number: ref #{issue-number}` or `Issue Number: close[sd]?|resolve[sd]?|fix(e[sd])? #{issue-number}`. `ref` means associated with an issue but does not close it. There should be no other content in the same line and the check is case-insensitive. Multiple issues should be separated by a comma, like `Issue Number: close #12341, close #12342`. For PRs trying to close issues in a different repository, contributors need to first create an issue in the same repository and use this issue to track. If the pull request body does not provide the required content, the bot will add the `do-not-merge/needs-linked-issue` label to the pull request to prevent it from being merged.

While merging the PR, the bot will extract the content after `Issue Number:` and add them as a new line to the final commit message body. So if a PR `#12345` has a title `pkg: what's changed in this one package` and its body contains `Issue Number: close #12341, close #12342`, after merging, its commit message is

```
pkg: what's changed in this one package (#12345)

close #12341, close #12342
```

2. Refactor the final commit message style

We hope to encourage contributors to write good, meaningful commit messages, drop useless messages, make the final commit message compact and clean. The current complex and messy merging rule will be changed to:

The one-line subject rule will not be changed. It's still the pull request title. The final commit message body will be completely refactored. It won't take the commit messages of the commits in the pull request any more. We'll introduce a new element in the PR body:

    ```commit-message
    any multiple line commit messages that go into
    the final commit message body

    * fix something 1
    * fix something 2
    ``` 

The content in the `commit-message` code block will be extracted and pasted into the final commit message body. The DCO requirement is still needed for each commit in the pull request. But along with the `Co-authored-by` information, they will be grouped and distinguished by the bot and be appended to the final commit message. So after the proposal, for the first sample commit message in the Motivation section, it will be like:

```
rsmeter: add pubsub datasink  (#11719)

Signed-off-by: Zhenchi <zhongzc_arch@outlook.com>
Co-authored-by: Wenxuan <hi@breeswish.org>
```

And if the pull request body contains the issue information `Issue Number: close #12341, close #12342` and the sample `commit-message` code block, the final commit message will be:

```
rsmeter: add pubsub datasink  (#11719)

any multiple line commit messages that go into
the final commit message body

* fix something 1
* fix something 2

Signed-off-by: Zhenchi <zhongzc_arch@outlook.com>
Co-authored-by: Wenxuan <hi@breeswish.org>

close #12341, close #12342
```

## Affected Repositories

* pd
* tikv

## Deadline

The vote will be open for at least 144 hours unless there is an objection or not enough votes.

We're looking for at least 2 votes from tikv-maintainers, and 2 votes from pd-maintainers.
