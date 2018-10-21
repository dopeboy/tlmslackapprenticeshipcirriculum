# Lesson 0:  Frontend testing tools for the web

We use a suite of tools to test web applications. In this lesson, we'll talk about the types of tools that come in a suite and a brief overview of how they work.

## Do now

Let's do a quick refresher. What is unit testing? What is end-to-end testing? Give an example of each that does not involve software.

## Assertion libraries

When we write tests, we set some things up, we run the part we want to test, and then we compare the result we get with the expected one. Assertion libraries makes it easier to perform the last step.They take a lot of code that would otherwise be duplicated and pack them into easy to read, reusable functions. 

For example, suppose we built a calculator application and wanted to test whether the application checks that operand are numbers that we can perform arithmetic on. If we wrote this comparison from scratch, it might look like:
```
if (typeof operand !== "number" || !isFinite(operand)) {
    throw new InvalidArgumentException(`${operand} should be a number`);
}
```

We'd have to duplicate this code many times over. It also misses a good opportunity for modular code; verifying the type of a variable should be a generic operation[0]. With an assertion library like [Chai](https://www.chaijs.com/), we could simplify this to [1]

```
var assert=chai.assert;
assert.isFinite(operand);
```

## Testing frameworks

A testing framework packages an assertion library, a testing environment/runner, and a testing structure together. When we write tests, we start at this level. There are several testing frameworks including [Mocha](https://mochajs.org/), [Jest](https://jestjs.io/), [Jasmine](https://jasmine.github.io/), [Enzyme](https://airbnb.io/enzyme/) and [Cypress](https://cypress.io). Here are how two unit tests would look like in Mocha [2]:

```
const {describe, it} = require('mocha')
const {expect} = require('chai')
const calculator = ...

describe('calculator', function () {
    const stream = ... // Access the data in the calculator 

    it('should show initial display correctly', () => {
        expect(calculator.initialState.display).to.equal('0') // This is Chai
    })
    
    it('should replace 0 in initialState', () => {
        expect(stream('4').display).to.equal('4') // This is Chai
    })
```

## Test runners

Most test frameworks package a test runner inside of them. A test runner is a piece of software that "...creates a fake server, and then spins up tests in various browsers using data derived from that fake server" [0]. The defintion of "fake server" can vary widely and affects the quality of the test environment. Some test frameworks spin up a runner that hits a representation of a DOM (see [JSDOM](https://github.com/jsdom/jsdom)). Some frameworks, like [Selenium](https://www.seleniumhq.org/), have a runner that makes calls to a browser's native API. Other frameworks, like Cypress, run directly inside the browser. There are pros and cons to each approach between speed, accuracy, etc. 

## Visual testing tools

Visual testing is a relatively new type of testing to help with the greater complexity we're seeing in the frontend. While we can test for functionality, how can we test whether the fonts, alignment, colors, etc are correct? We could check the rendered output against a baseline but given the massive amount of different states to account for, this approach can become too burdensome. 

Visual testing works by taking a snapshot of a view and comparing it against the baseline. The snapshot can take on different forms. Some solutions literally take an image snapshot and perform a pixel by pixel diff against a baseline. Other solutions render the page across different browsers, resolutions, etc and save the final representation [3]. [Applitools](https://applitools.com/), [Chromatic](https://www.chromaticqa.com/), and [Screener](https://screener.io/) are examples of visual testing tools. 

## Summary

Most test frameworks will decide which assertion library, runner, etc you will use. It is important, as a developer, to stay on top of the tooling changes occuring in this field. Ten years ago, Selenium ruled the day. Today, tools like Cypress and Enzyme are picking up speed. There is a whole new category being created by companies creating cloud hosted visual testing tools. 


## References & Additional Reading

[0] - https://matthiasnoback.nl/2018/09/assertions-and-assertion-libraries/

[1] - https://www.chaijs.com/api/assert/

[2] - https://hackernoon.com/testing-your-frontend-code-part-ii-unit-testing-1d05f8d50859

[3] - https://blog.hichroma.com/visual-testing-the-pragmatic-way-to-test-uis-18c8da617ecf