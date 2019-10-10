# FizzBuzz

[![Build Status](https://travis-ci.org/steandj/fizzbuzz.svg?branch=master)](https://travis-ci.org/steandj/fizzbuzz)

(See that "failing" image above? That's intentional! You can fix that and get it to pass in your fork of this project.)

This is an introduction to TDD (Test-Driven Development) using the simple FizzBuzz program. This repository will provide tests and stub methods.

## Why FizzBuzz?

According to the 2007 article [Why Can't Programmers.. Program?](https://blog.codinghorror.com/why-cant-programmers-program/) by Jeff Atwood, many applicants for programming or software development jobs are incapable of writing even simple programs on demand.

An example of such a program is FizzBuzz.

## Setup

Make sure you configure a Python virtual environment in your workspace, e.g.:

    cd fizzbuzz
    python3 -m venv venv
    source venv/bin/activate

Install the required Python libaries:

    pip3 install -r requirements.txt

Run the unit tests:

    python -m unittest discover -v

Did all the tests _fail_ but produce no errors? If so: perfect!

## Specification

In this example, the program will take one input:

n - a positive integer

The program should produce the following output:

1. Print a line for every number from 1 to n
2. For numbers divisible by 3 (without remainder), print Fizz instead of the number
3. For numbers divisible by 5 (without remainder), print Buzz instead of the number
4. For numbers divisible by both 3 _and_ 5 (without remainder), print FizzBuzz instead of the number.

## TDD (Test-Driven Development)

Test-driven development is a practice in which the developer writes unit tests prior to writing the code itself. This has a number of advantages, including but not limited to:

* Unit tests aren't an afterthought
* Developers consider _how_ to test functions/methods
* Developers can refactor or add features with confidence, because the unit tests serve as regression tests
* Unit tests are actually written at all

### Red, Green, Refactor (Repeat)

The phrase _Red, Green, Refactor_ is often used when talking about the practice of TDD. The first thing you do, as a developer, is write _one_ stub method and one or more unit tests for that method.

Then you run the test and watch it fail (RED).

It's important that the tests fails. If the test passes, that means the test is _vacuous_: it's not testing anything important.

(I personally believe that it is imporant for another reason: failure hurts, and it's easy to take it personally and be discouraged by failure. But in this particular case, you _want_ it to fail. Besides, success never comes before a series of failures! Learn to accept failure as a step to success.)

After you have a confirmed failing test, develop the method. Run another test. If your test passed, congratulations: you've reached GREEN!

(This might be a good time to commit your code to your Git repository.)

So what is the REFACTOR step? Often our first attempt to write code that passes a test won't be pretty. Now that you have something that works, you can clean up messy code, add any necessary comments, improve variable names, etc. The great part is, it will be easy to make sure your refactored code still passes the unit test.

See [The Cycles of TDD](https://blog.cleancoder.com/uncle-bob/2014/12/17/TheCyclesOfTDD.html) by Robert C. Martin, AKA Unble Bob, for more detail. Some people, as you can tell from that article, have spent a long time thinking about Test-Driven Development.

## Continuous Integration (CI)

There are a variety of tools that can run unit tests (and other tests) automatically when you push changes to your repository. In this example, we're using [Travis CI](https://travis-ci.org/).

Once you enable Travis CI for your GitHub account and add your fork of the fizzbuzz repository in Travis CI, you can add update the "Build Failing" image in this repository.

Use the following as a template, replacing `github_username` with your username:

    [![Build Status](https://travis-ci.org/github_username/fizzbuzz.svg?branch=master)](https://travis-ci.org/github_username/fizzbuzz)

If your tests are all passing, the image should change to a green "Build Passing" message!
