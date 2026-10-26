# First versions: making them useful and better

**Purpose:** for each row of the automation task map, how an imperfect first
version becomes useful straight away, and how it gets better from there. The first
version itself follows the plan in the "Automation targets" tab of the
[package doc](https://docs.google.com/document/d/1EqAkE7m0G9qMNDbYkQrEJn74h7t5Rc5WaXGpXIQHZaM/edit): connect every input, fix the output format (the row's
Output column), prompt simply. The three fields below are the row's Integration,
Testing and Metrics columns.

## The three fields

1. **Integration:** the first version designed so that using it replaces part of the
   person's work rather than adding to it: as few human steps as possible, and
   Claude's output and the review living in the tool where the person already does the
   final step. Imperfect output is fine as long as checking it costs less than doing
   the work; for high-stakes rows, the first version can check the work people already
   do.
2. **Testing:** how good it is, measured first by a backtest against
   past work (giving Claude only inputs dated before each case), then from evidence
   that builds up through normal use without extra effort. Changes are proposed to a
   named person, never made silently.
3. **Metrics:** two or three numbers anyone can read: how much of the work it handles
   (output used as is or lightly edited), the rate of the error that matters most for
   the row, compared with today's human rate where known, and hours saved. Each is
   computed from data the tools hold or normal use records, with judgement terms
   defined by what the systems record (for example, "applicants the recruiters
   advanced to screening").

## Decisions across rows

- **Output goes into the tool where the final step happens:** Xero records the
  bookkeeper confirms, Airtable fields, Gmail and Slack drafts, a Wise upload file.
  Review happens there, not in a separate document.
- **People keep only structural steps:** authorising payments, signing and submitting
  filings, live calls, sending under their name where a client or candidate would
  notice an error, and LinkedIn sending, which LinkedIn's terms ban automating.
- **Checks with a definite answer run on every unit:** quotes found word for word in
  their source, figures against the system of record, payee details against past
  payments, post details against the signed-off job description.
- **Hours metrics depend on a time tracker** such as Everhour, with staff logging
  time by task.

End with a short list of things to check before building, each naming the rows it
affects: connectors nobody has tried, and past work the backtests assume exists.
