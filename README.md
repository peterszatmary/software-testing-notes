# Software testing notes #

## Introduction ##

### Software needs tests at least because ###

-   to know that software works as intended
-   prevent software from bugs or find bugs asap
-   tests helps a lot with big changes in code as refactoring, migrations etc.

### As i see very important things regarding testing are ###

-   you would like to **write neither many nor not enough tests**. Balance is the key. Because to much tests costs time. And time means money. Not enough code leads to many bugs, production problems, unsatisfied customer that lead to more fixing less writing new code thatwhat cost also time and can lead to lossing the customer (worst scenario). 

-   you would like to **write tests that are working** !! You would like to have stronger tests than weak (weaker) tests. So question is, which testing strategies to choose and why? Because bad testing strategies could lead also to same results as many or not enough tests (result mentioned earlier).

-   you would like **automate your tests** to run them periodically. 

-   you would like to **do so less manual tests than it is possible** because they are time consuming and cannot be repeated immediately / on demand. Each repetition consumes a lot of time in comparison with automated tests.

### Personal notes ###

-   I believe in **multi-layered testing strategy**. That means you are using more than one type of tests to achieve the main goal - to have software properly tested. 
-   I dont believe in **hunting bigger code coverage percentage number** ! Why bigger number if your tests are weak or wrong ? First think about things like is my test correct ? Is it my test doing what i think ? It is my test testing properly ? Is it my test working just with correct inputs or also with wrong ones ?
- **I am not really fan of TDD**, regardless if [it is dead](https://martinfowler.com/articles/is-tdd-dead/) [or not](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html). Just philosophical question here (I would like not spend so much time here with TDD so just one question) : Why start with something that is not a main product (test) instead of something that is major (software) ? 


## Testing categories ##

There are so many test types. It is of course possible group different tests to categories. To have better picture i start with categories first. 

-   **Object of testing** - Functional testing, Non functional testing.
-   **Knowledge of the system** - Black box testing, White box testing, Grey box testing.
-   **Degree of automation** - Automated testing, Manual testing, Semi-automated testing.
-   **Degree of isolation components** - Component (Unit) testing, Integration testing, System / End to end testing.
-   **Basis of positive scenario** - Positive testing, Negative testing.
-   **Time of testing** - Alpha testing, Beta testing, Acceptance testing.
-   **Degree of preparedness to be tested** - documentation testing, Ad hoc testing.
-   **Functional testing** - Unit testing, Acceptance testing, White box testing ...
-   **Non functional testing** - Security testing, Load testing, Stress testing, Penetration testing, Smoke testing ...


### Testing tools / frameworks (Java) ###

-   [Junit]() - white box testing, unit testing, component testing, functional testing.
-   [Cucumber]() - white box testing, black box testing, grey box testing, acceptance testing, BDD.
-   [REST Assured]() - white box testing, black box testing, grey box testing, acceptance testing.
-   [Serenity]() - UI Testing
-   [JGiven](http://jgiven.org) - BDD.
-   [Selenium](https://www.seleniumhq.org) UI testing.
-   [Postman](https://www.getpostman.com)
-   [PowerMock](https://github.com/powermock/powermock)
-   [Mockito](https://site.mockito.org) Functional Testing
-   [TestNG](https://testng.org/doc/index.html)
-   [Spock](http://spockframework.org)
-   [Spring Test]() - Functional testing
-   [DBUnit](http://dbunit.sourceforge.net)
-   [Apache JMeter]() - Functional testing, Non Functional testing
-   [Arquillian]() - Functional testing
-   [Gatling]() - Non functional testing
-   [ArchUnit](https://github.com/TNG/ArchUnit) - Non functional testing
-   [Java Microbenchmark Harness (JMH)](https://github.com/peterszatmary/jmh-benchmark-demo)
-   [PIT](http://pitest.org) - Mutation Testing, Non functional testing, White box testing,
-   [Jacoco]() - Code coverage
-   [Cobertura]() - Code coverage
-   [Clover]() - Code coverage


### Usefull links ###

-   [the-classification-of-kinds-of-software-testing](http://blog.qatestlab.com/2011/04/09/the-classification-of-kinds-of-software-testing/)
-   [classification-among-testing](https://www.softwaretestinggenius.com/classification-among-testing/)
-   [the-classification-of-types-of-software-testing](https://www.utest.com/articles/the-classification-of-types-of-software-testing)
-   [software-testing](https://www.guru99.com/software-testing.html)
-   [types-of-software-testing](https://www.softwaretestinghelp.com/types-of-software-testing/) 
-   [types-of-software-testing](https://www.guru99.com/types-of-software-testing.html)
-   [Martin Fowler - Is TDD Dead](https://martinfowler.com/articles/is-tdd-dead/)
-   [tdd-is-dead-long-live-testing](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html)

