```mermaid
sequenceDiagram
    participant Browser 
    participant Server

    Browser->>Server: Request GET url=https://https://studies.cs.helsinki.fi/exampleapp/spa
    activate Server
    Server -->> Browser: response text/html(spa.html)
    deactivate Server

    Browser->>Server: Request GET url=https://studies.cs.helsinki.fi/exampleapp/main.css
    activate Server
    Server -->> Browser: response text/css(main.css)
    deactivate Server
    
    Browser->>Server: Request GET url=https://studies.cs.helsinki.fi/exampleapp/main.css
    activate Server
    Server -->> Browser: response application/javascript(spa.js)
    deactivate Server
    
    Note right of Browser: The browser starts executing javascript code

    Browser->>Server: Request GET url=https://studies.cs.helsinki.fi/exampleapp/data.json
    activate Server
    Server -->> Browser: response application/json(data.json)
    deactivate Server

```