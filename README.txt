All CI workflows must pass before code changes may be reviewed.
The existing code structure must not be changed without a strong reason.
Every bug must be reproduced by a unit test before being fixed.
Every new feature must be covered by a unit test before it is implemented.
Every newly introduced method must have a supplementary docblock preceding it.
Minor inconsistencies and typos in the existing code may be fixed.

Method bodies may not contain blank lines.
Method and function bodies may not contain comments.
Variable names must be single nouns, never compound or composite.
Method names must be single verbs, never compound or composite.
The principle of "Paired Brackets" suggested by Yegor Bugayenko must be respected.
Error and log messages should not end with a period.
Error and log messages must always be a single sentence, with no periods inside.
Favor "fail fast" paradigm over "fail safe": throw exception earlier.

Constructors may not contain any code except assignment statements.
Implementation inheritance must be avoided at all costs (not to be confused with subtyping).
Getters must be avoided, as they are symptoms of an anemic object model.
The DDD paradigm must be respected.
Elegant Objects design principles must be respected.
Class names may not end with the -er suffix.
Setters must be avoided, as they make objects mutable.
Immutable objects must be favored over mutable ones.
Every class may have only one primary constructor; any secondary constructor must delegate to it.
Every class may encapsulate no more than four attributes.
Every class must encapsulate at least one attribute.
Utility classes are strictly prohibited.
Static methods in classes are strictly prohibited.
Method names must respect the CQRS principle: they must be either nouns or verbs.
Classes must avoid using public static literals.
Methods must be declared in interfaces and then implemented in classes.
Public methods that do not implement an interface must be avoided.
Methods must never return null.
Methods should avoid checking incoming arguments for validity.
null may not be passed as an argument.
Type introspection and type casting are strictly prohibited.
Reflection on object internals is strictly prohibited.
All classes must be declared final, thus prohibiting inheritance.
Exception messages must include as much context as possible.

Every change must be covered by a unit test to guarantee repeatability.
Every test case may contain only one assertion.
In every test, the assertion must be the last statement.
Test cases must be as short as possible.
Every test must assert at least once.
Each test file must have a one-to-one mapping with the feature file it tests.
Every assertion must include a failure message that is a negatively toned claim about the error.
Tests must use irregular inputs, such as non-ASCII strings.
Tests may not share object attributes.
Tests may not use setUp() or tearDown() idioms.
Tests may not use static literals or other shared constants.
Tests must be named as full English sentences, stating what the object under test does.
Tests may not test functionality irrelevant to their stated purpose.
Tests must close resources they use, such as file handlers, sockets, and database connections.
Objects must not provide functionality used only by tests.
Tests may not assert on side effects such as logging output.
Tests may not check the behavior of setters, getters, or constructors.
Tests must not clean up after themselves; instead, they must prepare a clean state at the start.
Tests should not use mocks, favoring fake objects and stubs.
The best tests consist of a single statement.
Tests should use Hamcrest matchers if available.
Each test must verify only one specific behavioral pattern of the object it tests.
Tests must use random values as inputs.
Tests should store temporary files in temporary directories, not in the codebase directory.
Tests are not allowed to print any log messages.
The testing framework must be configured to disable logging from the objects under test.
Tests must not wait indefinitely for any event; they must always stop waiting on a timeout.
Tests must verify object behavior in multi-threaded, concurrent environments.
Tests must retry potentially flaky code blocks.
Tests must assume the absence of an Internet connection.
Tests may not assert on error messages or codes.
Tests must not rely on default configurations of the objects they test, providing custom arguments.
Tests must not mock the file system, sockets, or memory managers.
Tests must use ephemeral TCP ports, generated using appropriate library functions.
Tests should inline small fixtures instead of loading them from files.
Tests should create large fixtures at runtime rather than store them in files.
Tests may create supplementary fixture objects to avoid code duplication.
Test method names must spell “cannot” and “dont” without apostrophes.
