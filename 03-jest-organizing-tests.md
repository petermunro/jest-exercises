# Organizing Tests

1. Earlier you placed your tests in a test file.
   Now organize them into `describe()` blocks (which
   can be nested if necessary).

2. Run your tests.


## Write a Data-Driven Test

Sometimes you'll need to execute the same test, but with
different data each time.

Rather than defining lots of tests with different data,
you can do so once, but pass different data sets into a single test.

1. Create a test file to test an `add()` function.

2. Insert an `add()` function, for example:

    ```
    const add = (a, b) => a + b;
    ```

3. Write a data-driven test using [`test.each()`](https://jestjs.io/docs/en/api#testeachtablename-fn-timeout).
   Your test should:

    1. Specify the data, that is, the two numbers to add,
       and the expected result.
    2. Define a single test that works on this data.

## Skipping Tests

1. Experiment with skipping both `test`s and `describe` blocks.

## Setting Up and Resetting State

1. Experiment with:

    - `beforeAll` and `afterAll`
    - `beforeEach` and `afterEach`

  Verify that these enable you to 