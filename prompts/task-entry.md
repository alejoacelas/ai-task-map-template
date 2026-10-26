# How to write a task entry

**Purpose:** the rules for the automation task map, a table with one row per
repeated task, so anyone extending or re-rating it gets the same kind of row and
column. The input is the task notes from [find-tasks.md](find-tasks.md); the
"Sample tasks" tab of the [package doc](https://docs.google.com/document/d/1EqAkE7m0G9qMNDbYkQrEJn74h7t5Rc5WaXGpXIQHZaM/edit) shows six finished rows.

**Extending:** hours come from [hours.md](hours.md), trait ratings from
[trait-ratings.md](trait-ratings.md), Integration, Testing and Metrics from
[first-version.md](first-version.md) and the software columns from
[software-memo.md](software-memo.md). Write the rows to `tasks.md`, one section
per row, or to a Google Sheet; if it's a sheet, read it before writing to it and
keep edits made there.

## Rows

1. **A row is a repeated unit of work with a defined input and output** (an
   application scored, a payment batch, a client's month-end pack) that recurs per
   client, round or period, so its volume grows with clients. It should be something
   an agent could draft and that can be graded against a staff member's version.
2. **Work between rows is glue and has no row:** coordination, one-off projects,
   software troubleshooting, supervising colleagues, and the live calls themselves.
   Rows deliberately add up to well under each team's working time.
3. **Split a task where its outputs or its four traits differ;** merge rows that serve
   one outcome. For example, a team's tracker updates, client updates and call
   briefs are one row, "keep a client's status current".
4. **Human-only steps sit inside the row they belong to** (the screening call inside
   the write-up row, authorising payments inside the payment-batch row) and count
   towards its Fragmented rating.
5. **Ids rank rows within each team by h/month midpoint:** F1 is finance's biggest
   row. Ties go to the higher top of the range.

## Columns

In order:

- **#, Team, Task.**
- **Output:** what the agent produces for one unit, where it lands (a Xero record, an
  Airtable field, a Gmail draft) and what it must contain. It is the spec for whoever
  builds the automation and the thing its output is graded against.
- **h/month:** the low–high range of staff hours a month on the unit, done by hand,
  excluding glue, following hours.md. It is the figure to trust.
- **h/month midpoint:** the estimate the range is built around (the sum of each
  person's midpoint), for sorting.
- **Developer:** builds the automation. The person who spends most hours on the unit,
  with a one- or two-word reason, such as "(most hours)" or "(tied hours)". Never the
  process owner unless no one else does the work.
- **Process owner:** judges whether the output is good enough, usually the team's
  lead.
- **The four traits, each with a Why:** Unpredictable difficulty, High stakes,
  Fragmented, Tacit context, rated High, Med or Low with trait-ratings.md: one agent
  per trait rates every row side by side against fixed anchor rows. Ratings assume
  the best available connector for every tool, Claude in Chrome within its own limits,
  and a person only where a step structurally needs one, but take documentation as it
  is today.
  - Why: one sentence of at most 25 words, starting with the fact that sets the
    level, with no "High:" prefix and no scale mechanics. A number appears only when
    it is the point, such as a £ figure for stakes.
- **Software to connect:** software Claude needs beyond what is already connected
  (for example Google Workspace and your own Slack).
- **Data connector blockers:** only the steps that need a paid service, a build or a
  person, or can't be automated, in short plain sentences. "None" means free
  connectors cover it, which is the baseline and isn't stated.
- **Integration, Testing, Metrics:** how an imperfect first version becomes useful
  straight away and how it gets better, following first-version.md.
- **Existing automations:** what staff already do with AI or the tools' own
  automation, from the interviews.
- **Shared pattern:** tags rows in different teams that serve the same outcome, so
  their hours can be summed.
