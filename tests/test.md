Feature: First Test
    Scenario: First Test
        Given I open Everfit application
        And I click email, clear text, and type the value
        | email |
        | namtran+task@everfit.io    |
        And I click password, clear text, and type the value
        | password |
        | Pass1234!|
        Then I should see the Today screen
        And I should see the Tasks section in the Today screen
        When I click on the task nameed "Test 2" of the "Tasks" section
        Then I should see the Tasks screen
        And I click on "Take photo" button
        And I take a photo by click on the "Take photo" button at bottom of the screen
        And I click the "Check" button
        When I select random Weight by click on the "Weight" field
        And I double tap to the value "1"
        And I click "Done" button
        And I select random value from 1 to 99 Body fat by click on the "Body fat" field 
        And I type a random value
        When I click "Add photo" button
        And I disconect with the simulator
        When I use #browser_install to start the browser and continue the test
        And I navigate to the URL app.everfit.io
        And I login with namtran@everfit.io and Pass1234!
        And I click to Client tab
        And I click to the client "Add Task"
        And I Click to the Overview tab
        And I click to Progress photo
        Then verify the photo is uploaded with the Weight and Body fat I inputted