# testRunner
karma is a test runner develped by google angular development team.
It follow TTD(Test driven deveopment) TDD is an evolutionary approach to development which combines test-first development 
where you write a test before you write just enough production code to fulfill that test and then refactor the code to pass the test.

Why TTD

Now many will ask that I am not using TDD but my development is going well. I‘m delivering product in time with quality and good things. To answer your question, let me remind you first “No process in this world is the best in all cases”. Every process has its merits and demerits. Even if nowadays waterfall model is appropriate for some kind of systems. So my focus is not TDD is best over non-TDD approach. Rather TDD offers some sort of benefits that we can leverage:

1. Automated testing: Nowadays as system is getting bigger and complex, people are moving to automated testing. Automated system makes the testing much more easier and faster. Manual testing is slower and needs human interaction which is error-prone. Automated testing makes sure any particular test is not missing every time we test the system, whereas human may leave a test out mistakenly during testing process.

2. Better to test New/Modified Functionality: With manual testing whenever you add new functionality or modify existing functionality, QA personal needs to test all systems that may be affected due to the modification which may be time-consuming. This may also leave a hidden bug in the system after modification. With TDD whenever a new functionality is added or existing functionality is modified, the whole set of tests in the system is run to make sure existing tests are passed. This makes sure that existing functionality is not broken.

3. Developer’s confidence: With TDD, developers are more safe to change the system as any inappropriate changes will make some tests to fail. With non-TDD system developers needs to take more care to change existing system as the new change may fail other functionality. But with TDD developers can do so easily as after modification if developer runs the test he/she will find immediately that the change has failed some other tests (i.e. some other part of the system).

4. Manual testing stage is shortened: In non-TDD development, as soon as developers prepare a build, QA personal starts testing. This manual testing takes a reasonable amount of time and increases the time to deliver the product from the build time. With TDD, a major part of the system is tested during development and needs lesser QA involvement in the time between build and final delivery of the product.

5. Alternative Documentation: Unit tests are kind of documentation to system. Each unit test tells about an individual requirement to the module or system. For example, the following test ensures that only a logged in user with proper balance can buy an item when the item exists in stock. This test reflects a user aspect scenario of the system.


    var CheckUserCanNotSeeDetailsWithoutLogin = function()      {       
        LoginToTheSystem();       
        goToMyOrdersPage();       
        MakeSureItemExsitsInStock();       
    }


6. Better way to fix bugs: In TDD approach when QA finds a bug, developer first writes a test that generates the bug (that is the test will fail due to this bug). Then developer modifies code to make sure that the test is passed (i.e., the bug is fixed). This approach makes sure that next time the bug will not appear in the system as a test is written in the system to take care of the bug.

7. Repetition of the same bug reduced: The way bugs are fixed in TTD is described in point 6. With TDD once a bug is found, it's put under test. So every time you run the whole test in the system, the tests associated with the bug are run and make sure the bugs are not generated again.
