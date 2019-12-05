# TiKV Working Group Governance

## What is Working Group?

The Working Group provides a group to allow community contributors to collaborate for a period of time on an issue. Due to the Working Group usually solves a problem that spans the scope of responsibility of multiple Special Interest Groups (SIGs), so it usually consists of members from different SIGs or some other community contributors. The Working Group usually dismisses after the problem is solved. And the results or members in the Working Group can be accepted by the SIG after. For more detailed procedures of creating or dissmiss, see [WG Lifecycle](#wg-lifecycle).

The Working Group has the following characteristics: 

* Does not own the code
* Have clear measurable goals and results that can be delivered
* Is a short-term organization and will be disbanded after the goal or mission is completed

## Relationship between Working Group and Special Interest Group

![wg_sig_relationship](/media/governance/wg_sig_relationship.png)

The assets owned by the TiKV Project (eg: code, documentation, blogs, regulations, etc.) are owned and managed by SIGs . Except for special assets owned by the Working Group , such as:

* Calendar events
* Slack channel
* Event Progress Report

The Working Group is different from SIGs , the WG aims to:

* Promote collaboration between different SIGs
* Use the smallest organization to resolve some specific problems or solutions.

The SIGs related to this Working Group should be listed on the Working Group's page in the `Stakeholder SIGs` section. 

## WG Lifecycle 

### Create

* Determine WG organizers and members to ensure that members are TiKV Contributor at least.
* Create a `xyz-wg` directory in [wg directory](/wg) (modify xyz to your WG name) according to [Working Group template](working-group-template.md), and modify the Working Group template as `README.md` page
* Submit a Pull Request on [tikv/community](https://github.com/tikv/community) , which is determined by voting by the Maintainer/PMC. The Working Group is announced after the Pull Request is merged.
* Create a channel corresponding to the Working Group on [Slack: tikv-wg.slack.com](tikv-wg.slack.com) . 

### Dismiss

* The Working Group can be dismissed by the Tech Lead after mission completed.
* If the working group 's work has stalled, the PMC can also vote to dismiss the working group .
