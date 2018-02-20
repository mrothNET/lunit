# lunit - Unit Testing Framework for Lua.

* Provides 27 assert functions, and a few misc functions
  for usage in an easy unit testing framework.
* Comes with a test suite to test itself. 
  The testsuite consists of approximately 710 assertions.
* Licensed under the MIT license.



## Actual state

This package is not maintained anymore. It is here for pure
historically reasons for your interest.



## Example

Source: `example.lua`:

	require "lunit"

	module( "my_testcase", lunit.testcase )

	function test_success()
	  assert_false( false, "This test never fails.")
	end

	function test_failure()
	  fail( "This test always fails!" )
	end
	
	lunit.main(...)

Run tests:

	# lua example.lua 
	    F.

	2 Assertions checked.

	  1) Failure (my_testcase.test_failure):
	example.lua:10: failure
	example.lua:10: This test always fails!

	Testsuite finished (1 passed, 1 failed, 0 errors).




## Homepage

https://www.mroth.net/lunit



## Source code

[GitHub repository:](https://github.com/mrothNET/lunit)

	git clone https://github.com/mrothNET/lunit.git



### History

#### Up to today

- lunit no longer depends on `lunit.sh`. The script moved to
  the extra-directory.

####  2009-11-05 / Release 0.5

- New test function `assert_error_match()`.
- lunit shell script returns an error code on failed tests.
- Be more compatible with Darwin / Mac OS X.
- Bug fixes.

#### 2008-01-05 / Release 0.4

- Mostly complete rewrite.
- Lua-5.1 only.

####  2004-08-22 / Release 0.3 (alpha)

- New function `lunit.wrap()` to wrap a single function in a
  complete test case.
- Now a backtrace is printed, if an error or failure occurs
  in a test case.

#### 2004-08-18 / Release 0.2 (alpha)

- The test suite consists now of approximately 630 assertions.
- Fixed an ugly bug in `lunit.assert()`! Testcases for 
  `lunit.assert()` added.
- Now all assert functions return the actual value on success.


#### 2004-08-15 / Release 0.1 (alpha)

- First public release!



## Contact

Send email to: mail@mroth.net

