All CI workflow must pass before code changes may be reviewed.

Method bodies may not contain blank lines.
Method and function bodies may not contain comments.
Variable names must be single nouns, never compound or composite.
Method names must be single verbs, never compound or composite names.

Constructors may not contain any code, except assignment statements.
Implementation inheritance must be avoided at all cost (not to be confused with subtyping).
Getters must be avoided, as symptoms of anemic object model.
DDD paradigm must be respected.
Elegant Objects design principles must be respected.
Class names may not end with the -ER suffix.
Setters must be avoided, since they make objects mutable.
Immutable objects must be favored over mutable ones.

Every change made must be covered by a unit test, to guarantee repeatability.
Every test case may have only one assertion.
In every test, an assertion must be the last statement.
Test cases must be as short as possible.
Every test must assert at least once.
Every test file must be one-to-one mapped to the feature file that it tests.
Every assertion must have a failure message that is a negatively toned claim about the error.
Tests must use irregular inputs, such as non-ASCII strings.
Tests may not share objects attributes.
Tests may not use setUp() or tearDown() idioms.
Tests may not use static literals or any other shared constants.
Tests must be named as full English sentences, saying what an object under test does.
Tests may not test functionality that is not relevant to the purpose of the test.
Tests must close resources they use, such as file handlers, sockets, and database connections.
Objects must not provide functionality that is used only by tests.
Tests may not assert on side-effects, such as logging output.
Tests may not check the behavior of setters, getters, or constructors.
Tests must not clean up after themselves, instead they should prepare clean state on their start.
Tests should not use mocks, trying to use fake objects and stubs.
Bests tests consist of a single statement.
Tests should use Hamcrest matchers if they are available.
Each test must verify only one particular behavioral pattern of the object it tests.
Tests must use random values as inputs.
Tests should keep temporary files in temporary directories, not in the code base directory.
Tests are not allowed to print any log messages.
Testing framework must be configured to disable any logging messages of objects under test.
Tests must not wait for any event endlessly, always trying to stop waiting on timeout.
Tests must vefiry the behaviour of objects in multi-threaded concurrent mode.
Tests must retry possibly flaky code blocks.
Tests must assume the absence of the Internet connection.
Tests may not assert on error values, either messages or codes.
Tests must not rely on default configurations of the objects they test, always providing custom arguments.
Tests must not mock file system, sockets, and memory managers.
Tests must use ephemeral TCP ports, generating them with the help of relevant library functions.
Tests must try to inline reasonably small fixtures instead of using files.
Tests must try to create large fixtures in runtime instead of keeping them in files.
Tests may create and supplementary fixture objects to avoid code duplication.
