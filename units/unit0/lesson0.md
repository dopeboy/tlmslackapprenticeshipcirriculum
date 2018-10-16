# Lesson 0: QA vs QC vs Testing

In this lesson, we will go over what Quality Assurance (QA), Quality Control (QC), and Testing is. Throughout this lesson, references will be made to a fictional chair company called Chairs Inc.

## Do now

On paper, write down the words that come to your mind when you hear QA, QC, and Testing.

## Quality Assurance

**Quality Assurance** is defined as the "set of activities designed to ensure that the development and/or maintenance process is adequate to ensure a system will meet its objective" [0].

At Chairs Inc, QA would be the set of processes designed to ensure that the chairs made are sturdy, comfortable to sit on, safe to transport, don't send toxic fumes, etc. The architects who craft the chairs may run safety checks at different stages as a chair is constructed. Some of these checks may be required to satisfy rules drafted internally at Chairs Inc. Some of these checks may be required to satisfy regulations mandated by the government. The act of creating these processes and ensuring a company follows them in QA.

In software, an example of QA would be setting up a culture of Test Driven Development (TDD). Many teams require their developers to write tests along with the code that they produce so that they are self verifying their work. Many times, code will not be considered for review until it has tests associated with it; this requirement (sometimes cultural, sometimes written) is an example of QA. Another example of is the process an organization puts in place around verifying code. This gets defined by management; rules and protocols are typically put in place such that (1) there is a staffed QA team that is responsible for performing test work and (2) all teams must receive a sign-off from the QA team.

## Quality Control

**Quality Control** is defined as "a set of activities designed to evaluate a developed work product" [0].

At Chairs Inc, as a chair is designed, various specifications are drafted. These requirements are codified into a test plan. After the chair is made, the test plan is executed. Afterwards, real humans might be involved for a user acceptance kind of testing. These sub processes of drafting requirements, testing against them, etc are part of QC.

In software, we engage in a similar process. As we're designing a feature, QA members will draft requirements. As the feature is nearing completion, they'll start testing it against those requirements. This flow and sequence is part of QC.

## Testing

**Testing** is defined as "the process of executing a system with the intent of finding defects" [0].

At Chairs Inc, the QA team will examine the set of requirements. An example might be that a chair must be able to hold 300 pounds. The team responsible for testing the chairs will perform the test (by say, placing a weight on it) and analyze if it remains sturdy. This is an example of testing.

In software, the same process applies. The QA team will examine a requirement, pull up a testing tool (if necessary) and run the test using the tool (or manually). **You will be involved at this stage during your apprenticeship**.

## Summary

<img src='https://i.imgur.com/VLK09As.png'/> [1]


## Exit ticket

Suppose you are creating a chat client and you are adding a feature that lets admins delete each other's posts (as opposed to just their own). What sort of tests would you write?

## References & Additional Reading

[0] - http://www.mosaicinc.com/mosaicinc/rmThisMonth.asp

[1] - https://www.altexsoft.com/media/2016/10/Quality-Assurance-Quality-Control-and-Testing-%E2%80%94-the-Basics-of-Software-Quality-Management-Whitepaper.pdf

https://testing.googleblog.com/2007/03/difference-between-qa-qc-and-test.html