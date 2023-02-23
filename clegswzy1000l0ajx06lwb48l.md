# Flow Of Code Execution In JavaScript And The Execution Context

In javascript, all the code is executed inside a **javascript engine** (for example V8, JavaScriptCore, SpiderMonkey etc.).

## What is JavaScript Engine?

JavaScript engine is a program whose responsibility is to execute JavaScript code. It comes inside browsers(Chrome, Firefox) of servers(node, deno) to execute javascript code.

---

Modern javascript engines are using Just-in-Time compiler

## How does the JavaScript Just-in-Time compiler work?

As a new piece of JavaScript code enters the JavaScript Engine, the first step performed is **parsing** the code. During this process, the code is parsed into a data structure called the **Abstract Syntax Tree** (AST).

The Abstract Syntax Tree first splits each line of code into pieces that are meaningful to JavaScript, such as the `let`, `static`, or `function` keywords. It then saves these pieces of code into a tree-like structure. The next step checks whether there are any syntax errors and, if none are found, the resulting tree is used to generate the machine code.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677119649200/77bccbca-4f53-4c35-b062-2c72a6d3c690.png align="center")

---

As javascript is an interpreted language, it moves to the next line only when the execution of the current line is completed.

execution context

The entire javascript code exaction happens inside a container that is called **execution context**.

There are two kinds of Execution Context in JavaScript:

* Global Execution Context (GEC)
    
* Function Execution Context (FEC)
    

### Global execution context

Whenever the JavaScript engine receives a source file, it first creates a default Execution Context known as the Global Execution Context (GEC). It represents the environment in which the top-level code is executed.

> The GEC is always created, even with an empty file.

### Function execution context

Whenever a function is called, the JavaScript engine creates another type of Execution Context known as a Function Execution Context (FEC) on top of the GEC to evaluate and execute the code within that function.

---

The Execution Context was conducted in two phases:

1. Memory Allocation Phase
    
2. Code Execution Phase
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677124125655/ed6b161f-0587-4c61-80f2-ddaefebd080c.png align="center")

### Memory Allocation Phase

In this phase, javascript allocates the memory to all the variables and functions present in the program. The variables are stored with the value `undefined` and the function is stored with all the code present in that particular function.

### Code Execution Phase

In this phase, the main execution takes place and the javascript runs through the code line by line. Here all the variables get initialized with their values. And when a new function is invoked a new execution context is created inside the GEC.

Let's take an example:

```javascript
let a = 3
let b = 5
function add(a, b) {
  let sum
  sum = a + b
  return sum
}
let sum = add(a, b)
```

At first, as soon as the code is invoked an execution context is created.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677129325198/3e20247e-856b-41cc-a1c7-26d40dc53b34.png align="center")

Variables and functions are mounted into Memory Allocation.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677129709500/bdd5a9ef-0ba9-408c-9baa-18425fabd02e.png align="center")

At this time a **Call stack** is also maintained by javascript, to maintain the `Order of execution` of execution contexts.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677130393434/26dea36c-15b9-4490-89b3-79aa0f973890.png align="center")

Now Javascript executes code line-by-line and assigns the values.

It assigns values to variables `a` and `b`. At the time of function it skips that and executes the next line.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677130786328/23d5d7dd-ac58-4034-8868-c1a058846670.png align="center")

Now when the `sum` variable is called the `add()` function is invoked.

Because `add()` function is invoked a new execution context is created.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677131775699/e0c783cf-3779-4b80-b21f-c830d4f6f862.png align="center")

After the creation of another execution context, the **Call stack** is updated.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677134147930/c96be4a0-93ae-49a6-b1b1-37a3278ec1b6.png align="center")

Now in the function execution context variables `a` and `b` gets its value from the calling location.

At the assigned time of the `sum` variable, the operation `a + b` is executed in the **code execution** part and returns the result to the `sum` variable.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677134831503/ad50e734-cecb-4612-a438-c2b27aa1cbc7.png align="center")

After this function execution context returns the value to its calling variable.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677135667444/c346370f-299e-4c05-9bdb-a418db1d1e7d.png align="center")

And after FCE execution the whole execution context is deleted from GEC and **Call stack** is updated again.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677136140331/e5f46544-62cc-434f-a74f-80093c9267ee.png align="center")

At last after all code execution, the global execution context also disappeared.