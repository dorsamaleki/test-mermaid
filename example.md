```mermaid
sequenceDiagram

    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new-note-spa

    Note right of browser: The POST request to the address new_note_spa contains the new note as JSON data containing both the content of the note (content) and the timestamp (date):{content: "single page app does not reload the whole page", date: "2019-05-25T15:15:59.905Z"} The Content-Type header of the request tells the server that the included data is represented in JSON format.


    activate server
    server-->>browser: status code 201 created
    deactivate server




