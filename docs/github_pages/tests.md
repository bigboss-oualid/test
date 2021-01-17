# Tests

[Back to summary](index.md)

## PHPUnit
>Unit & fucntional tests are located in the folder ``./tests/PHPUnit``.

```shell
# Run all tests of the app
./bin/phpunit

# Run tests for one class (replace CLASS_NAME with the name of class you want test)
./bin/phpunit --filter CLASS_NAME
```

## Behat
>BDD tests are located in the folder ``./features``.

```shell
# Run all tests of the app
./vendor/bin/behat

# Run only one test (replace TAGS_NAME with the name of tag you want test)
./vendor/bin/behat.bat --tags=TAGS_NAME
```

[Next step](analysis.md "Run Tests")
