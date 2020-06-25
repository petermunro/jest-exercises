# Using Matchers

## Testing for Equality

One of the most common tests is to test that two values are equal.
But what do we mean by "equal"? For primitive values, that's easy -
we just compare the values.
But what about objects? Do we test that their fields are the same,
or whether two object references both point to the same object?

Over the following exercises you will explore these matchers:

- `.toBe()`
- `.toBeCloseTo()`
- `.toEqual()`
- `.toStrictEqual()`

### Getting Started

1. Create a new test file, for example `equality.test.js`.

2. We'll use the function below for the following exercises. Copy and paste it into your codebase. (You can either paste it directly into the test file, or use JavaScript export/import statements to access it.)

    ``` javascript
    function getProfile() {
      return {
        username: "jo_user",
        token: "fa79b0f10e67d5534b3c42aaa1ad8259",
        membership_level: "basic",
        learningLevel: 4,
        identityConfirmed: true,
        horizontalAcceleration: 0.1 + 0.2,
      };
    }
    ```


### Testing Primitive Values

1. Create a test to verify that the `learningLevel` is `4`.

2. Create a test to verify that the `membership_level` is as expected.

### Testing Floating Point Numbers

1. Create a test to verify that the `horizontalAcceleration` is as expected. Because floating point values are imprecise, you will need to use `.toBeCloseTo()`.

### Testing Objects

1. Create a test to verify the entire object returned by `getProfile()`. For this, `.toEqual()` should be enough.

2. How does `.toEqual()` differ from `.toBe()`?

3. When would you use `.toStrictEqual()`?


