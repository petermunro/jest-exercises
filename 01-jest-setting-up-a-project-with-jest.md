# Setting Up a Project with Jest

To get started with Jest, we'll add it to a project.

1. Create a new project directory and change into it:

    ```
    mkdir myproj1
    cd myproj1
    ```

2. Initialize the project with `npm` or `yarn`:

    ```
    npm init
    ```

   or:

    ```
    yarn init
    ```

3. Install Jest:

    ```
    npm install --save-dev jest
    ```

   or:

    ```
    yarn add --dev jest
    ```

4. Create a test file, eg simple.test.js to check that everything works:

    ```
    describe("Basic Test Suite", () => {
      it("should succeed", () => {
        expect(true).toEqual(true);
      });
    });
    ```

   Run your test from the command line:

   ```
   npx jest
   ```

5. Use the `--watchAll` flag to start Jest running in watch mode. Change your test and ensure that it is re-run automatically.

6. Now add a `test` _script_ in your `package.json` so you can run Jest in watch mode from there using one of:

   ```
   npm run test
   ```

   ```
   npm test
   ```

   ```
   yarn test
   ```
