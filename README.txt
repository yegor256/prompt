# Tools

Use GNU command-line tools such as gsed, gfind, ggrep, and gcat.
To make a commit, always use courier:commit-changes-to-git skill.
To submit a pull request, always use courier:submit-a-pull-request skill.
To file an issue, always use bugscribe:submit-an-issue skill.

# Discipline

Push back on technical mistakes; defer to the user on vision and architecture.
Stay on scope; refactor only what the task requires.
Git pull before making any changes.
Always TDD: reproduce bugs/features with tests before fixing.
Use extensive debug-logging for hard problems.
Don't fight upstream bugs; suggest filing an issue and wait for a fix.
Avoid large changes; leave TODO puzzles for follow-up (Puzzle Driven Development).
Flag smells and refactoring; suggest issues, don't fix silently.

# Code

No inline comments.
Prepend classes with ASCII docblocks explaining purpose, not usage.
Variables: single nouns.
Methods: single verbs per CQRS.
No blank lines in method bodies.
Error/log messages: no trailing period, single sentence, include context.
Follow "Paired Brackets".

# Objects

Follow Elegant Objects and DDD.
Favor "fail fast" over "fail safe".
Constructors: only assignments, one primary, delegate from secondary.
No inheritance, only composition.
No -er names.
No utility classes.
Only final classes.
1-4 attributes per class.
No static methods or public static literals.
No setters/getters.
Immutable objects.
Never change attributes after assignment.
Declare methods in interfaces first.
Avoid non-interface public methods.
Never return/pass null.
No type introspection, casting, or reflection.

# Tests

Follow "Angry Tests".
One assertion per test, as last statement, with negatively-toned failure message.
Keep tests short, ideally a single statement verifying one behavior.
Map test files 1:1 with feature files.
Name tests as sentences; spell "cannot"/"dont" without apostrophes.
No shared attributes, setUp/tearDown, or static constants between tests.
No cleanup before or after tests.
Provide custom arguments to tested objects, not defaults.
Don't test irrelevant functionality, side effects, setters/getters/constructors, or error messages.
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
