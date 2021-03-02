1)Start by going to https://nocode.testgold.dev/login website. Create a login either using your github id or google or using your email and password.
2)Login and go to https://nocode.testgold.dev/settings . ( Activation might take a few hours after login)
3)The token visible in this page is referred to as the CYPRESS_TG_TOKEN .
4)On your command line Run npm install -D to install Cypress  and the @aichemy/testgold-cypress-plugin package.
5)Run the below commands to set the respective tokens to activate Test Gold .
    export CYPRESS_TG_ENABLED=true ( use SET CYPRESS_TG_ENABLED=true for windows)
    export CYPRESS_TG_TOKEN=aiotoken-goes-here ( use SET CYPRESS_TG_TOKEN=aiotoken-goes-here for windows)
6)Run ./node_modules/.bin/cypress open to start the Cypress runner. 
 The command is "node_modules/.bin/cypress" in windows
7) This will open the Cypress UI and show all the tests available in the folder.
8) Run the reactbank-old.spec.js first to train Test Gold and wait for it to complete.
9) Run the reactbank-new.spec.js in order to see the healing in action. 
10) Other tests are in: https://github.com/aichemydev/cypress-examples/tree/main/cypress-tests/cypress/integration
