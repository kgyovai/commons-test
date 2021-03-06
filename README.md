[![Build Status](https://travis-ci.org/centic9/commons-test.svg)](https://travis-ci.org/centic9/commons-test) [![Gradle Status](https://gradleupdate.appspot.com/centic9/commons-test/status.svg?branch=master)](https://gradleupdate.appspot.com/centic9/commons-test/status)
[![Release](https://img.shields.io/github/release/centic9/commons-test.svg)](https://github.com/centic9/commons-test/releases)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.dstadler/commons-test/badge.svg?style=flat)](https://maven-badges.herokuapp.com/maven-central/org.dstadler/commons-test) [![Maven Central](https://img.shields.io/maven-central/v/org.dstadler/commons-test.svg)](https://maven-badges.herokuapp.com/maven-central/org.dstadler/commons-test)

This is a small library of code-pieces that I find useful when writing tests.

It covers areas that I miss in JUnit itself e.g. for verifying compare()/hashCode()/equals() implementations and for multi-threaded tests.

## Contents
 
* MockSMTPServer - simulate an SMTP Server for testing code which sends emails
* MockRESTServer - simulate a HTTP Server for testing code which accesses other systems, e.g. to mock REST interfaces in tests
* TestHelpers - small utilities for testing things like equals(), hashCode(), toString(), compare() and implementations of Comparator, they ensure some things that the Java spec mandates
* ThreadTestHelpers - easily run unit tests multiple times in parallel to ensure the code does not contain hidden race conditions
* MemoryLeakVerifier - a simple way of adding memory leak assertions to unit tests
* TestEnvironment - handling temporary files/directories in a clean way, ensure that files are not locked any more at the end of the test

## Use it

### Gradle

    compile 'org.dstadler:commons-test:1.+'

## Change it

### Grab it

    git clone git://github.com/centic9/commons-test

### Create Eclipse project files

	./gradlew eclipse

### Build it and run tests

	cd commons-test
	./gradlew check jacocoTestReport

#### Licensing
* commons-test is licensed under the [BSD 2-Clause License].
* A few pieces are imported from other sources, the source-files contain the necessary license pieces/references.

[BSD 2-Clause License]: http://www.opensource.org/licenses/bsd-license.php
