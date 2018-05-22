---
layout: page
title: Setup
root: .
---
Several setup steps may need to be completed before you can complete this lesson.

## Membership of the unix group `jupyterusers`

Out of security considerations only explicitly approved users can access
the Jefferson Lab Jupyter server. Those approved users are all members of the
unix group `jupyterusers`.

You can check whether you are currently a member of the `jupyterusers` group
by logging in to an interactive farm node and issuing the command
```
groups
```
This command will return the list of all groups you are a member of. You can
check the group membership of other users, e.g. `wdconinc`, by issuing the
command
```
groups wdconinc
```
If you are a member of the unix group `jupyterusers`, that group will appear
in the list of groups.

If you are not already a member of the `jupyterusers` group, you can request
to be added to the `helpdesk@jlab.org](mailto:helpdesk@jlab.org).
