<!--
Please review https://about.gitlab.com/handbook/engineering/infrastructure/change-management/ for the most recent information on our change plans and execution policies.
-->

# Production Change

### Change Summary

{+ Provide a high-level summary of the change and its purpose. +}

### Change Details

1. **Services Impacted**  - <!-- woodhouse: '{{ .ServiceLabels }}' -->{+ List services +}
1. **Change Technician**  - <!-- woodhouse: '`@{{ .Username }}`' -->{+ DRI for the execution of this change +}
1. **Change Reviewer**    - <!-- woodhouse: '@{{ .Reviewer }}' -->{+ DRI for the review of this change +}
1. **Time tracking**      - <!-- woodhouse: '{{ .Duration}}' -->{+ Time, in minutes, needed to execute all change steps, including rollback +}
1. **Downtime Component** - <!-- woodhouse: '{{ .Downtime }}' -->{+ If there is a need for downtime, include downtime estimate here +}

## Detailed steps for the change

### Pre-Change Steps - steps to be completed before execution of the change

*Estimated Time to Complete (mins)* - {+Estimated Time to Complete in Minutes+}

- [ ] Set label ~"change::in-progress" on this issue
- [ ] {+Pre-Change Step 1+}
- [ ] {+Pre-Change Step 2+}
- [ ] {+Pre-Change Step 3+}

### Change Steps - steps to take to execute the change

*Estimated Time to Complete (mins)* - {+Estimated Time to Complete in Minutes+}

- [ ] {+Change Step 1+}
- [ ] {+Change Step 2+}
- [ ] {+Change Step 3+}

### Post-Change Steps - steps to take to verify the change

*Estimated Time to Complete (mins)* - {+Estimated Time to Complete in Minutes+}

- [ ] {+Post-Change Step 1+}
- [ ] {+Post-Change Step 2+}
- [ ] {+Post-Change Step 3+}

## Rollback

### Rollback steps - steps to be taken in the event of a need to rollback this change

*Estimated Time to Complete (mins)* - {+Estimated Time to Complete in Minutes+}

- [ ] {+Rollback Step 1+}
- [ ] {+Rollback Step 2+}
- [ ] {+Rollback Step 3+}

## Monitoring

### Key metrics to observe

<!--
  * Describe which dashboards and which specific metrics we should be monitoring related to this change using the format below.
-->

- Metric: {+Metric Name+}
  - Location: {+Dashboard URL+}
  - What changes to this metric should prompt a rollback: {+Describe Changes+}

## Summary of infrastructure changes

- [ ] Does this change introduce new compute instances?
- [ ] Does this change re-size any existing compute instances?
- [ ] Does this change introduce any additional usage of tooling like Elastic Search, CDNs, Cloudflare, etc?

<!--
  * If you answer yes to any of the items in this checklist, summarize below.
-->
{+Summary of the above+}

## Changes checklist

<!--
To find out who is on-call, in #production channel run: /chatops run oncall production.
-->

- [ ] This issue has a criticality label (e.g. ~C1, ~C2, ~C3, ~C4) and a change-type label (e.g. ~"change::unscheduled", ~"change::scheduled") based on the [Change Management Criticalities](https://about.gitlab.com/handbook/engineering/infrastructure/change-management/#change-criticalities).
- [ ] This issue has the change technician as the assignee.
- [ ] Pre-Change, Change, Post-Change, and Rollback steps and have been filled out and reviewed.
- [ ] This Change Issue is linked to the appropriate Issue and/or Epic
- [ ] Necessary approvals have been completed based on the [Change Management Workflow](https://about.gitlab.com/handbook/engineering/infrastructure/change-management/#change-request-workflows).
- [ ] Change has been tested in staging and results noted in a comment on this issue.
- [ ] A dry-run has been conducted and results noted in a comment on this issue.
- [ ] SRE on-call has been informed prior to change being rolled out. (In #production channel, mention `@sre-oncall` and this issue and await their acknowledgement.)
- [ ] Release managers have been informed (If needed! Cases include DB change) prior to change being rolled out. (In #production channel, mention `@release-managers` and this issue and await their acknowledgment.)
- [ ] There are currently no [active incidents](https://gitlab.com/gitlab-com/gl-infra/production/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Incident%3A%3AActive).

