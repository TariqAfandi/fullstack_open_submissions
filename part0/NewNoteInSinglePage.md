```mermaid
sequenceDiagram
  participant browser
  participant server

  browser->>server: sends user input with HTTP POST request
  server-->>browser: responds with HTTP status code 201 (Created)

  Note left of server: The server does not ask for a redirect
  Note right of browser: The browser stays on the same page, sends no further HTTP requests
