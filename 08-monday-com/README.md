# monday.com — Client Onboarding Tracker

A client onboarding workflow system built in monday.com, covering board setup, multi-view configuration, and status-based automation.

## Session 1: Basics & Navigation

**Board built:** New Client Onboarding Tracker

### What I did
- Created a new board using the Task Management template
- Configured columns: Owner, Status, Due Date, Notes, Last Updated, Files, Priority
- Added 5 custom status labels representing onboarding stages: Inquiry Received, Contract Sent, Contract Signed, Kickoff Started, Active
- Populated the board with 5 sample client records
- Set up and tested four views: Table, Kanban, Calendar, Gantt

### What I learned
- Table and Calendar views read custom status labels natively, no extra configuration needed
- Kanban view requires an explicit "Group by → Status" setting (found in view settings, not the main toolbar) to reflect custom labels correctly — otherwise it defaults to the platform's built-in status set
- Gantt view is timeline-based and only displays items that have due dates; an item without one (an already-active client) was silently excluded until I understood the requirement

### Screenshots
1. `step01-select-category.png`
2. `step02-board-created.png`
3. `step03-sample-clients-added.png`
4. `step04-kanban-view.png`
5. `step05-calendar-view.png`
6. `step06-gantt-view.png`

## Session 2: Automations

**Goal:** Build status-triggered automations on the onboarding tracker

### What I did
- Built a first automation: "When status changes to Contract Signed, notify the owner"
- Tested it and caught a bug: the message showed the literal text "[Item Name]" instead of the client's actual name
- Fixed it by inserting the field via the field-picker instead of typing it manually, then retested and confirmed it worked correctly
- Built a second, multi-step automation: "When status changes to Kickoff Started, notify the owner AND create an update on the item"
- Tested the multi-step automation — worked correctly on the first run

### What I learned
- Dynamic fields (like an item's name) must be inserted through the platform's field-picker — typing a placeholder like "[Item Name]" manually just sends that literal text
- monday.com's automation builder is simpler and more linear than ClickUp's — plain-language recipes with limited branching, good for quick setup but less granular control
- Testing every automation after building it matters — a correctly configured automation can still fail in a small, easy-to-miss way (like the placeholder bug) that's only visible once it actually runs

### Screenshots
1. `step01-first-automation-created.png`
2. `step02-automation-test-notification.png` *(shows the placeholder bug)*
3. `step03-automation-fixed-notification.png` *(shows the fix)*
4. `step04-multistep-automation-created.png`
5. `step05-multistep-automation-test.png`
