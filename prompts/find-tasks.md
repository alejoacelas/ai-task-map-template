# Find tasks to automate

**Purpose:** list the repeated tasks in one person's job, with the facts
[task-entry.md](task-entry.md) needs to turn each into an entry.

**Running it:** Claude interviews the person, or reads notes they wrote and asks
only about what's missing. Write the result to `notes/<name>-tasks.md`.

1. **Ask one question at a time, about real recent work:** what they produced in
   the last two typical weeks, for whom, in which software, and how long it took.
   Ask for specific instances rather than general habits.
2. **Look for repeated units of work** with a defined input and output that recur
   per client, project or period (the Rows rules in task-entry.md). Coordination,
   one-offs and meetings are not tasks.
3. **For each task, find out:**
   - how often it happens and how long one takes;
   - the inputs and where they live, and where the output lands;
   - what a good output looks like, and where past examples are kept;
   - what goes wrong, how it's caught and what an error costs;
   - which steps wait on someone else or need a person (a call, a signature, a
     payment approval);
   - what they know that isn't written down;
   - what they already do with AI or the software's own automation.
4. **Stop** after about 25 minutes, or when the tasks found cover most of their
   week. Write one section per task with these facts, quoting their own words where
   the wording matters, then a line on how their week splits across the tasks.
