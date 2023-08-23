sequenceDiagram

Actor User

User->>Browser: Goes to the page

Browser->>Server: Fetch sp.html
Note over Browser: GET request

Server->>Browser: Provides sp.html

Browser->Server: Fetch main.css
note over Browser: GET request
Server->>Browser: Provides main.css (style sheet)

Browser->>Server: Fetch sp.js
note over Browser: GET request
Server->>Browser: Provides sp.js

Browser--x User: Loads CSS and HTML
Browser-->Server: data.json

Note left of Server: AJAX request
Server->>Browser: Provides data.json
Browser-->User: Renders the notes as a HTML list
