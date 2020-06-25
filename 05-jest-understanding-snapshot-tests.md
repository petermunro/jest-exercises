# Understanding Snapshot Tests

1. Create a test file, for example `snapshot.test.js`.

2. In the file, create a test function (`test("snapshot render", () => { ... })`).

3. In the test function, create a variable to hold a JavaScript object. For example:

   ```
   let myObj = {
     foo: "bar",
     isTuesday: true,
     days: 7,
   };
   ```

4. Assert that the JavaScript object you created matches the snapshot. To do this, pass your JavaScript object to `expect()` and call the `.toMatchSnapshot()` method.

5. The first time this is run, Jest will create the snapshot file. Examime it (it should be in a folder, eg `__snapshots__`).

6. Run the test again. ensuring that it passes.

## An "Accidental" Regression

1. Modify your JavaScript object (eg change the `7` to an `8`). We'll pretend that this value has changed accidentally.

2. Check that the test fails and note how Jest highlights the changed value.

3. Change the value back and ensure that the test passes.

## A Deliberate UI Change

Sometimes we want to make a deliberate code change that results in a change to our JS object or UI.

1. Modify your JavaScript object (eg change the `"bar"` to a `"Login:"`). We'll assume this should result in a wanted change to the object or UI.

2. Check that the test fails. However, we want it to pass!

3. To make it pass, we need to re-generate the snapshot files. To do this:

   - if Jest is in _watch mode_, press `u`
   - if running Jest manually each time,
     run `jest --updateSnapshot`:

     ```
     jest --updateSnapshot
     ```
