This is my github repository for the course https://fullstackopen.com.

sequenceDiagram
    activate client
    client->>server: GET request to https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    deactivate client
    server->>client: server responds to the request by sending "notes" HTML file
    deactivate server

    activate client
    client->>server: GET request to https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    deactivate client
    server->>client: server responds to the request by sending the css file
    deactivate server

    activate client
    client->>server: GET request to https://studies.cs.helsinki.fi/exampleapp/main.js
    activate server
    deactivate client
    server->>client: server responds to the request by sending javascript file
    deactivate server

    Note left of server: Client browser executes retrieved javascript and fetches the json data from the server
    activate client
    client->>server: GET request to https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    deactivate client
    server->>client: server responds with the json data
    deactivate server
    Note left of server: Client executes the callback function to display the data from json response
