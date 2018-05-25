---
layout: post
title: "Stub vs Mock in Unit Testing"
date: 2017-07-19 19:28
categories: Programming
---

## Concept
A testing is involved with two types of object
- SUT(System under test) object
- collaborator object

## State verification style
- Check the result of the method under testing
  - the state of the object under testing
  - the state of its collaborators

## Behavior verification style
- Check the state of object under testing as state verification style
- Check the order of method call of its collaborators
- Check the input parameters and the result of the methods of collaborators


## Conclusion
The difference is the state verification focuses on the result of the method under testing. While the behavior verification focuses on the order of calls to the collaborator objects. That is how the exercised method  interact with other objects.

## Test double
- **Dummy objects** are passed around but never actually used. Usually they are just used to fill parameter lists
- **Fake objects** actually have working implementation, but usually take some shortcut which make them not suitable for production
- **Stub objects** provide canned answers to calls made during the test, usually not responding at all to anything outside what's programmed in for the test.
- **Spies** are stubs that also record some information based on how they were called. One form of this might be an email service that records how many message it was sent.
- **Mocks** are objects are initialized with expectation which forms a specification of the calls that they are expected to receive.

## Reference
- https://martinfowler.com/articles/mocksArentStubs.html
