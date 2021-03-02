# How to run these tests

## Running test with the public NPM repo

The public package for our plugin is at:
https://www.npmjs.com/package/@aichemy/testgold-cypress-plugin

1. Run `npm install -D` to install Cypress as a devDependency and the
   `@aichemy/testgold-cypress-plugin` package as a dependency.

2. See the `cypress.json` file for options to tweak for the Interceptor. Also,
   look at the `cypress/support/index.js` and `cypress/plugins/index.js` file to
   see how the Cypress plugin is activated.

3. Acquire an Interceptor AIO token from the WAL server and export it as an
   environment variable and enable the interceptor:

   ```
   export CYPRESS_TG_ENABLED=true ( use SET YPRESS_TG_ENABLED=true for windows)
   
   export CYPRESS_TG_TOKEN=aiotoken-goes-here ( use SET CYPRESS_TG_TOKEN=aiotoken-goes-here for windows)
   ```

4. Run `./node_modules/.bin/cypress open` to start the Cypress runner.
 "node_modules/.bin/cypress" in windows

5. Run the `reactbank-old.spec.js` and `reactbank-new.spec.js` in order to see
   the healing in action. Other tests are in: https://github.com/sshivaji/testgold_sanity_tests/tree/master/cypress-tests/cypress/integration.


## Running tests with the private Github NPM repo

1. Read
   https://docs.github.com/en/packages/guides/configuring-npm-for-use-with-github-packages

2. You will need a Github personal access token and access to the
   https://github.com/aichemydev/cypress repository. The personal access token
   should have at least "read:packages" permissions for it to access the NPM repo.

3. Create a `.npmrc` file in your home directory and put the Github personal
   access token in it:

   ```
   //npm.pkg.github.com/:_authToken=your-token-goes-here
   ```

4. Uncomment the `.npmrc` file in this folder to make sure the Github package
   registry is used.

5. Change all instances of `@aichemy/testgold-cypress-plugin` to
   `@aichemydev/testgold-cypress-plugin` in the following files: `package.json`,
   `cypress/support/index.js`, and `cypress/plugins/index.js`.

6. Run `npm install -D` to install Cypress as a devDependency and the
   `@aichemydev/testgold-cypress-plugin` package as a dependency.

7. See the `cypress.json` file for options to tweak for the Interceptor. Also,
   look at the `cypress/support/index.js` and `cypress/plugins/index.js` file to
   see how the Cypress plugin is activated.

8. Acquire an Interceptor AIO token from the WAL server and export it as an
   environment variable and enable the interceptor:

   ```
   export CYPRESS_TG_ENABLED=true
   export CYPRESS_TG_TOKEN=aiotoken-goes-here
   ```

9. Run `./node_modules/.bin/cypress open` to start the Cypress runner.

10. Run the `reactbank-old.spec.js` and `reactbank-new.spec.js` in order to see
   the healing in action. Other tests are in: https://github.com/sshivaji/testgold_sanity_tests/tree/master/cypress-tests/cypress/integration.
