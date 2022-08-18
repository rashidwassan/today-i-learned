## Node js

### There are some of the points important to mention

- Node js is not a framework it is a `Runtime Environment`
- Node js is highly `scalable`
- Node js is based on `non blocking or asynchronous` architecture
- Node is best of the applications involving a lot of I/O operations.
- Node is not for computationally heavy apps due to being single threaded.
- There is the concept of `global` object:
```javaScript

console.log()
setTimeout()
clearTimeout();

// these methods belong to global object, what actually happens is:
global.console.log();
```

## Modules

- When we define a function with same name and signature in multiple files, they get added in global scope.
- The later definition of a function is considered, overriding the earlier one.
- To avoid this thing:
- There comes the concept of modules.
- Every file in node app is considered module.
- Modules are the building blocks of the node application.
- Modules prevent the overriding of the methods and variables.
- 