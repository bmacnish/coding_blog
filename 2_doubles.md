# Test doubles in RSpec

## What is a double?
##### Double is an umbrella term for an object that stands in for the real object in a test.

A common analogy is that a test double is a like a stunt double standing in for an actor on a film set. A stunt double has a different set of skills to the actor they are doubling for and when stunt work is required the double will perform the task rather than the actor. Similarly, test doubles can be used in ways that the real object making them useful in testing senarios when we want particular kinds of behaviours.

Using test doubles helps us isolate unit tests by standing in for classes and methods that are undefined, unavaliable, expensive or difficult to work with.

The langugae around these ideas is often used inexactly and interchangeably. For the purposes of this explanation we're going to use some definitions of types of test doubles from an article by [Martin Fowler](http://martinfowler.com/articles/mocksArentStubs.html).

This is not an exhaustive list of test doubles but these are the ones we will discuss further.

**Dummy** – an object that is only being used as a placeholder, it doesn't and can't respond to any messages. You use a dummy when you need to pass an object into a mathod as an argument but you don't plan on using any of its functionality in your test.
# Note: dummy alone can't respond, you can stub out methods on it.

**Stub** – an object can have a method on it stubbed, this stubbed method will be setup to provide a canned response when called.
# Note: stub a real method on a real object or on a dummy object

**Mock** – an object that has been given a method or list of methods that it must/must not receive during the test to allow the test to pass.

**Spy** – an object that has been set up to record all the methods it receives during a test, it can then report back on what it received during the expectation part of the test.

## Resources
RSpec Documentation
https://relishapp.com/rspec/rspec-mocks/docs/basics/test-doubles

Doubles in RSpec
https://www.tutorialspoint.com/rspec/rspec_test_doubles.htm

Introduction to stubs, mocks and spies with clear examples
https://about.futurelearn.com/blog/stubs-mocks-spies-rspec

Chapter 13, Effective Testing with RSpec 3
https://learning.oreilly.com/library/view/effective-testing-with/9781680502770/f_0103.xhtml#chp.understanding-test-doubles
