# Software memos

**Purpose:** one page per piece of software in the task map's "Software to connect"
column. Each page lets someone who knows the app in passing see how much of its
tasks Claude can do with connections that exist today, what paying or building would
add, and what stays with a person. The memos feed each row's "Data connector
blockers" column.

**Extending:** when a row names new software, add a memo. Recheck a memo's routes
when its "Checked" date is over three months old, since connectors change fast.
Search claude.ai's in-app connector directory, which lists community connectors that
claude.com's directory leaves out. "Out of reach" counts a route that breaks the
software's terms as out of reach, and names it.

## Format

Each memo is `software/<name>.md`: three summary bullets, then a body of about 500
words, then an appendix.

The bullets, each a few short, factual sentences without task ids:

1. **Available now:** free, already-built connections someone can switch on in about
   an hour (a Claude directory connector, an existing hosted or local MCP server,
   Zapier or Make on a free plan, Claude's web search, Claude in Chrome where the
   software's terms allow it). Name the connector, then what it reads and writes,
   measured against everything the tasks need.
2. **Building or buying adds:** what paid tiers, APIs that need code, or paid data
   and integration services add beyond that, as the outcome a staff member would
   notice, then the cost or build time.
3. **Out of reach:** what no route does, each with a one-line reason (no API, the law
   requires a person, a personal identity check, the vendor refuses), plus anything
   only a terms-breaking route such as Claude in Chrome reaches, with its consequence.
   "Nothing" if none.

The body's sections:

1. **What the tasks need:** a bullet per task in plain words, with its id from the
   map in parentheses, saying what Claude reads and writes.
2. **Routes:** a bullet per route, grouped under the three summary labels. Each says
   what it reads and writes, who sets it up and how long it takes, the cost and any
   terms risk, with the primary source linked inline.
3. **What a person still does:** two or three sentences.
4. **To check:** at most three open questions, each naming who could answer. Claims
   nobody has verified go here, not in the summary.
5. **Appendix:** relevant facts that don't fit above, such as the vendor's own AI,
   regulatory timelines and context from interviews.

End with "Checked <date>. Interviews: <person MM-DD>, …". Write in plain sentences,
and name a person when a fact comes from their interview.
