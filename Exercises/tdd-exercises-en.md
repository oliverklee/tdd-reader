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

For these exercises, it is a requirement that you always use a test list and
that you work strictly test-first.

1. Create a local branch `feature/sizes` from `origin/feature/coffee`.
1. Create a new `SizeOption` model/entity. Test that it can be instantiated.
1. Working in a test-driven way, add an `int` field `SizeOption.milliliters`
   (with a getter and setter).
   Throw an `UnexpectedValueException` if zero or a negative number is passed
   to the setter.
1. Add a `bool` field `SizeOption.includedInPrice`.
1. Add an 1:n association `CoffeeBeverage.sizeOptions`, including all necessary
   methods.
1. Add a method `CoffeeBeverage.getPriceTag` that returns a string containing
   all available size options with the information whether the size is included
   in the price.

### Regression tests (complex)

The `RunLengthEncoder` seems to have several bugs. Fix them using regression
tests with a test-driven approach.

Please create a new local branch off the `main` branch for this.

1. There are some special cases that currently are not covered with tests and
  that may or may note have bugs. To make sure those cases work fine, please
  test those cases (and fix any bugs you may encounter):
  - null bytes: `chr(0)`
  - umlauts and special characters: `äöüß,.-#'+*`
1. The marker character/byte `@` can also occur in the payload.
1. Sequences might be longer than 255 characters, e.g, 256 or 257 characters.
1. If a sequence in the compressed data has a length of 0, this should not
  create unwanted behavior. For better compression, let's use a length of 0
  to encode a length of 256 bytes.  
1. The compressed data might end after the marker character/byte, or one
  character later. In those cases, the decompressor needs to throw an
  `UnexpectedValueException`.

### Virtual file systems

Build a `SinglePhpStartTagSniffer` that extends `AbstractSniffer`.
The `sniff` method will scan the given path and
recursively return all `*.php` files in the given directory that include
at least two long PHP start tags.
(The sniffer does not need to check for start tags within strings.)

Only use virtual files for this (no real files allowed).

### Mocking

1. Without mocking, create a `Rocket` that will return `"Swoosh!"`
   if `launch()` is called.
1. Build a `RocketLauncher` that can collect `Rocket`s.
   `activate()` will `launch()` all `Rockets`.
   (You do not want to actually call `launch` on the rockets here
   for obvious reasons. To achieve this, use `Prophecy`).
1. Using [Swift Mailer](https://swiftmailer.symfony.com/docs/introduction.html),
   build a `QuickMailer` that sends an email with the following method:
   `send(\Swift_Message $email, string $fromEmail, string $toEmail, string $subject, string $body): void`.
   Use a partial mock for `$email` to avoid that the real `send()` method
   is run.

### Coverage and mutation testing

1. Run your tests with coverage in PhpStorm.
1. Run Infection (`vendor/bin/infection`), find out what your tests are
   missing, and add the missing tests.
