# AI automation task map template

Prompts for Claude Code that take someone from "what do I do all week" to a ranked
list of their repeated tasks, each with a structured entry saying how hard it is to
automate and how a first version would work, and then to building that first
version. Six example entries and the reasoning behind the four ratings are in the
[package doc](https://docs.google.com/document/d/1EqAkE7m0G9qMNDbYkQrEJn74h7t5Rc5WaXGpXIQHZaM/edit).

## Steps

1. **Learn Claude Code** with Anthropic's free
   [Claude Code 101](https://academy.claude.com/en/courses/claude-code-101) course. It
   needs a paid Claude plan or an API key.
2. **Find your tasks.** Clone this repository, open Claude Code in it and say
   `Interview me following prompts/find-tasks.md`. If you'd rather write, put your
   notes in `notes/<your-name>.md` and say
   `Read notes/<your-name>.md and follow prompts/find-tasks.md`.
3. **Write an entry per task:** say
   `Write an entry for each task in notes/<your-name>-tasks.md following prompts/task-entry.md`.
4. **Build one.** Pick a task with many hours and low ratings, and build the first
   version its Integration field describes. Backtest it as its Testing field says
   before relying on it, and track its Metrics.

## Prompts

1. [find-tasks.md](prompts/find-tasks.md): the interview that lists your repeated tasks.
2. [task-entry.md](prompts/task-entry.md): the rows and columns of an entry; it
   calls the four below.
3. [hours.md](prompts/hours.md): staff hours a month per task, with a range.
4. [trait-ratings.md](prompts/trait-ratings.md): the four traits that make a task
   harder to automate, rated High, Med or Low.
5. [first-version.md](prompts/first-version.md): how an imperfect first version is
   useful straight away, how it's tested and what to measure.
6. [software-memo.md](prompts/software-memo.md): a page per piece of software
   Claude can't reach yet, on what connecting it takes.
