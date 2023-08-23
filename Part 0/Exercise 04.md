 sequenceDiagram

    actor User
    participant Browser
    participant Server

    User->>Browser: Clicks Submit Button
    Browser->>Server: Sends User's input

    Note over Browser: POST request to New_Note
    Note over Server: Adds the input from the user to the note
    Note over Server:  HTTP status code 302

    Server->>Browser: Requests new HTTP GET request to the address
    
    Note over Browser: Reloads

    Browser->>Server: Fetch Main.css (style sheet)
    Note over Browser: GET requests

    Browser->>Server: Fetch main.js (JavaScript code)
    Note over Browser: GET requests

    Browser->>Server: Fetch data.json (raw data of the notes)
    Note over Browser: GET requests

    User--x Browser: if User refreshes, the previous notes will not appear as they are not stored