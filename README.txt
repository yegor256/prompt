My pronoun is HE/HIM. My name is Yegor.

Use GNU tools: gsed, gfind, ggrep, gcat, etc.
Don't change code structure without strong reason.
Git pull before making any changes.
Reproduce bugs/features with tests before fixing.
Use extensive debug-logging for hard problems.

No inline comments in source files.
Prepend classes with ASCII docblocks explaining purpose and usage.

Follow DDD, Elegant Objects, "Angry Tests", "Paired Brackets".
Favor "fail fast" over "fail safe".

Constructors: only assignments, one primary, delegate from secondary.
Classes: 1-4 attributes, final, no inheritance, no -er names, no utilities.
No static methods or public static literals.

No setters/getters. Immutable objects. Never change attributes after assignment.

Variables: single nouns. Methods: single verbs per CQRS.
Declare methods in interfaces first. Avoid non-interface public methods.
No blank lines in method bodies. Never return/pass null.
No type introspection, casting, or reflection.

Error/log messages: no trailing period, single sentence, include context.

Tests: one assertion per test, as last statement, with negatively-toned failure message.
Keep tests short, ideally single statement, verify one behavior.
Map test files 1:1 with feature files.
Name tests as sentences; spell "cannot"/"dont" without apostrophes.

No shared attributes, setUp/tearDown, or static constants between tests.
Prepare clean state at start. Provide custom arguments, not defaults.

Don't test irrelevant functionality, side effects, setters/getters/constructors, or error messages.
Favor fakes/stubs over mocks. Use Hamcrest matchers.

Use irregular/random inputs. Inline small fixtures, generate large ones at runtime.
Create fixture objects to avoid duplication.

Close resources. Use temp directories. Don't mock filesystem/sockets/memory.
Disable logging in tests. Use timeouts, never wait indefinitely.
Test concurrency. Retry flaky blocks. Assume no Internet. Use ephemeral ports.
