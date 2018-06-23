# Exercises for TDD with PHPUnit (and TYPO3 CMS)

## TDD with Composer (without TYPO3)

### Hello world!

1. Git-clone the [TDD seed project](https://github.com/oliverklee/tdd-seed).
1. Run composer install.
1. Configure PHPUnit in PhpStorm and run the existing tests.
1. Run the tests on the command line.
1. Create a local branch `hello-world`.
1. Create `Test/Unit/MathTest.php` and write a test that tests that 1 + 1 = 2
   (which always is good to know). Run the tests.
1. Commit your changes.

### Test patterns

1. Create a local branch `feature/sizes` from `feature/coffee`.
1. Create a `SizeOption`-Model. Test that it can be instantiated.
1. Working in a test-driven way, add an `int` field `SizeOption.milliliters`
   (with a getter and setter).
   Throw an `UnexpectedValueException` if zero or a negative number is passed
   to the setter.
1. Add a `bool` field SizeOption.includedInPrice`.
1. Add an 1:n association `CoffeeBeverave.sizeOptions`, including all necessary
   methods.
1. Add a methods `CoffeeBeverage.getPriceTag` that returns a string containing
   all available size options and the information whether the size is included
   in the price.
