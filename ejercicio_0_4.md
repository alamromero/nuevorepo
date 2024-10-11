´´´mermaid
sequenceDiagram
participant navegador
participant servidor

navegador->>servidor: POST https://studies.cs.helsinki.fi/exampleapp/notes
activate servidor
servidor-->>navegador: redirecciona hacer solicitud get location "/exampleapp/notes"
deactivate servidor

navegador->>srvidor: GET https://studies.cs.helsinki.fi/exampleapp/notes
activate servidor
servidor-->>navegador: HTML code
deactivate servidor

navegador->>servidor: https://studies.cs.helsinki.fi/exampleapp/main.css
activate servidor
servidor-->>navegador: the css file
deactivate servidor

navegador->>servidor: GET https://studies.cs.helsinki.fi/exampleapp/main.js
activate servidor
servidor-->>navegador: the JavaScript file
deactivate servidor

#ejecuta el javascript para traer el json

navegador->>servidor: GET https://studies.cs.helsinki.fi/exampleapp/data.json
activate servidor
servidor-->>navegador: [{ "content": "hi", "date": "2024-10-10" }, ... ]
deactivate servidor

#El navegador ejecuta la funcion y dibuja las notas# 
´´´
