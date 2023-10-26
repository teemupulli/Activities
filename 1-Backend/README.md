# Backend: Week 1

> [Homework](../Homework.md)

### Topics 

- JavaScript Engines
- Node.js Fundamentals
- JavaScript
  - Functions are First-Class Citizens
  - Arrow functions
  - Review: `const`, `var` and `let`

### Tentative Timeline

- Mini lecture (~35min)
- Group / Pair programming (~35min)
- Break (~15min)
- Mini lecture (~35min)
- Group / Pair programming (~35min)

---

### Browser Engines, JavaScript Engines

- [Browser Engines]
  - Rendering web content
  - Interaction with user interface
  - JavaScript engine as part of Browser Engines
  - Examples: [Blink], [Gecko], [WebKit]

- [JavaScript Engines]
  - Executes JavaScript code
  - Parses, compiles, and executes programs
  - Popular JavaScript engines: [V8], [SpiderMonkey]

-  [V8] JavaScript Engine
  - written in C++
  - Portable and runs on Mac, Windows, Linux
  - Modern JavaScript engines no longer just [interpret] JavaScript, they compile it.

### The Birth of [Node.js]

- JavaScript in the Browser
  - JavaScript's role in the browser environment
  - Limitations of client-side JavaScript
- Expanding Horizons with Node.js
  - Node.js as a server-side JavaScript platform
  - Utilizing V8 to run JavaScript on servers
- REPL
- Scripts

### JS: Arrow functions

- [Functions are First-Class Citizens](../Reading/functions.md)
- [Arrow Functions?](../Reading/arrow-functions.md)
- [Function declaration vs function expressions]
- Callbacks



### [Activity 1](./activity-1/README.md)

- JavaScript
  - Arrow Functions
  - Concept of hoisting 
  - `var`, `let`, `const`
- Custom Node.js modules

---

### Node.js Architecture

- Overview of Node.js architecture
- [Event Loop](https://www.tutorialandexample.com/node-js-event-loop)
- [libuv](https://codeahoy.com/learn/libuv/ch1/)
- Single threaded vs multi threaded
- Core Modules (e.g., 'fs', 'os')
- Demo using core modules

### [Node.js]: Key Features and Advantages

- Non-blocking I/O operations
- Single-threaded events loop model
- Three types of modules


### [Activity 2](./activity-2/README.md)

- Node built-in modules e.g. `fs`, `os`
- Blocking vs Non-blocking operations

---

### Study Material
- [JS Engines]
- [Node Intro]
- [Arrow Functions]
- [Functions]


### Other Links used during the lecture
- https://en.wikipedia.org/wiki/Comparison_of_browser_engines
- https://hacks.mozilla.org/2017/05/quantum-up-close-what-is-a-browser-engine/
- https://0xedward.github.io/dom-visualizer/
- https://html5up.net/
- https://codedocs.org/what-is/comparison-of-javascript-engin
- https://en.wikipedia.org/wiki/Node.js
- https://en.wikipedia.org/wiki/V8_(JavaScript_engine)
- https://www.javascripttutorial.net/nodejs-tutorial/what-is-nodejs/
- https://javascript.info/variables
- https://javascript.info/function-expressions
- https://javascript.info/arrow-functions-basics
- https://css-tricks.com/dom/
- https://css-tricks.com/an-introduction-and-guide-to-the-css-object-model-cssom/
- https://github.com/getify/You-Dont-Know-JS
- https://www.makeareadme.com/#template-1
- [Do you know JS](https://github.com/getify/You-Dont-Know-JS)
- [Event Loop](https://www.tutorialandexample.com/node-js-event-loop)
- [libuv](https://codeahoy.com/learn/libuv/ch1/)

<!-- Links -->
[Browser Engines]:https://en.wikipedia.org/wiki/Browser_engine
[Blink]:https://en.wikipedia.org/wiki/Blink_(browser_engine)
[Gecko]:https://en.wikipedia.org/wiki/Gecko_(software)
[WebKit]:https://en.wikipedia.org/wiki/WebKit
[JavaScript Engines]:https://en.wikipedia.org/wiki/JavaScript_engine
[V8]:https://en.wikipedia.org/wiki/V8_(JavaScript_engine)
[SpiderMonkey]:https://en.wikipedia.org/wiki/SpiderMonkey
[interpret]:https://nodejs.dev/en/learn/the-v8-javascript-engine/
[Node.js]:https://nodejs.dev/en/learn/
[JS Engines]:../Reading/JS-engines.md
[Node Intro]:../Reading/node-intro.md
[Variables]:../Reading/variables.md
[Arrow Functions]:../Reading/arrow-functions.md
[Functions]:../Reading/functions.md
[Activity 1-]:https://github.com/tx00-web/labs/tree/main/be-node-basics1
[Activity 2-]:https://github.com/tx00-web/labs/tree/main/be-node-basics2
[Modern JavaScript Tutorial]:https://www.youtube.com/playlist?list=PL4cUxeGkcC9haFPT7J25Q9GRB_ZkFrQAc
[Function declaration vs function expressions]:https://www.freecodecamp.org/news/when-to-use-a-function-declarations-vs-a-function-expression-70f15152a0a0/