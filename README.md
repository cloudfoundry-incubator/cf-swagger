CF-Swagger [![Build Status](https://travis-ci.org/maximilien/cf-swagger.svg?branch=master)](https://travis-ci.org/maximilien/cf-swagger#)
==============================

[![Join the chat at https://gitter.im/maximilien/cf-swagger](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/maximilien/cf-swagger?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Collection of Swagger descriptions and applications for CloudFoundry APIs

This tool is licensed under the [Apache 2.0 OSS license](https://github.com/maximilien/i18n4go/blob/master/LICENSE). We'd love to hear from you if you are using, attempting to use, or planning to use this tool. 

Two additional ways, besides Gitter or Slack chat above, to contact us:

1. Feel free to [open an issue (good or bad)](https://github.com/maximilien/i18n4go/issues) here on Github.
2. Send email to `cf.swagger` at the Gmail domain.

## Getting Started
------------------

### Overview Presentations, Talks, Blogs
----------------------------------------

* Overview presentation on September 16th, 2015. Slides ([PDF](https://github.com/maximilien/presentations/blob/master/2015/cf-swagger/releases/cf-swagger-v0.7.0.pdf) and [PPTX](https://github.com/maximilien/presentations/blob/master/2015/cf-swagger/releases/cf-swagger-v0.7.0.pptx)), [video](https://www.youtube.com/watch?v=S_NdzSj1syg)


### Getting Started
-------------------

Assuming you have a valid [Golang 1.4.2](https://golang.org/dl/) or [later](https://golang.org/dl/) installed for your system, you can quickly get the latest `i18n4go` executable by running the following `go` command:

```
$ go get ...
```

TODO: add rest of how to get going

### Cloning and Building
------------------------

Clone this repo and build it. Using the following commands on a Linux or Mac OS X system:

```
$ mkdir -p i18n4go/src/github.com/maximilien
$ export GOPATH=$(pwd)/i18n4go:$GOPATH
$ cd i18n4go/src/github.com/maximilien
$ git clone https://github.com/maximilien/i18n4go.git
$ cd i18n4go
$ ./bin/build
```

NOTE: if you get any dependency errors, then use `go get path/to/dependency` to get it, e.g., `go get github.com/onsi/ginkgo` and `go get github.com/onsi/gomega`

The executable output should now be located in: `out/i18n4go`. Place it wherever you want, e.g., `/usr/local/bin` on Linux or Mac OS X.

You can now use the `i18n4go` executable to issue some of the typical i18n tooling processes.

### Running Tests
-----------------

You should run the tests to make sure all is well, do this with: `$ ./bin/test` in your cloned repository.

The output should be similar to:

```
$ bin/test

 Cleaning build artifacts...

 Formatting packages...

 Integration Testing packages:
ok  	github.com/maximilien/i18n4go/integration/checkup	1.571s
ok  	github.com/maximilien/i18n4go/integration/create_translations	1.542s
ok  	github.com/maximilien/i18n4go/integration/extract_strings	1.694s
ok  	github.com/maximilien/i18n4go/integration/fixup	1.657s
ok  	github.com/maximilien/i18n4go/integration/merge_strings	1.645s
ok  	github.com/maximilien/i18n4go/integration/rewrite_package	1.853s
ok  	github.com/maximilien/i18n4go/integration/show_missing_strings	1.590s
?   	github.com/maximilien/i18n4go/integration/test_helpers	[no test files]
ok  	github.com/maximilien/i18n4go/integration/verify_strings	1.701s

 Vetting packages for potential issues...

SWEET SUITE SUCCESS
```

### Running TCK
---------------

You should run the tests to make sure all is well, do this with: `$ ./bin/test` in your cloned repository.

The output should be similar to:

```
$ bin/test

 Cleaning build artifacts...

 Formatting packages...

 Integration Testing packages:
ok  	github.com/maximilien/i18n4go/integration/checkup	1.571s
ok  	github.com/maximilien/i18n4go/integration/create_translations	1.542s
ok  	github.com/maximilien/i18n4go/integration/extract_strings	1.694s
ok  	github.com/maximilien/i18n4go/integration/fixup	1.657s
ok  	github.com/maximilien/i18n4go/integration/merge_strings	1.645s
ok  	github.com/maximilien/i18n4go/integration/rewrite_package	1.853s
ok  	github.com/maximilien/i18n4go/integration/show_missing_strings	1.590s
?   	github.com/maximilien/i18n4go/integration/test_helpers	[no test files]
ok  	github.com/maximilien/i18n4go/integration/verify_strings	1.701s

 Vetting packages for potential issues...

SWEET SUITE SUCCESS
```

## Troubleshooting / FAQs
-------------------------

None for now. Submit questions/comments as issues and we will update here

### Filing Bugs
---------------

##### For simple bugs (eg: text formatting, help messages, etc), please provide

- the command options you ran
- what occurred
- what you expected to occur

##### For panics and other crashes, please provide

- the command you ran
- the stack trace generated (if any)
- any other relevant information

## Cloning the repository
-------------------------

1. Install [Go](https://golang.org)
1. Clone (Forking beforehand for development).
1. [Ensure your $GOPATH is set correctly](http://golang.org/cmd/go/#hdr-GOPATH_environment_variable)

## Building
-------------

1. Run `./bin/build`
1. The binary will be built into the `./out` directory

Optionally, you can use `bin/run` to compile and run the executable in one step.

## Developing
-------------

1. Run `go get golang.org/x/tools/cmd/vet`
2. Run `go get github.com/xxx ...` to install test dependencies (as you see errors)
1. Write a [Ginkgo](https://github.com/onsi/ginkgo) test
1. Run `bin/test` and watch the test fail
1. Make the test pass
1. Submit a pull request

## Contributing
---------------

* We gratefully acknowledge and thank the [current contributors](https://github.com/maximilien/i18n4go/graphs/contributors)
* We welcome any and all contributions as Pull Requests (PR)
* We also welcome issues and bug report and new feature request. We will address as time permits
* Follow the steps above in Developing to get your system setup correctly
* Please make sure your PR is passing Travis before submitting
* Feel free to email me or the current collaborators if you have additional questions about contributions
* Before submitting your first PR, please read and follow steps in [CONTRIBUTING.md](CONTRIBUTING.md)

## Managing dependencies
-------------------------

* All dependencies managed via [Godep](https://github.com/tools/godep). See [Godeps/_workspace](https://github.com/maximilien/i18n4go/tree/master/Godeps/_workspace) directory on master

### Short `godep` Guide
* If you ever import a new package `foo/bar` (after you `go get foo/bar`, so that foo/bar is in `$GOPATH`), you can type `godep save ./...` to add it to the `Godeps` directory.
* To restore dependencies from the `Godeps` directory, simply use `godep restore`. `restore` is the opposite of `save`.
* If you ever remove a dependency or a link becomes deprecated, the easiest way is probably to remove your entire `Godeps` directory and run `godep save ./...` again, after making sure all your dependencies are in your `$GOPATH`. Don't manually edit `Godeps.json`!
* To update an existing dependency, you can use `godep update foo/bar` or `godep update foo/...` (where `...` is a wildcard)
* The godep project [readme](https://github.com/tools/godep/README.md) is a pretty good resource: [https://github.com/tools/godep](https://github.com/tools/godep)

## Current conventions
-----------------------

* Basic Go conventions
* Strict TDD for any code added or changed
* Go fakes when needing to mock objects

(*) these items are in the works, we will remove the * once they are available