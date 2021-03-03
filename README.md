Start by going to https://nocode.testgold.dev/login website. Create a login either using your github id or google or using your email and password.   

Login and go to https://nocode.testgold.dev/settings . ( Activation might take a few hours after login)   

The token visible in this page is referred to as the CYPRESS_TG_TOKEN .   

On your command line Run npm install -D to install Cypress  and the @aichemy/testgold-cypress-plugin package.   

Run the below commands to set the respective tokens to activate Test Gold.

    export CYPRESS_TG_ENABLED=true ( use SET CYPRESS_TG_ENABLED=true for windows)  
    export CYPRESS_TG_TOKEN=aiotoken-goes-here ( use SET CYPRESS_TG_TOKEN=aiotoken-goes-here for windows)  
    
Run

    ./node_modules/.bin/cypress open to start the Cypress runner.   
    The command is "node_modules/.bin/cypress" in windows  
 
 This will open the Cypress UI and show all the tests available in the folder.  
 
Run the reactbank-old.spec.js first to train Test Gold and wait for it to complete.

Run the reactbank-new.spec.js in order to see the healing in action.   
Other tests are in: https://github.com/aichemydev/cypress-examples/tree/main/cypress-tests/cypress/integration

Note that the same test reactbank-new-spec.js will fail if CYPRESS_TG_ENABLED=false or a token variable is not specified.
