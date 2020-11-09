# Test naming exercises

Find good names for the described behavior. Please note:

- Please start with the scenarios you find the most tricky to name.
- Some scenarios require more than one test to cover the behavior,
  particularly if there are edge cases.
  It is your task to identify those and come of with the test names.
- Some scenarios build on assumptions concerning how the system behaves
  outside of the described behaviour, or on certain method names.
  In those cases, please come up with the missing parts as necessary.

## Scenarios

1. `Article::getCroppedTitle`: A title shorter than 80 characters does not get
   cropped, and a title with a length of at least 80 characters gets cropped.
1. `Article::isNew` initially returns `true`. After a call
   to `markAsFinished`, it returns `false` (and will continue to do so).
1. `Article::getSorting` returns zero if no other value has been set, and the value set via `setSorting` otherwise.
1. `Article::setSorting` with a negative value throws an `UnexpectedValueException`.
1. `ArticleController::indexAction` hides the "Next" link
   if the current page is the last page.
1. `ArticleController::indexAction` passes the models from `findAll` to the view.
1. `ArticleRepository::findExpired` finds only articles that have a past
   expiry date.
1. `ArticleRepository::findAllPublishedIn` returns articles published at
   the start, in between and at the end of the given time span,
   but not before or after.
1. `Command\Import::import` command calls the `run` function of the
   `UserImporter`.
1. `FileReader::readFile` will throw a `RuntimeException` if the file does
    not exist. If called with an empty file, it will return an empty array.
    If there are several lines in the file, it will return the file's lines
    as an array of strings.
1. `LogCollector::getDigest` returns all logged messages in one concatenated
   string. An arbitrary number of log messages can be added:
   none, one, two, three, …
1. `NotificationService`: When an e-mail gets sent, the `lastEmailSent` date
   field in the article gets updated.
1. `NotificationService`: The e-mail contains the article title.
1. `NotificationService`: For articles that are not published yet,
   no e-mail gets sent.
1. `ShoppingCart::calculatePrice` returns the total of all items' prices.
   There may also be no items.
1. `User`: The method `locateUser` retrieves the geo coordinates
   and saves the user.
1. `User::getCountry` returns the associated country (if there is any).
1. `User::hasCity` returns `false` if the model has no associated city,
    and `true` if it has one.
1. `User::hasGeoLocationError` returns `true` after `setGeoLocationError`
    has been called.
1. `User::clearLocationGeoError` leads to `hasGeoLocationError` returning `false`
    even if it has returned `true` before that.
1. `User::isPasswordCorrect` checks whether the given password is correct.
1. `User::setRadius` sets the radius (in kilometers) for positive integers
    and for zero.
    If the value is negative, an `UnexpectedValueException` gets thrown.
