# Software testing notes #

## Introduction ##

### Software needs tests at least because ###

-   to know that software works as intended
-   prevent software from bugs or find bugs asap
-   tests help a lot with big changes in code as refactoring, migrations etc.

### Important things regarding testing ###

-   you would like to **write neither many nor not enough tests**. Balance is the key. Because too much tests costs time. And time means money. Not enough tests leads to many bugs, production problems, unsatisfied customer that lead to more fixing less writing new code / features that will cost also time and could lead to losing the customer (the worst scenario). 

-   you would like to **write tests that are working**! You would like to have stronger (with bigger test coverage) tests than weak (with lower test coverage) tests. So question is, which testing strategies to choose and why? Because bad testing strategies could lead also to same results as many or not enough tests (result mentioned earlier).

-   you would like **automate your tests** to run them periodically. 

-   you would like to **do minimum manual tests than is possible to do** because they are time-consuming and cannot be repeated immediately / on demand. Each repetition consumes a lot of time in comparison with automated tests.

-  In the very beginning it is crucial to **choose right testing strategies**. Your software has some nature and / or characteristic. Use it to choose correct testing strategy.

### Personal notes ###

-   I believe in **multi-layered testing strategy**. That means you are using more than one type of tests to achieve the main goal - to have software properly tested. 
-   I do not believe in **hunting bigger code coverage percentage number**! Why bigger number if your tests are weak or wrong? Or you are testing just units and these tests does not say anything about how the hell the code works together? (you have just junit tests and nothing else). First think about things like is my test doing what i think? Have I big coverage number, but I do not have automated higher level tests for testing dependencies and see if modules are working together?  
- **I am not really fan of TDD**, regardless if [it is dead](https://martinfowler.com/articles/is-tdd-dead/) [or not](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html). Just philosophical question here (I would like not spend so much time here with TDD so just one question) : Why start with something that is not a main product (test) instead of something that is major (software)? Why spend so much time with tests. I would like to spend as little time with writing test as possible!


## Testing categories ##

There are so many test types. It is of course possible group different tests into categories. To have better picture I start with categories first. 

-   **Object of testing** - Functional testing, Non-functional testing.
-   **Knowledge of the system** - Black box testing, White box testing, Grey box testing.
-   **Degree of automation** - Automated testing, Manual testing, Semi-automated testing.
-   **Degree of isolation components** - Unit testing, Component testing, Integration testing, System testing, End to end testing.
-   **Basis of positive scenario** - Positive testing, Negative testing.
-   **Time of testing** - Alpha testing, Beta testing, Acceptance testing...
-   **Degree of preparedness to be tested** - documentation testing, Ad hoc testing.
-   **Who is executing the tests** - developer, testing team, QA team, end user ...
-   **Functional testing** - Unit testing, Acceptance testing, White box testing ...
-   **Non-functional testing** - Security testing, Load testing, Stress testing, Penetration testing, Smoke testing ...


## Testing tools / frameworks (Java) ##

In this section there are all testing types listed which have tools / frameworks / libraries for performing it. For example, you can do [Acceptance testing](https://www.guru99.com/user-acceptance-testing.html) with [Cucumber](https://cucumber.io), so it is on list. But on other side for example [Ad Hoc testing](https://www.guru99.com/adhoc-testing.html) as far as i know has no tool / framework for it, so you can use whatever make sense to you. Here it is important  what  Ad hoc is, not the tool for it. No tool is definitely wired to that type of test. That is the reason why it is not on the list. 

### Acceptance testing ###

Formal testing conducted to determine whether a system satisfies its acceptance criteria and to enable the customer to determine whether to accept the system. It is usually performed by the customer.[More info](https://www.guru99.com/user-acceptance-testing.html)

-   [Cucumber](https://cucumber.io) - BDD
-   [JGiven](http://jgiven.org) - BDD
-   [YatSpec](https://github.com/bodar/yatspec) - BDD
-   [Concordion](https://concordion.org)
-   [FitNesse](http://www.fitnesse.org)

### Accessibility Testing ###

Type of testing which determines the usability of a product to the people having disabilities (deaf, blind, mentally disabled etc.). The evaluation process is conducted by persons having disabilities. [More info](https://www.guru99.com/accessibility-testing.html)

-   [Accessibility Developer Tools](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb?hl=en)
-   [AChecker](https://achecker.ca/checker/index.php)
-   [Wave](http://wave.webaim.org)
-   [TAW](https://www.tawdis.net)
-   [Accessibility Valet](http://valet.webthing.com/access/url.html)
-   [Quick Accessibility Page Tester](https://accessify.com/tools-and-wizards/accessibility-tools/favelets/quick-page-test/)
-   [aDesigner](http://www.eclipse.org/actf/downloads/tools/aDesigner/)

### API Testing ###

Testing technique similar to Unit Testing in that it targets the code level. API Testing differs from Unit Testing in that it is typically a QA task and not a developer task. [More info](https://www.guru99.com/api-testing.html)

-   [Postman with Newman](https://www.getpostman.com)
-   [SOAP UI](https://www.soapui.org)
-   [Curl](https://curl.haxx.se)

### All-pairs Testing / Pairwise Testing ###

Combinatorial testing method that tests all possible discrete combinations of input parameters. It is performed by the testing teams. It is a Black box testing method. [More info](https://www.softwaretestinghelp.com/what-is-pairwise-testing/) and [even more info](http://www.pairwise.org).

-   [QuickTheories](https://github.com/ncredinburgh/QuickTheories)
-   [junit-quickcheck](http://pholser.github.io/junit-quickcheck/site/0.8.1/)
-   [QuickCheck (Java)](https://bitbucket.org/blob79/quickcheck/src/default/)
-   [jqwik](https://jqwik.net)
-   [All Pairs](http://www.satisfice.com/tools.shtml)
-   [More tools](http://www.pairwise.org/tools.asp)

### Statement Testing ###

is a structural testing strategy that uses the program’s control flow as a model. 100% statement coverage. Execute all statements in a program at least once under some test. Control flow path contains statements linked together with links. Links link together statements. Statement is basic (simple) executable code. Related topic please see [Statement coverage](https://www.guru99.com/code-coverage.html#4)

**Related** : Statement Testing <= Branch Testing <= Path Testing.

### Basis Path Testing ###

A testing mechanism which derives a logical complexity measure of a procedural design and use this as a guide for defining a basic set of execution paths. Basis path testing involves execution of all possible blocks in a program and achieves maximum path coverage with least number of test cases. It is a hybrid of branch testing and path testing methods. [More info](https://www.guru99.com/basis-path-testing.html)

### Branch Testing ###

is a structural testing strategy that uses the program’s control flow as a model. 100% branch coverage. Execute all branches in a program at least once under some test. Control flow path contains statements linked together with links. If between 2 statements exists more than 1 link all these are named branches and are executed also with original link (original link is special branch lets say but still branch). Related topic please see [Branch coverage](https://www.guru99.com/code-coverage.html#6)

**Related** : Statement Testing <= Branch Testing <= Path Testing.

### Path Testing ###

is structural testing method that involves using the source code of a program in order to find every possible executable path. 100% Path coverage. Execute all possible control flow paths through the program. Control flow path contains statements linked together with links.

**Related** : Statement Testing <= Branch Testing <= Path Testing.

**More info**

-   [1](https://www.guru99.com/basis-path-testing.html), [2](https://ifs.host.cs.st-andrews.ac.uk/Books/SE9/Web/Testing/PathTest.html), [3](https://www.cs.drexel.edu/~jhk39/teaching/cs576su06/L4.pdf)

### Mutation testing ###

Method of software testing which involves modifying programs' source code or byte code in small ways in order to test sections of the code that are seldom or never accessed during normal tests execution. It is normally conducted by testers. [More info](https://www.guru99.com/mutation-testing.html).

-   [PIT](http://pitest.org)
-   [MuJava](https://cs.gmu.edu/~offutt/mujava/)
-   [JavaLanche](https://github.com/david-schuler/javalanche)
-   [Major](http://mutation-testing.org)
-   [Jumble](http://jumble.sourceforge.net)
-   [Descartes](https://github.com/STAMP-project/pitest-descartes)
-   [Jester](http://jester.sourceforge.net)
-   [Judy](http://madeyski.e-informatyka.pl/tools/judy/)

### Benchmark testing ###

-   [Java Microbenchmark Harness (JMH)](https://github.com/peterszatmary/jmh-benchmark-demo)
-   [Benchmark Framework 2.0 & TechEmpower](https://www.techempower.com/benchmarks/)

### Unit testing ###

-   [Junit]()
-   [ArchUnit](https://github.com/TNG/ArchUnit)
-   [DBUnit](http://dbunit.sourceforge.net)

### Load testing ###

-   [Gatling](https://gatling.io)
-   [Apache JMeter](https://jmeter.apache.org)

### Performance testing ###

-   [Gatling](https://gatling.io)
-   [Apache JMeter](https://jmeter.apache.org)

### Endurance Testing ### 
-   Type of testing which checks for memory leaks or other problems that may occur with prolonged execution. It is usually performed by performance engineers.

-   [Apache JMeter](https://jmeter.apache.org)
-   [Gatling](https://gatling.io)

### UI testing ###

-   [Serenity]()
-   [Selenium](https://www.seleniumhq.org)

### End to end testing ###

-   [Endly](https://github.com/viant/endly/)

### Other ###

-   [EasyMock](http://easymock.org)
-   [REST Assured]()
-   [PowerMock](https://github.com/powermock/powermock)
-   [Mockito](https://site.mockito.org)
-   [TestNG](https://testng.org/doc/index.html)
-   [Spock](http://spockframework.org)
-   [Spring Test]()
-   [Arquillian]()
-   [Fit](http://fit.c2.com)

### Code covarage tools ###

[Code coverage theory](https://www.guru99.com/code-coverage.html).

**Watch out** : [Test Coverage is not a code coverage](https://www.sealights.io/test-metrics/code-coverage-vs-test-coverage-pros-and-cons/)

-   [Jacoco](https://github.com/jacoco/jacoco)
-   [Cobertura](http://cobertura.github.io/cobertura/)
-   [Clover](https://bitbucket.org/atlassian/clover/src/default/)
-   [EclEmma](https://www.eclemma.org)

### Test Coverage ###

Simplified, it measures test quality or test strength. In other words it measures how much of code has one test executed in real. [More info](https://www.guru99.com/test-coverage-in-software-testing.html)

**Watch out** : [Test Coverage is not a code coverage](https://www.sealights.io/test-metrics/code-coverage-vs-test-coverage-pros-and-cons/)

-   [Java Test Coverage Tool](http://www.semdesigns.com/Products/TestCoverage/JavaTestCoverage.html?Home=TestCoverage)
-   [EclEmma](https://www.eclemma.org)

## Not mentioned testing types ##

- Active Testing, Agile Testing, Age Testing, Ad-hoc Testing:, Automation Testing, Alpha Testing, Assertion Testing, Beta Testing,

## Useful links ##

-   [the-classification-of-kinds-of-software-testing](http://blog.qatestlab.com/2011/04/09/the-classification-of-kinds-of-software-testing/)
-   [classification-among-testing](https://www.softwaretestinggenius.com/classification-among-testing/)
-   [the-classification-of-types-of-software-testing](https://www.utest.com/articles/the-classification-of-types-of-software-testing)
-   [software-testing](https://www.guru99.com/software-testing.html)
-   [types-of-software-testing](https://www.softwaretestinghelp.com/types-of-software-testing/) 
-   [List of 100 Different Testing Types](https://www.guru99.com/types-of-software-testing.html)
-   [Martin Fowler - Is TDD Dead](https://martinfowler.com/articles/is-tdd-dead/)
-   [tdd-is-dead-long-live-testing](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html)

