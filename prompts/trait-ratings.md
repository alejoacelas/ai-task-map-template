# Rating tasks on the four traits

**Purpose:** the prompt agents follow to rate each task in the task map on the four
traits that make a task harder to automate, so ratings are comparable across teams
and repeatable. The traits come from the "Automation targets" tab of the
[package doc](https://docs.google.com/document/d/1EqAkE7m0G9qMNDbYkQrEJn74h7t5Rc5WaXGpXIQHZaM/edit).

**Running it:** one agent per trait rates every row, so each trait is judged with all
rows side by side. Give the agent the shared rules, its trait's section and the row
list. Each row gets High, Med or Low and one or two sentences of reasoning that name
the deciding fact and, where the scale asks for one, the estimate.

## Shared rules

1. **A row is one repeated unit of work with a defined output**, such as one
   application scored, one payment batch or one client's month-end pack. Judge a
   typical unit, as named in the Task column.
2. **Picture the hand-off.** Claude gets one unit and does it as a staff member
   would. A person sees the result at the end.
3. **Assume the best connection to every tool.** Claude has the best available or
   custom connector for each piece of software, reading every input a staff member
   uses (CVs attached in Airtable included) and writing every output. It can use
   Claude in Chrome on any site, within its limits: it blocks only adult and
   pirated-content sites, asks permission before financial sites, and may not enter
   sensitive data (such as Social Security numbers or bank credentials) or bypass
   CAPTCHAs
   ([help](https://support.claude.com/en/articles/12902428-using-claude-in-chrome-safely)).
   A site's terms banning automation, such as LinkedIn's, are a risk to note, not a
   block.
4. **Don't assume today's practice.** A step needs a person only for a structural
   reason: it's a live conversation, it waits on someone outside the team, it needs
   an action Claude in Chrome may not take (entering sensitive data, passing a
   CAPTCHA or two-factor login), a law or platform requires a person (identity
   checks, signatures, authorising a payment), or it needs judgement Claude can't
   make reliably. That someone does it by hand today is not a reason.
5. **Take documentation as it is today.** Don't credit playbooks or client briefs
   nobody has written; writing them is part of the work an automation needs.
6. **Rate each trait on its own.** A task can be high stakes and low on everything
   else.
7. **Use the sources.** Facts come from the task notes and interview transcripts.
   Cite the person when a fact comes from an interview, such as "(Sam)".
8. **Calibrate.** Each trait lists anchor rows with fixed ratings. Rate everything
   else relative to them, then reread the whole column and fix any pair whose order
   looks wrong.
9. **Reasoning:** at most two sentences, plain words, starting with the deciding
   fact. Write "Low: …", not "This task is rated Low because …".

## Unpredictable difficulty

*Errors are hard to predict, making it hard to delegate to AI only the instances
where it's expected to work reliably.*

Ask: before Claude starts an instance, could a simple rule using only what is
known at the start (amount, client, payee, category, source, the question's topic)
pick out the instances Claude would likely get wrong, so only those go to a person?
Estimate two numbers and state them: the share of instances that are hard for
Claude, and the share of those hard instances such a rule would catch.

- **Low:** fewer than about 5% of instances are hard, or a rule catches 90% or more
  of the hard ones.
- **Med:** a rule catches roughly half to 90% of the hard ones.
- **High:** hard instances look like easy ones at the start; a rule catches less
  than half, and you find out only by doing the work.

Anchors:

- Post a role: **Low.** The same post goes to the same channels each round, and a
  wrong field is obvious.
- Score applications and CVs: **Med.** Clear yeses and nos are easy to spot;
  borderline candidates look like the rest until someone reads closely.
- Research and answer one-off tax questions: **High.** A few words in the facts
  can change the tax treatment, and the question's wording doesn't reveal which
  ones.

## High stakes

*Errors are costly, requiring the automation to have a demonstrably high
performance.*

Estimate in pounds what one typical error costs if Claude's output goes ahead with
only the checks that already exist later in today's process. Don't add a new
review step. Add up:

1. Money lost or misdirected that can't be recovered, and fines or penalties.
2. Staff time to find and fix the error, at £100 an hour (or your billing rate).
3. Harm to the client relationship when the client or a candidate sees the error:
   chance it costs the client × a year of fees. Assume £24,000 a year per client
   unless a source gives a better figure.

Also estimate a bad but plausible error, about 1 in 20. Rate on the typical error,
and go one level higher if the bad one is irreversible or costs over £50,000. State
the typical estimate in the reasoning.

- **Low:** a typical error costs under £200. It is caught later in the process
  within minutes and nobody outside the team sees it.
- **Med:** £200 to £5,000. Hours of rework, or a mistake the client sees but is
  quickly fixed.
- **High:** over £5,000, or money moves irreversibly, or the error reaches a
  regulator, or it could plausibly lose a client.

Anchors:

- Write up call notes and scores: **Low.** The recruiter reads the notes before
  using them; a wrong detail costs minutes.
- Code transactions to account and fund: **Med.** Month-end review catches most
  miscoding at an hour or two of rework; one that slips through misreports a
  restricted grant to the client.
- Build a payment batch, including release: **High.** Money leaves the
  account, and payments under £1,000 skip client review, so a mistake can't be
  recovered.

## Fragmented

*The task interleaves steps that can't be (reliably) performed by AI, requiring
humans to intervene or evaluate outputs at multiple steps.*

Walk one instance from start to finish as steps. Count the points before the end
where a person has to act or check before Claude can continue. These are steps
Claude:

- can't do reliably, because it lacks the judgement;
- can't do at all, for a structural reason under shared rule 4: live calls,
  entering sensitive data or passing two-factor logins, identity checks, signatures,
  authorising payments;
- or has to wait on someone outside the team for: a client's reply, a bank, HMRC.

The one review at the end doesn't count; that's ordinary delegation. State the
count and name the hand-offs.

- **Low:** no hand-offs before the end. Claude could do the task from start to
  finish and a person reviews the result.
- **Med:** one or two hand-offs.
- **High:** three or more, or a live human step in the middle (a call, a portal
  session with an identity check), or waits on outside parties with unpredictable
  delays.

Anchors:

- Write up call notes and scores from a transcript: **Low.** The transcript is
  complete when Claude starts, and a person reviews the scorecard once.
- Build a payment batch: **Med.** Claude builds and checks the batch, but a person
  authorises it on the bank or Wise site, behind a two-factor login, before
  Claude records and reconciles the payments.
- Send a client its unexplained transactions and chase the answers: **High.** Each
  item waits on the client, with unpredictable delays and partial answers.

## Tacit context

*The task may silently fail when AI omits inputs that are undocumented, numerous,
and scattered.*

List the inputs a person uses to do one instance correctly. For each, ask whether
it is written down somewhere Claude can read. Then ask whether Claude's output would
still look plausible without the unwritten inputs; that is the silent failure. A
useful test: could a competent new hire with access to every system but none of the
conversations do an instance correctly on day one?

- **Low:** yes. The inputs are in the systems or a template, and a missing input
  shows up as an obvious gap.
- **Med:** they'd need a short brief per client, a page or less, that doesn't exist
  yet; or the missing context makes the output visibly wrong.
- **High:** they'd need many per-client facts spread across calls, Slack and
  people's heads, and output made without them looks right.

Anchors:

- Post a role: **Low.** The job description and the list of channels hold
  everything needed.
- Write round materials: **Med.** Past examples sit on the Drive; what this client
  wants comes from the kick-off call.
- Code transactions to account and fund: **High.** The rules are per client and
  mostly in the bookkeeper's head, and a wrong fund looks like a right one.
