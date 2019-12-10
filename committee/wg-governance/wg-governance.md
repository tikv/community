# TiKV Working Group Governance

## What is Working Group?

Contributors are totally able to just work on goals together without it being a WG or formal. We're not 'allowing' it, this is just a formal recognition that this will happen and that WGs can empower and enhance these cooperations.

Due to the Working Group usually solves a problem that spans the scope of responsibility of multiple Special Interest Groups (SIGs), so it usually consists of members from different SIGs or some other community contributors. The Working Group usually dismisses after the problem is solved. And the results or members in the Working Group can be accepted by the SIG after. For more detailed procedures of creating or dismiss, see [WG Lifecycle](#wg-lifecycle).

The Working Group has the following characteristics: 

* Does not own the code
* Have clear measurable goals and results that can be delivered
* Is a short-term organization and will be disbanded after the goal or mission is completed
* Typically addresses a concern affecting multiple SIGs or subprojects

## Relationship between Working Group and Special Interest Group

![wg_sig_relationship](/media/governance/wg_sig_relationship.png)

The assets owned by the TiKV Project (eg: code, documentation, blogs, regulations, etc.) are owned and managed by SIGs. However, there are assets that are specially owned and managed by Working Groups, such as:

* Calendar events
* Slack channel
* Event Progress Report

Working Groups have different goals with those of SIGs. A WG aims to:

* Promote collaboration between different SIGs
* Resolve some specific problems with a minimal organization

The SIGs related to this Working Group should be listed on the Working Group's page in the `Stakeholder SIGs` section. 

## WG Lifecycle 

### Create

* Before creating a working group, make sure you get the following ready:
  * Ensure all WG Organizers, and other leadership roles are community members
  * Have the answers to following questions:
    * What is the exact problem this group is trying to solve?
    * What is the artifact that this group will deliver, and to whom?
    * How does the group know when the problem-solving process is completed, and it is time for the Working Group to dissolve?
    * Who are all of the stakeholder SIGs involved in this problem this group is trying to solve? Have you
    * What are the meeting mechanics (frequency, duration, roles)?
* Once you have met the above criteria, you can submit a Pull Request titled "WG-Creation-Request: XXX-WG", with all the items and related documents (RFCs, PRs) attached. The PR will be reviewed by the PMC. 2 approvals are required for the PR to pass.

* Create an xyz-wg directory in [wg directory](/wg) (modify xyz to your WG name) according to the requirements defined in [Working Group template](working-group-template.md), and modify the Working Group template accordingly.

* Once the PR is approved, this WG is properly charted. You can create a channel corresponding to the Working Group on Slack: tikv-wg.slack.com

### Dismiss

* The Working Group can be dismissed by the organizer after the mission completed.
* If the working group has met one of the following requirements, the working group can be dismissed voluntarily:
  * None of the communication channels for the Working Group have been in use for the goals outlined at the founding of the Working Group in 2 months:
    * Slack channel
    * Zoom meeting room
