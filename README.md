# Software testing notes #

## Introduction ##

### Software needs tests at least because ###

-   to know that software works as intended
-   prevent software from bugs or find bugs asap
-   tests helps a lot with big changes in code as refactoring, migrations etc.

### As i see very important things regarding testing are ###

-   you would like to **write neither many nor not enough tests**. Balance is the key. Because to much tests costs time. And time means money. Not enough code leads to many bugs, production problems, unsatisfied customer that lead to more fixing less writing new code that what cost also time and can lead to lossing the customer (worst scenario). 

-   you would like to **write tests that are working** !! You would like to have stronger tests than weak (weaker) tests. So question is, which testing strategies to choose and why? Because bad testing strategies could lead also to same results as many or not enough tests (result mentioned earlier).

-   you would like **automate your tests** to run them periodically. 

-   you would like to **do minimum manual tests than is possible to do** because they are time consuming and cannot be repeated immediately / on demand. Each repetition consumes a lot of time in comparison with automated tests.

### Personal notes ###

-   I believe in **multi-layered testing strategy**. That means you are using more than one type of tests to achieve the main goal - to have software properly tested. 
-   I dont believe in **hunting bigger code coverage percentage number** ! Why bigger number if your tests are weak or wrong ? First think about things like is my test correct ? Is it my test doing what i think ? It is my test testing properly ? Is it my test working just with correct inputs or also with wrong ones ?
- **I am not really fan of TDD**, regardless if [it is dead](https://martinfowler.com/articles/is-tdd-dead/) [or not](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html). Just philosophical question here (I would like not spend so much time here with TDD so just one question) : Why start with something that is not a main product (test) instead of something that is major (software) ? 


## Testing categories ##

There are so many test types. It is of course possible group different tests to categories. To have better picture i start with categories first. 

-   **Object of testing** - Functional testing, Non functional testing.
-   **Knowledge of the system** - Black box testing, White box testing, Grey box testing.
-   **Degree of automation** - Automated testing, Manual testing, Semi-automated testing.
-   **Degree of isolation components** - Unit testing, Component testing, Integration testing, System testing, End to end testing.
-   **Basis of positive scenario** - Positive testing, Negative testing.
-   **Time of testing** - Alpha testing, Beta testing, Acceptance testing...
-   **Degree of preparedness to be tested** - documentation testing, Ad hoc testing.
-   **Functional testing** - Unit testing, Acceptance testing, White box testing ...
-   **Non functional testing** - Security testing, Load testing, Stress testing, Penetration testing, Smoke testing ...


## Testing tools / frameworks (Java) ##

In this section there are are all testing types listed which have tools / frameworks / libraries for performing it. For example you can do [Acceptance testing](https://www.guru99.com/user-acceptance-testing.html) with [Cucumber](https://cucumber.io) so it is on list. But on other side for example [Ad Hoc testing](https://www.guru99.com/adhoc-testing.html) as far as i know has no tool / framework for it so you can use whatever make sense to you. Here it is important  what  Ad hoc is, not the tool for it. No tool is definitelly wired to that type of test. That is the reason why it is not on the list. 

### Acceptance testing ###

Formal testing conducted to determine whether or not a system satisfies its acceptance criteria and to enable the customer to determine whether or not to accept the system. It is usually performed by the customer.[More info](https://www.guru99.com/user-acceptance-testing.html)

-   [Cucumber](https://cucumber.io) - BDD
-   [JGiven](http://jgiven.org) - BDD
-   [YatSpec](https://github.com/bodar/yatspec) - BDD
-   [Concordion](https://concordion.org)
-   [FitNesse](http://www.fitnesse.org)

### Accessibility Testing ###

Type of testing which determines the usability of a product to the people having disabilities (deaf, blind, mentally disabled etc). The evaluation process is conducted by persons having disabilities. [More info](https://www.guru99.com/accessibility-testing.html)

-   [Accessibility Developer Tools](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb?hl=en)
-   [AChecker](https://achecker.ca/checker/index.php)
-   [Wave](http://wave.webaim.org)
-   [TAW](https://www.tawdis.net)
-   [Accessibility Valet](http://valet.webthing.com/access/url.html)
-   [Quick Accessibility Page Tester](https://accessify.com/tools-and-wizards/accessibility-tools/favelets/quick-page-test/)
-   [aDesigner](http://www.eclipse.org/actf/downloads/tools/aDesigner/)

### Mutation testing ###

Method of software testing which involves modifying programs' source code or byte code in small ways in order to test sections of the code that are seldom or never accessed during normal tests execution. It is normally conducted by testers. [More info](https://www.guru99.com/mutation-testing.html).

-   [PIT](http://pitest.org) - Non functional testing, White box testing.
-   [MuJava](https://cs.gmu.edu/~offutt/mujava/) - Non functional testing, White box testing.
-   [JavaLanche](https://github.com/david-schuler/javalanche) - Non functional testing, White box testing.
-   [Major](http://mutation-testing.org) - Non functional testing, White box testing.
-   [Jumble](http://jumble.sourceforge.net) - Non functional testing, White box testing.
-   [Descartes](https://github.com/STAMP-project/pitest-descartes) - Non functional testing, White box testing.
-   [Jester](http://jester.sourceforge.net) - Non functional testing, White box testing.
-   [Judy](http://madeyski.e-informatyka.pl/tools/judy/) - Non functional testing, White box testing.

### Benchmark testing ###

-   [Java Microbenchmark Harness (JMH)](https://github.com/peterszatmary/jmh-benchmark-demo)
-   [Benchmark Framework 2.0 & TechEmpower](https://www.techempower.com/benchmarks/)

### Unit testing ###

-   [Junit]() - white box testing, unit testing, component testing, functional testing.
-   [ArchUnit](https://github.com/TNG/ArchUnit) - Non functional testing
-   [DBUnit](http://dbunit.sourceforge.net)

### Code covarage tools ###

-   [Jacoco]()
-   [Cobertura]()
-   [Clover]()

### Load testing ###

-   [Gatling]() - Non functional testing
-   [Apache JMeter]() - Functional testing, Non Functional testing

### Performance testing ###

-   [Gatling]() - Non functional testing
-   [Apache JMeter]() - Functional testing, Non Functional testing

### UI testing ###

-   [Serenity]()
-   [Selenium](https://www.seleniumhq.org)

### End to end testing ###

-   [Endly](https://github.com/viant/endly/)

### Other ###

-   [EasyMock](http://easymock.org)
-   [REST Assured]() - white box testing, black box testing, grey box testing, acceptance testing.
-   [Postman](https://www.getpostman.com)
-   [PowerMock](https://github.com/powermock/powermock)
-   [Mockito](https://site.mockito.org) Functional Testing
-   [TestNG](https://testng.org/doc/index.html)
-   [Spock](http://spockframework.org)
-   [Spring Test]() - Functional testing
-   [Arquillian]() - Functional testing
-   [Fit](http://fit.c2.com)


## Usefull links ##

-   [the-classification-of-kinds-of-software-testing](http://blog.qatestlab.com/2011/04/09/the-classification-of-kinds-of-software-testing/)
-   [classification-among-testing](https://www.softwaretestinggenius.com/classification-among-testing/)
-   [the-classification-of-types-of-software-testing](https://www.utest.com/articles/the-classification-of-types-of-software-testing)
-   [software-testing](https://www.guru99.com/software-testing.html)
-   [types-of-software-testing](https://www.softwaretestinghelp.com/types-of-software-testing/) 
-   [List of 100 Different Testing Types](https://www.guru99.com/types-of-software-testing.html)
-   [Martin Fowler - Is TDD Dead](https://martinfowler.com/articles/is-tdd-dead/)
-   [tdd-is-dead-long-live-testing](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html)

