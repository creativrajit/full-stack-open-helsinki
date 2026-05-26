```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: When you click save, the JavaScript code (`spa.js`) prevents the default form submission, adds the new note directly to the local array in the browser memory, and rerenders the notes list.

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: application/json
    deactivate server


    Note right of browser: The browser runs the event handler function that renders the notes

```