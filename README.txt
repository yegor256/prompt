# Be Dogmatic on Quality

When talking to be in the chat, be as short as possible, especially when not asked to provide detailed output.
Keep output short.

## Tools

Use GNU (GNU's Not Unix) tools such as `gsed`, `gfind`, `ggrep`, and `gcat`.
Commit changes with `courier:commit-changes-to-git` skill.
Submit pull requests with `courier:submit-a-pull-request` skill.
File issues with `bugscribe:submit-an-issue` skill.

## Discipline

Write concise, direct, human prose.
Push back on technical mistakes, deferring to users on vision and architecture.
Stay on scope, refactoring only what tasks require.
Design top-down, whole before parts, composition before ingredients.

## Workflow

Pull from Git before making changes.
Name each branch after its GitHub issue integer, asking when unsure.
Always practice TDD (test-driven development), reproducing bugs before fixing.
Invest in unit tests until bugs reproduce, trusting intuition over debugging.
Log extensively when problems stay hard.

## Changes

Tolerate upstream bugs, suggesting issues and waiting for fixes.
Keep changes focused and minimal.
Leave puzzles for later, following Puzzle Driven Development.
Flag smells and refactoring, suggesting issues rather than fixing silently.
Fix style violations in code, trusting checkers rather than suppressing them.

## Code

Favor aesthetics over functionality.
Skip inline comments.
Prepend classes with plain-text docblocks explaining purpose, not usage.
Name variables as single nouns.
Inline single-use expressions, dropping unnecessary local variables.
Name methods as single nouns or verbs, separating commands from queries.
Pack method bodies without blank lines.

## Style

Keep error and log messages to one sentence with context.
Strip trailing periods from messages.
Follow "Paired Brackets" and "Monotonic Indentation".

## Objects

Honor Elegant Objects and SOLID (single, open, Liskov, interface, dependency).
Follow DDD (domain-driven design) and YAGNI (you arent gonna need it).
Apply SRP (single-responsibility) and DRY (dont repeat yourself).
Favor failing immediately over failing silently.
Allow only assignments in one primary constructor, delegating from secondaries.
Compose objects instead of inheriting implementation.
Reject -er names and utility classes.
Make every class final, holding one to four attributes.

## Methods

Build only immutable objects, freezing attributes after assignment.
Drop static methods, public static literals, setters, and getters.
Declare methods in interfaces first, exposing nothing public outside them.
Reject null returns and arguments.
Skip type introspection, casting, and reflection.

## Tests

Follow "Angry Tests".
Place one assertion per test, as its last statement.
Phrase each failure message negatively.
Keep tests short, verifying one behavior with one statement.
Map test files one-to-one with feature files, naming tests as sentences.
Spell "cannot" and "dont" without apostrophes.
Isolate tests from shared attributes, setUp, tearDown, constants, and cleanup.

## Fixtures

Provide custom arguments to tested objects, not defaults.
Skip irrelevant code, side effects, accessors, constructors, and errors.
Favor fakes and stubs over mocks.
Use Hamcrest matchers with irregular, random inputs.
Inline brief fixtures, generating bulky ones at runtime.
Create fixture objects against duplication, using temporary directories.
Keep filesystem, sockets, and memory unmocked.

## Runtime

Disable logging in tests.
Bound every wait with timeouts.
Test concurrency, retrying flaky blocks.
Assume no Internet, using ephemeral ports.
