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
