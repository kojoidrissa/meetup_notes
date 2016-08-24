# Introduction to Software Testing
-  https://www.meetup.com/Google-Developers-Group-Houston/events/232998793/
-  https://github.com/gdghtown/IntroToTesting

## Why test?
-  Cost/benefit analysis on what to test, when and how
    -  risk assessment
-  Functional vs. Non functional behavior to test
-  How much does your *code* need to change before you test again?
-  How much does a *dependency* need to change before you test again?
    -  libraries, compilers, OS, APIs, etc.

## How to test

### Manual
The path to madness, in most cases

### Automated

## What to test
-  Whole system?
    -  acceptance testing
    -  Time-consuming; brittle; hard to automate; "combinatorial explosion"
-  "A Big chunk"
    -  integration testing
    -  still brittle; harder to set up
-  Tiny Pieces
    -  unit tests
    -  fast; no "connected" testing; each piece could pass while the whole fails
-  Tests that interact w/ code you DON'T control aren't really "unit" tests anymore.
    -  surrounding your "known system" with 'doubles' helps you isolate your tests

### Test Doubles
-  SUT: System Under Test
-  DOC: Depended on Component
-  Indirect Output: Any message sent to a DOC; SUT doesn't see these directly
-  Indirect Input: Any message received from a DOC; SUT doesn't see these directly
-  Double: any DOC that's controlled by the test (mock object?)
    -  Mock: tests indirect outputs (fails immediately)
    -  Spy: tests indirect outputs (doesn't fail immediately)
    -  Stub: provides indirect inputs to SUT
    -  Fake: full implementation of DOC, but simplified & customizable (Mockingbird)

### Benefits
-  Faster tests: You've isolated the specific code you're trying to test
-  More test coverage: you can test a larger % of your system
-  You know exactly where the problems are
-  isolation from error sources and extraneous details
-  ability to simulate errors
    -  Michael Feathers: Working with Legacy Code (code w/o tests)
-  more progress w/ less info & coordination (due to fakes/mocks/stubs); interface discovery or emergent design

-  Constructor argument vs. Function argument (`player` passed to `Turn_Engine`)

## Issues
- Test-induced Design Damage (the OTHER TDD): remain aware of the *cost* of testing vs. it's *benefit*.
- Complitcated test set up
- Law of Demeter violations
- Don't mock 'value' objects (constants, strings, etc)
- Change-Detector tests: test that breaks w/ ANY change to the system
