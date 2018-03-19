
# Test-coverage

A.What is test coverage?

Test coverage meaning

Testing coverage can have a different meaning in different context. Let’s discover those contexts one-by-one:

Product coverage – What aspects of the product did you look at?

Yes, when testing coverage is being measured in terms of product, the main area to focus on is – which areas of product you have tested and which remains untested?

Test Coverage, on the other hand, is testing every requirement

Example #1:

If “knife” is a product, you are testing; just do not concentrate on checking whether it cuts the vegetables/fruits properly. There are other aspects to look for such as – the user should be able to handle it comfortably.

Example #2:

If “notepad” is an application, you are testing, checking relevant features is a must thing.

But other aspects to be taken care are – application responds properly while using other applications simultaneously, the application does not crash when the user tries to do something unusual, the user is provided proper warning/error messages, the user is able to understand and use the application easily, help content is available when required.

If you don’t look into the mentioned scenarios, you can’t claim that the testing coverage for the application is complete.

requirements coverage – What requirements have you tested for?

If a product or application is developed very well but if it’s not matching with customer’s requirements then it’s of no use. Requirement coverage while testing is as important as product coverage.

Example #1 :

While testing a chat application, tester took care of all the important points like multiple users chatting in a group, two users chatting independently, all types of emoticons available, updates sent to user immediately etc. but forgot to look into requirement document, which clearly mentioned that when two users chat independently, video call option should be enabled.

Basic coverage criteria
There are a number of coverage criteria, the main ones being:[5]

Function coverage – Has each function (or subroutine) in the program been called?
Statement coverage – Has each statement in the program been executed?
Branch coverage – Has each branch (also called DD-path) of each control structure (such as in if and case statements) been executed? For example, given an if statement, have both the true and false branches been executed? Another way of saying this is, has every edge in the program been executed?
Condition coverage (or predicate coverage) – Has each Boolean sub-expression evaluated both to true and false?

For example, consider the following C function:

`int foo (int x, int y)`

`{`
`int z = 0;`

`if ((x > 0) && (y > 0))`
`{`

  `z = x;`

  `}`
`return z;`
`}`

Assume this function is a part of some bigger program and this program was run with some test suite.

If during this execution function 'foo' was called at least once, then function coverage for this function is satisfied.
Statement coverage for this function will be satisfied if it was called e.g. as foo(1,1), as in this case, every line in the function is executed including z = x;.
Tests calling foo(1,1) and foo(0,1) will satisfy branch coverage because, in the first case, both if conditions are met and z = x; is executed, while in the second case, the first condition (x>0) is not satisfied, which prevents executing z = x;.
Condition coverage can be satisfied with tests that call foo(1,0) and foo(0,1). These are necessary because in the first cases, (x>0) evaluates to true, while in the second, it evaluates false. At the same time, the first case makes (y>0) false, while the second makes it true.

if a and b then
Condition coverage can be satisfied by two tests:

a=true, b=false
a=false, b=true

**B.Why is test coverage useful?**

1.It can assure the quality of test.

2.It can help identify what portions of the code were actually touched for the release or fix.

3.It can help to determine the paths in your application that were not tested.

4.Prevent Defect leakage.

5.Time, scope and cost can be kept under control.

6.Defect prevention at an early stage of project life cycle.

7.It can determine all the decision points and paths used in the application, which allows you to increase test coverage.

8.Gaps in requirements, test cases and defects at unit level and code level can be found in an easy way.

What Test Coverage does?

1.Finding area of a requirement not implemented by a set of test cases
2.Helps to create additional test cases to increase coverage
3.Identifying a quantitative measure of test coverage, which is an indirect method for quality check
4.Identifying meaningless test cases that do not increase coverage


### What are Istanbul and nyc?
##### Istanbul - a JS code coverage tool written in JS. It computes statement, line, function and branch coverage. with module loader hooks to transparently add coverage when running tests. Supports all JS coverage use cases including unit tests, server side functional tests and browser tests.

##### Features:
* Well-tested on node (prev, current and next versions) and the browser (instrumentation library only).
* Can be used on the command line as well as a library.
* Multiple report formats: HTML, LCOV, Cobertura and more.
##### > Getting started
`$ npm install -g istanbul`

##### > To see it in action
Say you have a test script test.js that runs all tests for your node project without coverage.

Simply:

`$ cd /path/to/your/source/root`

`$ istanbul cover test.js`
<p align="center">
  <img src="istanbul.png" width="350"/>
</p>
and this should produce a `coverage.json,` `lcov.info` and `lcov-report/*html` under `./coverage`

##### The command line
`$ istanbul help`

gives you detailed help on all commands.

Why the funky name?

Since all the good ones are taken.
 Comes from the loose association of ideas across coverage, carpet-area coverage, the country that makes good carpets and so on...

# NYC

The NYC Node module can be used to generate test coverage reports. These reports will track how much of the application code is covered by unit tests. If any code is not being called or tested, NYC will indicate the ‘uncovered’ lines in both the command line and the generated reporting page.

## Instrumenting your code
You can install nyc as a development dependency and add it to the test stanza in your package.json.

`npm i nyc --save-dev`

`{
  "scripts": {
    "test": "nyc mocha"
  }
}`

Alternatively, you can install nyc globally and use it to execute npm test:

`npm i nyc -g`

`nyc npm test`
