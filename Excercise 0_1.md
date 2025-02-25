# Part 0 | excercises 0.3 to 0.6
>The first excersise to showcase in this repository starts in 0.4

## 0.4
- Illustration of the sequence for adding a new note after submitting it through the form.


```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server
    server-->>browser: URL redirection
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>browser: new request for the HTML file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: new request for the CSS file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate server
    server-->>browser: new request for the JavaScript file
    deactivate server

    Note right of browser: The browser starts executing the JavaScript code that fetches the JSON from the server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: retrieves the JSON  
    deactivate server

    Note right of browser: The browser executes the callback function that renders the notes
```

## 0.5
- Illustration of the sequence to access an SPA
```mermaid
sequenceDiagram
    participant browser
    participant server
```
