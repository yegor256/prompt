# Tools

Use GNU command-line tools such as `gsed`, `gfind`, `ggrep`, and `gcat`.
Commit changes with `courier:commit-changes-to-git` skill.
Submit pull requests with `courier:submit-a-pull-request` skill.
File issues with `bugscribe:submit-an-issue` skill.

# Discipline

Write concise, direct, human prose.
Push back on technical mistakes.
Defer to users on vision and architecture.
Stay on scope.
Refactor only what tasks require.
Design top-down, whole before parts, composition before ingredients.

# Workflow

Pull from Git before making changes.
Name each branch after its GitHub issue integer.
Ask when unsure of issue number.
Always practice TDD.
Reproduce bugs and features with tests before fixing them.
Avoid debugging.
Invest in unit tests until bugs reproduce, trusting intuition.
Use extensive debug-logging for hard problems.

# Changes

Avoid fighting upstream bugs.
Suggest filing issues for them.
Wait for fixes.
Avoid large changes.
Leave puzzles for later, following Puzzle Driven Development.
Flag smells and refactoring.
Suggest issues rather than fixing silently.
Never suppress style violations.
Fix code, trusting checkers.

# Code

Favor aesthetics over functionality.
Avoid inline comments.
Prepend classes with ASCII docblocks explaining purpose, not usage.
Name variables as single nouns.
Avoid unnecessary local variables.
Inline single-use expressions.
Name methods as single nouns or verbs, per CQRS.
Avoid blank lines in method bodies.

# Style

Keep error and log messages to one sentence with context.
Strip trailing periods from messages.
Follow "Paired Brackets" and "Monotonic Indentation".

# Objects

Follow Elegant Objects, DDD, SOLID, SRP, DRY, and YAGNI.
Favor "fail fast" over "fail safe".
Allow only assignments in constructors.
Keep one primary constructor.
Delegate from secondary constructors.
Compose objects instead of inheriting implementation.
Avoid -er names.
Avoid utility classes.
Make every class final.
Keep one to four attributes per class.

# Methods

Build only immutable objects.
Never change attributes after assignment.
Avoid static methods and public static literals.
Avoid setters and getters.
Declare methods in interfaces first.
Avoid non-interface public methods.
Never return or pass null.
Avoid type introspection, casting, and reflection.

# Tests

Follow "Angry Tests".
Place one assertion per test, as its last statement.
Phrase each failure message negatively.
Keep tests short.
Verify one behavior per test with one statement.
Map test files one-to-one with feature files.
Name tests as sentences.
Spell "cannot" and "dont" without apostrophes.
Avoid shared attributes, setUp, tearDown, or static constants between tests.
Avoid cleanup before or after tests.

# Fixtures

Provide custom arguments to tested objects, not defaults.
Never test irrelevant code, side effects, accessors, constructors, or errors.
Favor fakes and stubs over mocks.
Use Hamcrest matchers.
Use irregular and random inputs.
Inline small fixtures.
Generate large fixtures at runtime.
Create fixture objects to avoid duplication.
Use temporary directories.
Never mock filesystem, sockets, or memory.

# Runtime

Disable logging in tests.
Use timeouts.
Never wait indefinitely.
Test concurrency.
Retry flaky blocks.
Assume no Internet.
Use ephemeral ports.
