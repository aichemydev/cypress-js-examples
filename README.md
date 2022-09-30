# How to run these examples

Make sure you have [NodeJS](https://nodejs.org) installed, along with `npm`.

1. Sign up for an account at [app.wring.dev](https://app.wring.dev). You'll need
   to wait until we can verify your sign-up and activate your account; it
   usually takes less than a couple of hours.
2. Once your account is activated, login and click on **Installation** in the
   sidebar to see instructions to download the Cypress plugin as well as the
   token required to let the plugin talk to our API.
3. Set the required environment variable `CYPRESS_TG_TOKEN='your-token-here'` by
   copy-pasting the command shown on the **Installation** page.
4. Set the required environment variable `CYPRESS_TG_ENABLED='true'` to enable
   the plugin.

Now, you can run:

```
npm install
```

to install Cypress and our plugin.

Once that's done, run:

```
./node_modules/.bin/cypress open
```

to open Cypress. You may run any of the tests already present in the
`cypress/integration` directory. We recommend running these two tests in order:

1. Run `reactbank-old-spec.js` to see the Wring API train itself on a working
   example of a website.
2. Run `reactbank-new-spec.js` to see the Wring API automatically heal selectors
   that are now broken because the website page elements moved or were updated.

Try running `reactbank-new-spec.js` with the environment variable
`CYPRESS_TG_ENABLED='false'` to see the test run failing without healed
selectors.

Additional documentation on the Wring Cypress plugin can be found at its
[NPMJS.com page](https://www.npmjs.com/package/@aichemy/wring-cypress-plugin).
The plugin can be configured using a `wring` settings object in the
`cypress.json` file. This repository has an
[example](https://github.com/aichemydev/cypress-js-examples/blob/main/cypress.json)
that you can customize.
