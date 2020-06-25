# Using Mock Functions

A function may depend on other functions or modules.
But what if we want to test only the function under test, and not the dependencies?

To do this, we can _mock_ the dependency functions.

That is, we can provide a trivial function that "pretends" to be the dependency function, but which really just returns the same data without doing anything else.

1. Create a calculator file. We should be able to call it
   like this:

    ``` javascript
    import { add, subtract, multiply } from './calculator';

    let result = add(2,3);      // returns 5
    ```

2. Add a function `addAndMultiply()` that takes 3 arguments:

    - a number
    - a nuber to add to it
    - a number to multiply the total by

  This function should call your `add()` and `multiply()`
  functions.

3. Use Jest's mocking functions to mock the underlying
   calculator functions, and verify that `addAndMultiply()`
   works correctly.


