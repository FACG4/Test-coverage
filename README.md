
# Test-coverage

### What are Istanbul and nyc?
##### Istanbul - a JS code coverage tool written in JS. It computes statement, line, function and branch coverage. with module loader hooks to transparently add coverage when running tests. Supports all JS coverage use cases including unit tests, server side functional tests and browser tests.

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

# Test-coverage


B.Why is test coverage useful?
1.It can assure the quality of test
2.It can help identify what portions of the code were actually touched for the release or fix
3.It can help to determine the paths in your application that were not tested
4.Prevent Defect leakage
5.Time, scope and cost can be kept under control
6.Defect prevention at an early stage of project life cycle
7.It can determine all the decision points and paths used in the application, which allows you to increase test coverage
8.Gaps in requirements, test cases and defects at unit level and code level can be found in an easy way




D. How would you use them to improve your testing?


review is very key thing in testing and each phase of testing review should be incorporate,testcases coverage should be cover with the scenario and scenario should be derived from requirement and this the flow of writing test cases and also review the test cases.

Testcase should be written to have focus of risk and the static and dynamic technique implemented as the measurement of test cases is the fault found which is actully increase the confidence.for writing the test cases many thing needs to keep focus as company to company process would be different but the concept of test case coverage should be define with the requirement and all the possible combination.

There are different type of test cases review process and its define as below

#1. Understand the fundamentle ,Before writting ( try to do some paper work before wrting test case )


#2. Do self review and try to find the improvement not mistake


#3. Ask developer/technicale expert for review.


#4. Do review updated testcase

