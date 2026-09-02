## Session 3: Advanced Automation — Overdue Client Escalation

**Goal:** Build a more complex, real-world automation: detect when a client's due date has passed while they're still not "Active," and escalate automatically.

### What I did
- Designed an automation: "When due date arrives, and only if Item Status is not Active, then notify Me and set Item Priority to High"
- Configured it with a trigger (date arrives), a condition (status is not Active), and two chained actions (notify + change priority)
- Tested it by setting a due date/time for the same day, expecting the same instant behavior I'd seen with status-change automations in Session 2
- The automation did not fire. Checked Run History — no run attempts logged at all
- Tested three separate times across the evening with different set times. Still no trigger

### What I learned
- Status-change automations (Session 2) fire instantly, the moment the value changes — they're event-triggered
- Date-based automations work differently: monday.com checks against one fixed time set in the automation itself (defaulting to midnight if unset), not the specific time entered in each item's due date field
- This means date-triggered automations are not real-time and can't be assumed to fire immediately, even when correctly configured
- For time-sensitive escalations in real client work, status-change triggers are more reliable than date-based ones; date triggers are better suited to daily/scheduled checks rather than precise timing

### Why this matters
Escalation automations are meant to catch problems humans might miss, not resolve them. The notify + priority-change actions surface the issue; a human still has to actually follow up with the client. This automation's job is detection, not resolution, and that boundary is intentional, not a limitation of the build.

### Screenshots
1. `step01-overdue-escalation-automation-config.png`

*(Follow-up: checking Run History again after 24 hours to confirm whether the automation fired overnight — result to be added.)*
