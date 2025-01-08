```mermaid
sequenceDiagram
  participant browser
  participant server

  browser->>server: sends user input with HTTP POST request
  server-->>browser: responds with HTTP status code 302 (Found)

  Note right of browser: browser automatically follows the redirect
  
  browser->>server: GET /notes (Reload request 1)
  server-->>browser: HTML document
  
  browser->>server: GET /main.css (Reload request 2)
  server-->>browser: CSS file
  
  browser->>server: GET /main.js (Reload request 3)
  server-->>browser: Javascript file

  Note right of browser: The browser executes the JavaScript to render the updated content
