sequenceDiagram

Actor User

User--xBrowser: Clicks the submit button
Browser-->Server: Sends user input (submits element button) in the form of JSON

note right of User: Adds input to the note
Browser--x User: Shows the updated list of notes

Browser--> Server: Sends user input in the form of JSON
note over Browser: POST request

Server --> Browser: Sends response to the browser after saving data
note over Server: responds with: 201 status code

Browser--x User: The data in form of notes will be stored