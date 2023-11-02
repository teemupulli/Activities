# 2023-11-02: Front End

> In the afternoon, we will be using Postman. If you haven't installed it yet, you can download it from [here](https://www.postman.com/downloads/).

### Topics

- HTTP, Status codes
- TCP Ports
- JavaScript e.g. JSON, Callback, Template Literals
- API server &  Middleware

### Tentative Timeline per session

- Mini lecture (~35min)
- Group / Pair programming `+ Break` (~50min)
- Mini lecture (~35min)
- Group / Pair programming (~35min)

----

### Demo 1

- `npm init -y` ,  `npm i express`, `node server.js`
- visit `http://localhost:3001/`
- Scripts:  `npm start`, `npm run dev`
- Stop server: `ctr + c` ([Mac users] `command-c`)

### Express: Introduction

- [TCP ports] 
- [HTTP methods] - `app.get()`
- Endpoint vs routes
- Request vs Response: `req`, `res`
- Status codes
- JSON: `res.json()`
  - [JSON]
  - [JSON.parse()]
  - [JSON.stringify()] 
  - `Demo2`
- `app.listen()`
- [Template Literals] 
  - String interpolation 
  - Multi-line strings
- Naming `app.js` vs `server.js` vs `index.js`


### Activity 1

- Simple API with Express
- [Activity](./activity1/README.md)

---

### Middlewares

- Middleware as a pipeline
- [Middlewares]
  - Custom middleware
    - Logging middleware
    - 404: not found middleware
    - Order: Beginning, middle, end
    - Example: append requestTime
  - Built-in 
    -  `app.use(express.static('public'));`
    -  `app.use(express.json());` (**In the afternoon**)
  - Error middleware (**Later**)

### Misc.
- CRUD operation (Afternoon)
- Naming `app.js` vs `server.js` vs `index.js`
- [`nodemon`]
  - why `nodemon`? 
  - `npm install nodemon --save-dev`
  - Script: `"dev": "nodemon app.js"`
  - Run script: `npm run dev` **NOT** `npm dev`
  - `npx` vs `npm`

### Activity 2

- Custom middleware
  - Logging middleware
  - 404: not found middleware
- [Activity](./activity2/README.md)



### Summary

- [Summary](./Summary.md)
- [(Optional activity): JavaScript](./activity3/README.md)
- Reading
  - [TCP and UDP Ports Explained](https://www.bleepingcomputer.com/tutorials/tcp-and-udp-ports-explained/) 
  - [Express: hello world]
  - [Middlewares]
  - [Express middleware: A complete guide]
- Review: Functions are [first class citizens]
  -  Ability to treat functions as values
  -  Ability to pass a function as arguments
  -  Ability to return a function from another 


<!-- Links -->

[Mac users]:https://support.apple.com/guide/terminal/keyboard-shortcuts-trmlshtcts/mac
[Callback Functions: (first 18 min only)]:https://youtu.be/QSqc6MMS6Fk
[How The Web Works: (12 min)]:https://youtu.be/hJHvdBlSxug
[HTTP Methods: (3 min)]:https://youtu.be/tkfVQK6UxDI
[JSON vs JavaScript Object Literals: (5 min)]:https://youtu.be/912_cPllMyg
[JavaScript Template Literals: (5 min)]:https://youtu.be/NgF9-pdTDGs
[Express JS Crash Course: (first 16 min only)]:https://youtu.be/L72fhGm1tfE
[JSON]:https://www.json.org/json-en.html
[Express]:http://expressjs.com/
[JSON]:https://www.w3schools.com/js/js_json_intro.asp
[JSON.parse()]:https://www.w3schools.com/js/js_json_parse.asp
[JSON.stringify()]:https://www.w3schools.com/js/js_json_stringify.as
[Template Literals]:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals 
[TCP ports]:https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers
[HTTP methods]:https://en.wikipedia.org/wiki/HTTP#Request_methods
[`nodemon`]:https://www.npmjs.com/package/nodemon
[first class citizens]:https://www.geeksforgeeks.org/what-is-first-class-citizen-in-javascript/ 
[Middlewares]:https://expressjs.com/en/guide/writing-middleware.html
[Express: hello world]:https://expressjs.com/en/starter/hello-world.html
[Express middleware: A complete guide]:https://blog.logrocket.com/express-middleware-a-complete-guide/
[ChatGPT Cheat Sheet for Developers]:https://hackr.io/blog/chatgpt-cheat-sheet-for-developer
[4 ways devs can use ChatGPT to be more productive]:https://www.educative.io/blog/chatgpt-how-it-can-help-devs-productivity
