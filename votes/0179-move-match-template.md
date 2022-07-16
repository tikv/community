# A Vote for moving match_template to tikv org

## Proposal

[match_template](https://github.com/tikv/tikv/tree/master/components/match_template) is a procedural macro that generates repeated match arms by pattern, which is almost the only way to dispatch code path to static types depending on a runtime value. Since it's general enough, I propose to move it to TiKV org and then publish it to crates.io so that the rust community could be benifit from it.

## Deadline

The vote will be open for at least 6 days unless there is an objection or not enough votes.

## Result

Approved by 2 binding votes.    

- busyjay (binding)
- skyzh (binding)
- tisonkun (binding)
