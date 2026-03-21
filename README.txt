My pronoun is HE/HIM, not THEY/THEM.
My name is Yegor, call me by name.

Always use GNU tools, like gsed, gfind, ggrep, gcat, etc.
Don't change existing code structure without a strong reason.
Reproduce a bug or a feature with a unit or integration test and only then fix it.
Be verbose and direct in README.md and code documentation.
Don't use inline code comments, only codeblocks on top of classes and methods.
Prepent every class with a docblock that explains the purpose of the class and provides usage examples.
Use English only to write doclbocks, using only ASCII.
Don't put black lines into method bodies.
Use single nouns for variable names, never use compound or composite names.
Use single verbs for method names, never compound or composite.
Respect the principle of "Paired Brackets" suggested by Yegor Bugayenko.
Don't end error and log messages should with a period.
Keep error and log messages as single sentences, with no periods inside.
Favor "fail fast" paradigm over "fail safe": throw exception earlier.
Don't put any code in constructors except assignment statements.
Avoid implementation inheritance at all costs (not to be confused with subtyping).
Avoid getters, as they are symptoms of an anemic object model.
Respect the DDD paradigm.
Respect Elegant Objects design principles.
Don't use the -er suffix in class names: don't create Managers, Controllers, Routers, Readers, and Writers.
Avoid setters, as they make objects mutable.
Favor immutable objects over mutable ones.
Never change attributes after assignment.
Use only one primary constructor per class; delegate from secondary constructors to it.
Encapsulate no more than four attributes per class.
Encapsulate at least one attribute per class.
Don't create utility classes.
Don't use static methods in classes.
Name methods according to CQRS principle: use either nouns or verbs.
Don't use public static literals in classes.
Declare methods in interfaces and then implement them in classes.
Avoid public methods that do not implement an interface.
Never return null from methods.
Avoid checking incoming arguments for validity in methods.
Never pass null as an argument.
Don't use type introspection or type casting.
Don't use reflection on object internals.
Declare all classes as final, prohibiting inheritance.
Include as much context as possible in exception messages.

Cover every change with a unit test to guarantee repeatability.
Put only one assertion in every test case.
Place the assertion as the last statement in every test.
Keep test cases as short as possible.
Assert at least once in every test.
Map each test file one-to-one with the feature file it tests.
Include a failure message in every assertion that is a negatively toned claim about the error.
Use irregular inputs in tests, such as non-ASCII strings.
Don't share object attributes between tests.
Don't use setUp() or tearDown() idioms in tests.
Don't use static literals or other shared constants in tests.
Name tests as full English sentences, stating what the object under test does.
Don't test functionality irrelevant to the test's stated purpose.
Close resources in tests, such as file handlers, sockets, and database connections.
Don't provide functionality in objects used only by tests.
Don't assert on side effects such as logging output in tests.
Don't check the behavior of setters, getters, or constructors in tests.
Prepare a clean state at the start of tests instead of cleaning up after themselves.
Favor fake objects and stubs over mocks in tests.
Aim for tests that consist of a single statement.
Use Hamcrest matchers in tests if available.
Verify only one specific behavioral pattern per test.
Use random values as inputs in tests.
Store temporary files in temporary directories, not in the codebase directory.
Don't print any log messages in tests.
Configure the testing framework to disable logging from the objects under test.
Never wait indefinitely for any event in tests; always stop waiting on a timeout.
Verify object behavior in multi-threaded, concurrent environments in tests.
Retry potentially flaky code blocks in tests.
Assume the absence of an Internet connection in tests.
Don't assert on error messages or codes in tests.
Don't rely on default configurations of the objects under test, provide custom arguments.
Don't mock the file system, sockets, or memory managers in tests.
Use ephemeral TCP ports in tests, generated using appropriate library functions.
Inline small fixtures in tests instead of loading them from files.
Create large fixtures at runtime rather than store them in files.
Create supplementary fixture objects to avoid code duplication in tests.
Spell "cannot" and "dont" without apostrophes in test method names.
