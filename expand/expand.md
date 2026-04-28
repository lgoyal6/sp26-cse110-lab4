# Expand - Reflection Questions

1. **What are some pain points of JavaScript as a language?**

JavaScript's asynchronous nature is a pain point because the execution order of code is not always top-to-bottom. Callbacks, promises, and async/await can be confusing to reason about, especially when multiple async operations depend on each other. Developers coming from synchronous languages find it hard to predict when code will actually run, leading to race conditions and bugs that are hard to trace.

Loose typing is a pain point because variables can silently change type, and operations between mismatched types produce unexpected results instead of errors. A bug caused by adding a string and a number returning a concatenated string instead of a sum can be nearly invisible and hard to debug. Strict typing in languages like TypeScript or Java catches these errors at compile time.

The web platform itself is a pain point because JavaScript must run in every browser, and browsers do not always implement features consistently. Developers have to write code defensively to support multiple environments, and the DOM API is widely considered clunky and verbose compared to modern alternatives.

2. **Why do you think JavaScript was made loosely typed and with async features?**

JavaScript was made loosely typed likely because it was designed to be approachable for non-programmers and quick to write. Brendan Eich created it in 10 days to be a lightweight scripting language for the web, not an enterprise language. Strict typing would have created a steeper learning curve for the web designers and hobbyists it was targeting. Async features were added because the web is inherently asynchronous — a browser needs to respond to user events, load resources from servers, and render UI all at the same time. Blocking the main thread while waiting for a network response would make every website freeze, so async behavior was a practical necessity from the start.

3. **What is the difference between a compiled and interpreted language? What are the benefits/drawbacks of JavaScript being interpreted?**

A compiled language is translated to machine code before execution. The compiler reads the entire source, checks for errors, and produces an optimized binary that the machine runs directly. Examples are C and Java. An interpreted language is executed line by line at runtime by an interpreter without a separate compilation step. JavaScript is interpreted (though modern engines like V8 use JIT compilation to improve performance). The benefits of JavaScript being interpreted are that there is no build step, code can be run immediately, and it is easier to prototype quickly. The drawbacks are that errors are only caught at runtime rather than ahead of time, and raw performance is generally lower than fully compiled languages for CPU-intensive tasks.

4. **Why do you think the professor is focusing on vanilla JavaScript? What are the benefits and drawbacks of not learning a framework?**

The professor is likely focusing on vanilla JavaScript because frameworks abstract away what is actually happening under the hood. If you learn React before you understand the DOM, you do not truly understand what React is doing for you — you just memorize its API. Understanding vanilla JS gives you the foundation to learn any framework faster, debug framework issues more effectively, and make better architectural decisions. The benefits of mastering vanilla JS first are a deeper understanding of the language, better debugging skills, and not being locked into one framework's way of thinking. The drawbacks of not learning a framework are that in a real job, almost every team uses one, and not knowing React or Vue can be a hiring disadvantage. Also, frameworks solve real problems around state management and component reuse that become very painful to handle manually at scale.

5. **How does this lab relate to your project?**

This lab directly relates to the project because we will be building a web application using JavaScript. Understanding variable scoping means we will not accidentally introduce bugs from leaking variables across functions. The pipeline section mirrors exactly what our team should set up — automated tests that run on every push so broken code does not quietly make it into the main branch. The DevTools section is immediately practical since we will spend time debugging our own project's JavaScript in the browser. The diagramming section is relevant because we need to plan our app's user flows before building them, and having a shared diagram keeps the whole team aligned. Every section of this lab is a skill we will use directly on the project.
