# Staff hours by task

**Purpose:** monthly staff hours for each row of the automation task map, built
person by person from what each person said about their own time, as the best
estimate of "hours saved if this task were fully automated", with a low–high range.

**Extending:** after an interview or a time-tracking export, replace that person's
figure in each row they work on with what they stated, using the range rules below,
then re-sum the row and recheck their monthly total. Where nobody stated a time, use
units × minutes. Round rows to the nearest 5 h (minimum 5).

## Method

1. **Rows are repeated units of work.** Each row recurs per client-month, payment
   run, round, application, call or question. Coordination, supervision, one-offs,
   troubleshooting and the live calls themselves are glue and have no row, so a
   person's rows should leave room for them. Human-only steps inside a row are
   excluded too, because the hours measure time an automation could save: the
   screening call itself, releasing payments, and submitting, identity checks and
   fees for an application.
2. **Person by person.** Within a row, each person who does the work gets a
   midpoint. Where they stated their own time (a share of their week × 140 h, hours
   a week, or counts with times per unit), that is their midpoint. A 140 h month is
   a 37.5-hour week less leave and bank holidays.
3. **Stated figures get narrow ranges**, about ±20%, widened only for a named reason:
   - the share covers several rows and was split by guess: ±35–40%;
   - the person is new, in their first two months: ±50%;
   - the answer reflects a peak, such as a filing season: the midpoint moves to a
     typical month and the range widens;
   - the person's statements exceed their month: the vaguest one is cut, with the
     cut stated.
4. **Shares include the glue around the work.** A share of the week, such as "80%
   books and payments", includes the meetings, Slack and admin around that work,
   which people did not separate out. So no one's rows exceed about 100 h a month.
   Where someone's stated figures add up to more, their rows are scaled down
   uniformly to 100 h: mid and low scale, and the high stays at the unscaled figure,
   so the literal reading of what they said stays inside the range.
5. **Where nobody stated a time**, midpoint = units × minutes, and the range
   combines the two uncertainties in log space: the high is mid ×
   exp(√(ln(units high ÷ units best)² + ln(minutes high ÷ minutes best)²)), and the
   low likewise downwards.
6. **Row totals.** The row midpoint is the sum of person midpoints. The row range
   sums person deviations in quadrature, treating people as independent; where one
   units × minutes guess is split across several people, their shares move together
   and are summed first.

## Output

First, per person, a bullet with what they said about their own time, cited as
`<person>/<MM-DD>:<line>` (the line of their interview transcript of that date).
Then a table per team:

| Row | h/month mid (low–high) | Range reason | People (h) | Basis |
|---|---|---|---|---|
