<!--
SPDX-FileCopyrightText: Copyright (c) 2025 Yegor Bugayenko
SPDX-License-Identifier: MIT
-->

# Java Code Generation Rules [v1.0]

## Usage Guide
- Rules have severity: [C]ritical, [H]igh, [M]edium, [L]ow
- When rules conflict: Higher severity wins → Existing code patterns take precedence
- Process rules by severity (Critical first)

## Architecture & Structure [A]

- **[A1-C]** The existing code structure must not be changed without a strong reason.
- **[A2-C]** Every bug must be reproduced by a unit test before being fixed.
- **[A3-C]** Every new feature must be covered by a unit test before it is implemented.
- **[A4-M]** Minor inconsistencies and typos in the existing code may be fixed.
- **[A5-H]** All CI workflows must pass before code changes may be reviewed.
- **[A6-H]** The DDD paradigm must be respected.
- **[A7-H]** Elegant Objects design principles must be respected.

## Code Style & Patterns [S]

- **[S1-H]** Method bodies may not contain blank lines.
- **[S2-H]** Method and function bodies may not contain comments.
- **[S3-M]** Variable names must be single nouns, never compound or composite.
- **[S4-M]** Method names must be single verbs, never compound or composite.
- **[S5-H]** The principle of "Paired Brackets" suggested by Yegor Bugayenko must be respected.
- **[S6-M]** Error and log messages should not end with a period.
- **[S7-M]** Error and log messages must always be a single sentence, with no periods inside.
- **[S8-H]** Favor "fail fast" paradigm over "fail safe": throw exception earlier.
- **[S9-M]** Method names must respect the CQRS principle: they must be either nouns or verbs.
- **[S10-H]** Classes must avoid using public static literals.

## Class Requirements [C]

- **[C1-C]** Every class must have a supplementary docblock preceding it.
- **[C2-H]** A class docblock must explain the purpose of the class and provide usage examples.
- **[C3-H]** Constructors may not contain any code except assignment statements.
- **[C4-C]** Implementation inheritance must be avoided at all costs (not to be confused with subtyping).
- **[C5-H]** Getters must be avoided, as they are symptoms of an anemic object model.
- **[C6-M]** Class names may not end with the -er suffix.
- **[C7-H]** Setters must be avoided, as they make objects mutable.
- **[C8-H]** Immutable objects must be favored over mutable ones.
- **[C9-H]** Every class may have only one primary constructor; any secondary constructor must delegate to it.
- **[C10-M]** Every class may encapsulate no more than four attributes.
- **[C11-H]** Every class must encapsulate at least one attribute.
- **[C12-C]** Utility classes are strictly prohibited.
- **[C13-C]** Static methods in classes are strictly prohibited.
- **[C14-C]** All classes must be declared final, thus prohibiting inheritance.

## Method Requirements [M]

- **[M1-C]** Every method and function must have a supplementary docblock preceding it.
- **[M2-H]** Methods must be declared in interfaces and then implemented in classes.
- **[M3-H]** Public methods that do not implement an interface must be avoided.
- **[M4-C]** Methods must never return null.
- **[M5-M]** Methods should avoid checking incoming arguments for validity.
- **[M6-C]** null may not be passed as an argument.
- **[M7-C]** Type introspection and type casting are strictly prohibited.
- **[M8-C]** Reflection on object internals is strictly prohibited.
- **[M9-H]** Exception messages must include as much context as possible.

## Documentation [D]

- **[D1-H]** The README.md file must explain the purpose of the repository.
- **[D2-H]** The README.md file must be free of typos, grammar mistakes, and broken English.
- **[D3-M]** The README.md file must be as short as possible and must not duplicate code documentation.
- **[D4-H]** Docblocks must be written in English only, using UTF-8 encoding.

## Testing Standards [T]

- **[T1-C]** Every change must be covered by a unit test to guarantee repeatability.
- **[T2-H]** Every test case may contain only one assertion.
- **[T3-H]** In every test, the assertion must be the last statement.
- **[T4-M]** Test cases must be as short as possible.
- **[T5-H]** Every test must assert at least once.
- **[T6-M]** Each test file must have a one-to-one mapping with the feature file it tests.
- **[T7-H]** Every assertion must include a failure message that is a negatively toned claim about the error.
- **[T8-M]** Tests must use irregular inputs, such as non-ASCII strings.
- **[T9-H]** Tests may not share object attributes.
- **[T10-H]** Tests may not use setUp() or tearDown() idioms.
- **[T11-H]** Tests may not use static literals or other shared constants.
- **[T12-M]** Tests must be named as full English sentences, stating what the object under test does.
- **[T13-H]** Tests may not test functionality irrelevant to their stated purpose.
- **[T14-H]** Tests must close resources they use, such as file handlers, sockets, and database connections.
- **[T15-H]** Objects must not provide functionality used only by tests.
- **[T16-M]** Tests may not assert on side effects such as logging output.
- **[T17-L]** Tests may not check the behavior of setters, getters, or constructors.
- **[T18-M]** Tests must not clean up after themselves; instead, they must prepare a clean state at the start.
- **[T19-H]** Tests should not use mocks, favoring fake objects and stubs.
- **[T20-M]** The best tests consist of a single statement.
- **[T21-M]** Tests should use Hamcrest matchers if available.
- **[T22-H]** Each test must verify only one specific behavioral pattern of the object it tests.
- **[T23-M]** Tests must use random values as inputs.
- **[T24-M]** Tests should store temporary files in temporary directories, not in the codebase directory.
- **[T25-H]** Tests are not allowed to print any log messages.
- **[T26-H]** The testing framework must be configured to disable logging from the objects under test.
- **[T27-H]** Tests must not wait indefinitely for any event; they must always stop waiting on a timeout.
- **[T28-H]** Tests must verify object behavior in multi-threaded, concurrent environments.
- **[T29-H]** Tests must retry potentially flaky code blocks.
- **[T30-H]** Tests must assume the absence of an Internet connection.
- **[T31-M]** Tests may not assert on error messages or codes.
- **[T32-H]** Tests must not rely on default configurations of the objects they test, providing custom arguments.
- **[T33-H]** Tests must not mock the file system, sockets, or memory managers.
- **[T34-M]** Tests must use ephemeral TCP ports, generated using appropriate library functions.
- **[T35-M]** Tests should inline small fixtures instead of loading them from files.
- **[T36-M]** Tests should create large fixtures at runtime rather than store them in files.
- **[T37-M]** Tests may create supplementary fixture objects to avoid code duplication.
- **[T38-L]** Test method names must spell "cannot" and "dont" without apostrophes.

## AI Code Generation Process [AI]

- **[AI1-H]** Analyze existing code patterns first
- **[AI2-H]** Write tests before implementation
- **[AI3-H]** Design interfaces before classes
- **[AI4-H]** Implement with immutability in mind
- **[AI5-H]** Error handling: validate early, use Optional<T>, throw specific exceptions
