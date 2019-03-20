* Tutorial [Using WebSockets on Heroku with Node.js](https://devcenter.heroku.com/articles/node-websockets)
* Este código se corresponde con la sección: **Option 2: Socket.io** que muestra como usar websockets en Heroku
utilizando el módulo [Socket.io](https://socket.io/)
* Repo [heroku-examples/node-socket.io](https://github.com/heroku-examples/node-socket.io)
* Aquí es esencial habilitar [session affinity](https://devcenter.heroku.com/articles/session-affinity):

  ```
  [~/local/src/javascript/learning/websockets/websockets-heroku-socket-io(master)]$ heroku features:enable http-session-affinity
  Enabling http-session-affinity for ⬢ dsi-socket-io-example... done
  ```

  Session affinity, sometimes referred to as sticky sessions, is a platform feature that associates all HTTP requests coming from an end-user with a single application instance (web dyno).
