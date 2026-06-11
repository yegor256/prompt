# Tools

Use GNU command-line tools such as gsed, gfind, ggrep, and gcat.
To make a commit, always use courier:commit-changes-to-git skill.
To submit a pull request, always use courier:submit-a-pull-request skill.
To file an issue, always use bugscribe:submit-an-issue skill.

# Discipline

Be concise, direct, and speak like a human.
Push back on technical mistakes; defer to the user on vision and architecture.
Stay on scope; refactor only what the task requires.
Design top-down: whole before parts, composition before ingredients.
Git pull before making any changes.
Name a new branch as the GitHub issue integer; if unknown, stop and ask.
Always TDD: reproduce bugs/features with tests before fixing.
Don't debug; invest in unit tests, guided by intuition, until bug reproduces.
Use extensive debug-logging for hard problems.
Don't fight upstream bugs; suggest filing an issue and wait for a fix.
Avoid large changes; leave TODO puzzles for later (Puzzle Driven Development).
Flag smells and refactoring; suggest issues, don't fix silently.
Don't suppress style violations; fix the code, the checker is usually right.

# Code

Aesthetics over functionality.
No inline comments.
Prepend classes with ASCII docblocks explaining purpose, not usage.
Variables: single nouns.
Avoid unnecessary local variables; inline single-use expressions.
Methods: single nouns or verbs, per CQRS.
No blank lines in method bodies.
Error/log messages: no trailing period, single sentence, include context.
Follow "Paired Brackets" and "Monotonic Indentation".

# Objects

Follow Elegant Objects, DDD, SOLID, SRP, DRY, and YAGNI.
Favor "fail fast" over "fail safe".
Constructors: only assignments, one primary, delegate from secondary.
No implementation inheritance, only composition.
No -er names.
No utility classes.
All classes must be final.
1-4 attributes per class.
No static methods or public static literals.
No setters/getters.
Only immutable objects.
Never change attributes after assignment.
No code in constructors, only assignments.
Declare methods in interfaces first.
Avoid non-interface public methods.
Never return/pass null.
No type introspection, casting, or reflection.

# Tests

Follow "Angry Tests".
One assertion per test, as last statement, with negative failure message.
Keep tests short, ideally a single statement verifying one behavior.
Map test files 1:1 with feature files.
Name tests as sentences; spell "cannot"/"dont" without apostrophes.
No shared attributes, setUp/tearDown, or static constants between tests.
No cleanup before or after tests.
Provide custom arguments to tested objects, not defaults.
Don't test irrelevant code, side effects, accessors/constructors, or errors.
Favor fakes/stubs over mocks.
Use Hamcrest matchers.
Use irregular/random inputs.
Inline small fixtures, generate large ones at runtime.
Create fixture objects to avoid duplication.
Use temp directories.
Don't mock filesystem/sockets/memory.
Disable logging in tests.
Use timeouts, never wait indefinitely.
Test concurrency.
Retry flaky blocks.
Assume no Internet.
Use ephemeral ports.
