``` mermaid
sequenceDiagram
    participant browser
    participant server

    note left of browser:new note is enter and submit button is pressed
    note left of browser:now the onsubmit event is trigger and onsubmit event handlers is excuted
    note left of browser: new note value is pushed to the existing note list and screen is redrawn

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    note right of server:new note from the request json is deserialized and and the data is stored
    server-->>browser: JSON  {"message":"note created"}

```
