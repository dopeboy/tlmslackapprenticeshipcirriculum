# Lesson 2: Types of testing

In this lesson, we will go over the different types of testing used to verify software. Throughout this lesson, references will be made to a fictional chair company called Chairs Inc and also to a user registration module on a website.

## Do now

Suppose a new chair is being built at Chairs Inc. Come up with three consumer safety standards and then draft a test case for each one.

Now, suppose you sit on the user experience team. Draft three test cases that touch on the desired experience the user should have with the chair.

## Types

There are two different categories of testing: functional, and non-functional. Within each category, there are several types of testing.

## Functional

Functional tests "...focus on the business requirements of an application" [0]. In software, before a product is built, requirements are laid out and codified. (Depending on the type of company, this is handled by either the Product team or the Business Analysis team). Let's go over the most important types of functional tests.

### Unit tests

Unit tests "...isolate a section of code and verify its correctness. In procedural programming a unit may be an individual function or procedure" [1]. They tend to be automated and are usually performed by developers.

Suppose we're building a chair. The chair leg, seat, and back are all constructed independently. Before they are connected, we can unit test each piece. For example, we may test how sturdy the seat itself is by placing it on the ground and putting a weight on top of it.

In software, it's the same concept. Taking our user registration module, there are a lot of pieces involved when signing up a user including sending an email. A unit test here could verify that the service we use to send an email works in a timely fashion. We could write the test to compare what we send to the user with what is received. 

Unit tests are modular by nature which means you can run them in parallel. They double as a documentation source which can help newcomers learn how a code base works [1].

### Integration tests

An integration test is  "...where individual units are combined and tested as a group. The purpose of this level of testing is to expose faults in the interaction between integrated units" [2]. They tend to be automated and are usually performed by developers.

Taking the chair example from above, we would now test whether the legs of the chair fit into the seat. 

In software, we would test whether two separate pieces (they could be functions, services, etc) correctly connect together. Taking the user registration example from above, we could connect the process of creating a new in the backend with the process of sending an email to confirm registration. 

[Here's](https://giphy.com/gifs/unit-test-integration-3o7rbPDRHIHwbmcOBy?utm_source=iframe&utm_medium=embed&utm_campaign=Embeds&utm_term=http%3A%2F%2Fsoftwaretestingfundamentals.com%2Fintegration-testing%2F) a GIF that shows what happens when you pass your unit tests but fail your integration test.

### End-to-end tests

An end-to-end (E2E) test verifies whether an integrated system meets its requirements [3]. They come in automated and manual (human) forms. These tests are usually performed by an internal QA team.

Taking the chair example, suppose before we built our chair, we set out with a specification that it should withstand 100 pounds of weight. To test this system specification, once we've assembled the legs, seat, and back together, we would perform that the end-to-end testing. 

Going back to software with our same example from above, we wrote up specifications on how the user registration module should behave including the structure of the data that comes in, the model to be populated when creating a user, and the structure of the confirmation email. An E2E test for this module would involve inputting data into the frontend forms, injesting in our backend, creating a user, and then sending the confirmation email out. Each of these steps in isolation form unit tests. Sequencing pieces of them together form integration tests. Running it front to back forms our E2E test.

### User acceptance tests

A user acceptance test (UAT) verifies whether a product is ready for real world scenarios. It is performed by *real users*. It is the last stage of testing before the product is shipped.

Taking the chair example, this is when our assembled chair would be sat on by individuals we selected to test our product. These individuals are ideally selected at random and completely disconnected from the construction process of the chair. They'll report back any faults they find with the chair.

Taking our software example, this is when we bring outside testers to trial our product. These testers will typically know the requirements already or be given them. They'll tend proceed to use the product and record any errors they see. These are passed on to the development team, another release is made, and UAT begins again. Services like [Rainforest QA](https://www.rainforestqa.com/) play a useful role here. 

## Non-functional

Non-functional tests cover aspects like performance, usability, reliability, etc. They connect closer to the user's *satisfaction* rather than user's requirements [4]. Let's go over the most important types of non-functional tests.

### Performance

There are many way to test performance including loading testing, stress testing, spike testing, and scalability testing. Further reading is encouraged [here](https://www.softwaretestingclass.com/what-is-performance-testing/).

If we're building our user registration module, we care how much time elapses between submitting the form and seeing a new page confirming our registration.

The key takeaway here is that user engagement and interest drop as performance drops. We must ensure our product runs fast and achieving often means having including performant code and an appropriate infrastructure among other things.

### Usability

"Usability testing is the practice of testing how easy a design is to use on a group of representative users. It usually involves observing users as they attempt to complete tasks and can be done for different types of designs, from user interfaces to physical products" [5].

If we're building a chair, we care about the user's comfort and whether it is ergonomically sound for them. If it's a chair that involves assembly, we care about the design and instructions (think Ikea).

If we're building our user registration module, we care whether our users can understand our front end form easily. Do we have validation to assist when they choose a weak password? How is the validation performed: on the frontend so they are immediately made aware (but perhaps more stress inducing) or throught the backend where there's a longer delay? Design and user experience, among other disciplines, are pulled in for usability testing.

### Accessibility

Accessibility testing is a subset of usability testing. It is done so "...that the application being tested is usable by people with disabilities like hearing, color blindness, old age and other disadvantaged groups" [6]. One classic accessibility test is to verify screen reader compatibility. Screen readers will narrate over a page so that visually impaired users can still use it.

### Localization

When a product is made for an international audience, foreign speakers are consulted to perform translation services. Many times, as words or phrases are embedded into a product, the context can completely throw off their placement. Some languages use character sets that occupy a lot of screen real estate which might lead to cut off text or readabiity issues. This is where QA testing with foreign language experts is needed [7].

### Security

Assessing the security of a system is an entire field in itself. Most organizations have internal teams devoted to performing security testing. There has been a growing trend to separate security  testing from quality assurance. We encourage the reader to pursue further reading here.

## Summary

Functional testing refers to verifying a product against its requirements. In software, developers create a module and write/perform unit tests in parallel. Once this developer is satisfied, they commit their code to the larger base where tests are run verify whether their software successfully integrates with the software of their teammates'. End-to-end tests follow to verify whether the entire product works. Lastly, real users give the product a whirl.

Non-functional testing refers to verifying a product against user desire and comfort. Various factors surrounding performance, usability, security, UI, etc are tested here.

## Exit ticket

Suppose you are creating a mobile app like Instagram. Write all the functional and non-functional tests you would perform and including how you would perform them.

## References & Additional Reading

[0] - https://www.atlassian.com/continuous-delivery/different-types-of-software-testing

[1] - https://www.guru99.com/unit-testing-guide.html

[2] - http://softwaretestingfundamentals.com/integration-testing/

[3] - http://softwaretestingfundamentals.com/system-testing/

[4] - https://www.guru99.com/non-functional-testing.html

[5] - https://www.interaction-design.org/literature/topics/usability-testing

[6] - https://www.guru99.com/accessibility-testing.html

[7] - https://www.welocalize.com/6-reasons-localization-qa-testing-important/
