# SkillNG Backend Curriculum — Improved Assessment
## Sessions 1–24

> **Format Guide**
> Each session contains four question types based on the recommended assessment framework:
> - **Objective (40%)** — Multiple choice: terminology, command recognition, conceptual knowledge
> - **Code Interpretation (20%)** — Read code and answer: what does it do? What is the output?
> - **Debugging (20%)** — Identify and fix errors in a provided code block
> - **Code Completion / Modification (20%)** — Add a missing line or modify code to produce a different output

---

## Module 1: Programming Fundamentals

---

### Session 1: Introduction to Backend Engineering

**Objective**

1. Which of the following best describes the Request-Response Lifecycle?
   - A) The process of writing code in an IDE
   - B) The communication cycle where a client sends a request and the server returns a response
   - C) The way a database stores information
   - D) The installation of a server-side language

2. What is a primary responsibility of a backend developer?
   - A) Designing the visual layout of a website
   - B) Managing server-side logic, databases, and APIs
   - C) Writing CSS animations for UI elements
   - D) Ensuring the website is mobile-responsive

**Code Interpretation**

3. Look at the following simplified client-server exchange:

```
Client → GET /profile → Server
Server → 200 OK { "name": "Ada", "role": "admin" } → Client
```

   a. What HTTP status code does the server return, and what does it mean?
   b. If the resource `/profile` did not exist, what status code would you expect instead?

**Debugging**

4. A junior developer describes their backend setup:
   > "The client sends a POST request to `/login`. The server receives it, checks the database, but never sends anything back — the browser just hangs forever."

   What is the most likely mistake? Describe what the server must do to complete the lifecycle correctly.

**Code Completion / Modification**

5. Fill in the blank to complete the description of a standard HTTP response:

```
An HTTP response consists of:
1. A __________ line (e.g., HTTP/1.1 200 OK)
2. Headers (e.g., Content-Type: application/json)
3. An optional __________
```

---

### Session 2: Programming Basics — Variables and Data Types

**Objective**

6. Which of the following is considered a primitive data type in most backend languages?
   - A) List
   - B) Dictionary
   - C) Integer
   - D) Object

7. What is type conversion?
   - A) Changing a value from one data type to another (e.g., string to integer)
   - B) Deleting a variable from memory
   - C) Naming a variable according to syntax rules
   - D) Encrypting data for security

**Code Interpretation**

8. What is the output of this JavaScript code?

```
const age = "25";
const height = 5.9;
const isActive = true;

console.log(typeof age);
console.log(Number(age) + 5);
console.log(typeof height);
```

**Debugging**

9. The following code logs `NaN` instead of the correct total. Identify the bug and fix it.

```
const price = "49.99";
const tax = 0.075;
const total = price * (1 + tax);
console.log("Total:", total);
```

**Code Completion / Modification**

10. Complete the code so that `userId` is stored as a number and `isVerified` is stored as a boolean:

```
const rawId = "1042";
const rawVerified = "true";

const userId = __________(rawId);
const isVerified = rawVerified.toLowerCase() === __________;
console.log(userId, isVerified);
```

---

### Session 3: Control Flow — Logic and Conditionals

**Objective**

11. Which operator is used to check if two values are equal in most programming languages?
    - A) `=`
    - B) `==`
    - C) `!=`
    - D) `<>`

12. In boolean logic, the AND operator returns `true` only if:
    - A) At least one condition is true
    - B) All conditions are true
    - C) All conditions are false
    - D) The first condition is true

**Code Interpretation**

13. What does this JavaScript function return when called as `checkAccess(17, false)`?

```
function checkAccess(age, isMember) {
    if (age >= 18 && isMember) {
        return "Full access";
    } else if (age >= 18) {
        return "Limited access";
    } else {
        return "Access denied";
    }
}
```

**Debugging**

14. This code is supposed to log `"Discount applied"` only when the price is above 100 and the user is a member. Find and fix the bug:

```
const price = 120;
const isMember = true;

if (price > 100 || isMember) {
    console.log("Discount applied");
} else {
    console.log("No discount");
}
```

**Code Completion / Modification**

15. Fill in the blanks so the function returns `"Valid"` only when the score is between 0 and 100 inclusive:

```
function validateScore(score) {
    if (__________ && __________) {
        return "Valid";
    }
    return "Invalid";
}
```

---

### Session 4: Loops and Iteration

**Objective**

16. Which loop construct is best used when you know the exact number of iterations?
    - A) For loop
    - B) While loop
    - C) If-Else statement
    - D) Switch statement

17. What does a `break` statement do inside a loop?
    - A) Skips the current iteration and moves to the next
    - B) Exits the loop entirely
    - C) Restarts the loop from the beginning
    - D) Pauses the program for a set time

**Code Interpretation**

18. What is the output of this code?

```
let total = 0;
for (let i = 1; i <= 5; i++) {
    if (i % 2 === 0) {
        continue;
    }
    total += i;
}
console.log(total);
```

**Debugging**

19. This code is supposed to log numbers 1 through 5. Find and fix the bug:

```
let i = 1;
while (i < 5) {
    console.log(i);
    i++;
}
```

**Code Completion / Modification**

20. Modify this loop so it stops (using `break`) as soon as it finds the first negative number, then logs that number:

```
const numbers = [4, 7, 2, -3, 8, -1];

for (const num of numbers) {
    if (__________) {
        __________;
        __________;
    }
}
```

---

### Session 5: Functions and Modularity

**Objective**

21. What are "parameters" in the context of a function?
    - A) The final output of the function
    - B) Variables used to pass data into the function
    - C) The name of the function
    - D) Comments written inside the function

22. What is "scope" in programming?
    - A) The speed at which a function runs
    - B) The physical size of the code file
    - C) The region of a program where a variable is accessible
    - D) The process of finding bugs

**Code Interpretation**

23. What is the output of the following code?

```
function greet(name, greeting = "Hello") {
    return `${greeting}, ${name}!`;
}

console.log(greet("Alex"));
console.log(greet("Sam", "Hi"));
```

   a. What would happen if you called `greet()` with no arguments at all?

**Debugging**

24. This function is supposed to return the square of a number but always returns `undefined`. Fix it:

```
function square(n) {
    const result = n * n;
}

console.log(square(4));
```

**Code Completion / Modification**

25. Rewrite the following code as a reusable function called `calculateDiscount` that takes `price` and `discountRate` as parameters and returns the discounted price:

```
const price = 200;
const discountRate = 0.1;
const discounted = price - (price * discountRate);
console.log(discounted);
```

---

### Session 6: Core Data Structures

**Objective**

26. Which data structure stores data in key-value pairs?
    - A) List
    - B) Set
    - C) Map / Dictionary
    - D) Array

27. A Set is a data structure characterized by:
    - A) Storing elements in a fixed order
    - B) Allowing duplicate values
    - C) Storing only unique elements
    - D) Having no maximum size

**Code Interpretation**

28. What is the output of this code?

```
const inventory = { apples: 10, bananas: 5, oranges: 8 };
inventory.bananas += 3;
inventory.grapes = 6;

for (const [item, qty] of Object.entries(inventory)) {
    if (qty > 7) {
        console.log(item);
    }
}
```

**Debugging**

29. This code is supposed to remove duplicates from an array and log the result. Find and fix the bug:

```
const numbers = [1, 2, 2, 3, 4, 4, 5];
const unique = [...numbers];
console.log(unique);
```

**Code Completion / Modification**

30. Complete the code to build an object that maps each name to its string length:

```
const names = ["Alice", "Bob", "Charlie"];
const nameLengths = {};

for (const name of names) {
    nameLengths[__________] = __________;
}

console.log(nameLengths);
```

---

### Session 7: Files, Error Handling, and Debugging Fundamentals

**Objective**

31. What is exception handling?
    - A) Writing code that never has bugs
    - B) Managing and responding to runtime errors to prevent crashes
    - C) Deleting files after they are read
    - D) Converting a program into machine code

32. Which of these is a defensive programming practice?
    - A) Writing as much code as possible in one file
    - B) Validating user input before processing it
    - C) Ignoring errors to keep the program running
    - D) Hard-coding passwords into the source code

**Code Interpretation**

33. What will this code log if the file `data.txt` does not exist?

```
const fs = require("fs");

try {
    const content = fs.readFileSync("data.txt", "utf8");
    console.log(content);
} catch (err) {
    if (err.code === "ENOENT") {
        console.log("File not found. Please check the path.");
    }
} finally {
    console.log("Done.");
}
```

**Debugging**

34. This code crashes when the user provides a non-numeric value. Rewrite it with proper error handling so it logs `"Invalid input"` instead of crashing:

```
const userInput = "abc";
const result = 100 / Number(userInput);
console.log("Result:", result);
```

**Code Completion / Modification**

35. Complete the code so it writes an array of log entries to a file called `log.txt`, one entry per line:

```
const fs = require("fs");

const logs = ["Started server", "Connected to DB", "Request received"];
const content = logs.__________("\n");

fs.__________(  "log.txt", content, "utf8");
```

---

### Session 8: Project 1 — Command-Line Application

**Objective**

36. What does "persistence" refer to in a CLI application?
    - A) The speed of command execution
    - B) The colors used in the terminal
    - C) Saving data so it remains available after the program closes
    - D) The user's ability to type commands

37. Which of the following is a key component of a terminal-based tool?
    - A) Graphic User Interface (GUI)
    - B) CSS Styling
    - C) Command-Line Interface (CLI)
    - D) Web Browser

**Code Interpretation**

38. What does this CLI snippet do, and what happens when the user types `quit`?

```
const fs = require("fs");
const readline = require("readline");

const DATA_FILE = "tasks.json";

function loadTasks() {
    if (fs.existsSync(DATA_FILE)) {
        return JSON.parse(fs.readFileSync(DATA_FILE, "utf8"));
    }
    return [];
}

const tasks = loadTasks();
const rl = readline.createInterface({ input: process.stdin, output: process.stdout });

function prompt() {
    rl.question("Enter command (add/list/quit): ", (cmd) => {
        if (cmd === "quit") {
            rl.close();
        } else if (cmd === "list") {
            tasks.forEach(t => console.log("-", t));
            prompt();
        } else {
            prompt();
        }
    });
}

prompt();
```

**Debugging**

39. This save function is supposed to persist tasks to `tasks.json` but never actually writes anything. Find and fix the bug:

```
const fs = require("fs");

function saveTasks(tasks) {
    fs.readFileSync("tasks.json", JSON.stringify(tasks), "utf8");
}
```

**Code Completion / Modification**

40. Complete the `addTask` function so it appends a new task to the array and saves it to disk:

```
const fs = require("fs");

function saveTasks(tasks) {
    fs.writeFileSync("tasks.json", JSON.stringify(tasks), "utf8");
}

function addTask(tasks, taskName) {
    tasks.__________(taskName);
    __________;
}

const tasks = [];
addTask(tasks, "Buy groceries");
addTask(tasks, "Write report");
```

---

## Module 2: Backend Runtime & Networking Fundamentals

---

### Session 9: Server-Side Programming Concepts

**Objective**

41. What is a "language runtime"?
    - A) The time it takes to write a script
    - B) The environment in which a program executes
    - C) A specific type of database
    - D) A text editor for backend code

42. What does "concurrency" allow a backend system to do?
    - A) Handle multiple tasks at the same time
    - B) Run on only one CPU core
    - C) Delete unused variables automatically
    - D) Turn off the server during low traffic

**Code Interpretation**

43. What does this Node.js code demonstrate about execution order?

```
console.log("Start");

setTimeout(() => {
    console.log("Timeout fired");
}, 0);

console.log("End");
```

   a. What is the output, and in what order?
   b. Why does `"Timeout fired"` print last even though the delay is `0`?

**Debugging**

44. A developer reports: *"My server handles requests fine normally, but when a file upload takes 10 seconds to process, no other users can get a response during that time."*

   Identify the architectural problem and explain what change would fix it.

**Code Completion / Modification**

45. Fill in the blank to make this Node.js server respond to every request with `"Hello, World!"`:

```
const http = require("http");

const server = http.createServer((req, res) => {
    res.writeHead(200, { "Content-Type": "text/plain" });
    res.__________("Hello, World!");
    res.end();
});

server.listen(3000);
```

---

### Session 10: API Testing & Inspection Workflows

**Objective**

46. Which tool is commonly used for request inspection and testing APIs?
    - A) VS Code
    - B) Postman
    - C) Photoshop
    - D) Slack

47. In API testing, "response validation" involves checking:
    - A) If the computer is plugged in
    - B) If the status code, headers, and body are correct
    - C) The font size of the documentation
    - D) The speed of the internet connection

**Code Interpretation**

48. A tester makes the following request and receives the response below:

```
POST /api/login
Content-Type: application/json
Body: { "email": "user@example.com", "password": "wrong123" }

Response:
HTTP/1.1 401 Unauthorized
{ "error": "Invalid credentials" }
```

   a. What does the `401` status code mean?
   b. What should the tester try next to verify the happy path (successful login)?

**Debugging**

49. A developer tests an endpoint and always gets a `400 Bad Request` error. Looking at the request below, identify the problem:

```
POST /api/users
Content-Type: text/plain
Body: { "name": "Ada", "email": "ada@example.com" }
```

**Code Completion / Modification**

50. Complete this Postman-style test script so it checks that the response status is `200` and the body contains a `token` field:

```
pm.test("Status is 200", function () {
    pm.response.to.have.status(__________);
});

pm.test("Response has token", function () {
    const body = pm.response.__________();
    pm.expect(body).to.have.property(__________);
});
```

---

### Session 11: Asynchronous and Concurrent Programming

**Objective**

51. What is the main characteristic of "non-blocking" execution?
    - A) The program stops until a task finishes
    - B) The program continues to other tasks while waiting for a process to complete
    - C) It only works for mathematical calculations
    - D) It requires a physical server restart

52. What is a Promise (or Future) in programming?
    - A) A guarantee that the code has no bugs
    - B) An object representing the eventual completion or failure of an async operation
    - C) A variable that cannot be changed
    - D) A function that returns only strings

**Code Interpretation**

53. What is the output of the following code, and in what order?

```
async function fetchData() {
    console.log("Fetching...");
    const result = await new Promise((resolve) => {
        setTimeout(() => resolve("Data ready"), 1000);
    });
    console.log(result);
}

console.log("Before fetch");
fetchData();
console.log("After fetch");
```

**Debugging**

54. The following async function is supposed to return user data but always returns `undefined`. Find and fix the bug:

```
async function getUser(id) {
    fetch(`/api/users/${id}`)
        .then(res => res.json())
        .then(data => {
            return data;
        });
}
```

**Code Completion / Modification**

55. Rewrite the following callback-based code using `async/await`:

```
function loadUser(id, callback) {
    setTimeout(() => {
        callback({ id: id, name: "Ada" });
    }, 500);
}

// Rewrite using async/await below:
async function getUser(id) {
    // your code here
}
```

---

### Session 12: Core System Libraries and Environment Management

**Objective**

56. Why are environment variables used?
    - A) To store the user's profile picture
    - B) To store sensitive configuration like API keys outside of the source code
    - C) To speed up the computer's CPU
    - D) To define the colors of the website

57. A "configuration pattern" helps a developer:
    - A) Write better HTML
    - B) Manage settings across different environments (Dev, Production)
    - C) Choose a background color for the IDE
    - D) Design a database schema

**Code Interpretation**

58. What does this Node.js code do, and what would happen if `PORT` is not defined in the environment?

```
require("dotenv").config();
const PORT = process.env.PORT || 3000;
console.log(`Server running on port ${PORT}`);
```

**Debugging**

59. A developer hardcoded their database credentials directly in the source code (shown below). Explain why this is a problem and rewrite it using environment variables:

```
const db = connectDB({
    host: "db.internal.company.com",
    user: "admin",
    password: "SuperSecret123",
    database: "production_db"
});
```

**Code Completion / Modification**

60. Complete the `.env` file and the code snippet so the app reads `DB_HOST` and `DB_PORT` from the environment:

```
# .env file
DB_HOST=__________
DB_PORT=__________
```

```
require("dotenv").config();
const host = process.env.__________;
const port = process.env.__________;
console.log(`Connecting to ${host}:${port}`);
```

---

### Session 13: Package Management, Dependency Isolation, and Version Control

**Objective**

61. Semantic Versioning (SemVer) typically uses which format?
    - A) Name.Date.Time
    - B) Major.Minor.Patch (e.g., 1.2.3)
    - C) Red.Blue.Green
    - D) Alpha.Beta.Gamma

62. In Git workflows, what does a "commit" do?
    - A) Deletes all files in the directory
    - B) Downloads code from a remote server
    - C) Records changes made to the files in the repository history
    - D) Opens a new terminal window

**Code Interpretation**

63. A `package.json` contains this dependency entry:

```json
"dependencies": {
    "express": "^4.18.2"
}
```

   a. What does the `^` (caret) symbol mean?
   b. Would version `5.0.0` be automatically installed? Why or why not?

**Debugging**

64. A developer's git log looks like this:

```
commit a3f1c9d — "fixed bug"
commit b82e01a — "fixed bug"
commit cc71234 — "stuff"
commit d9900ef — "wip"
```

   Describe two problems with this commit history and explain what good commit messages should look like.

**Code Completion / Modification**

65. Fill in the correct Git commands to complete this workflow:

```bash
# 1. Create and switch to a new branch called "feature/login"
git __________ feature/login

# 2. Stage all changed files
git __________ .

# 3. Commit with a descriptive message
git commit -m "__________"

# 4. Push the branch to the remote origin
git push __________ feature/login
```

---

### Session 14: HTTP Fundamentals and Web Servers

**Objective**

66. Which HTTP method is used to create a new resource?
    - A) GET
    - B) POST
    - C) DELETE
    - D) OPTIONS

67. What does an HTTP 404 status code mean?
    - A) Success
    - B) Internal Server Error
    - C) Not Found
    - D) Unauthorized

**Code Interpretation**

68. Examine this HTTP request and response pair:

```
Request:
PUT /api/users/42
Content-Type: application/json
Body: { "name": "Ibrahim", "email": "ibrahim@example.com" }

Response:
HTTP/1.1 200 OK
{ "id": 42, "name": "Ibrahim", "email": "ibrahim@example.com" }
```

   a. What operation is being performed?
   b. What would be the appropriate status code if the user with ID 42 did not exist?

**Debugging**

69. This Express endpoint crashes sometimes. Explain why and fix it:

```
app.get('/users', (req, res) => {
    const users = getUsers();
    res.send(users);
});
```

**Code Completion / Modification**

70. Complete the Express route so that it returns a `404` status with an error message when no product is found:

```
app.get("/products/:id", (req, res) => {
    const product = findProduct(req.params.id);
    if (!product) {
        return res.status(__________).json({ error: __________ });
    }
    res.json(product);
});
```

---

### Session 15: Debugging, Logging, and Observability

**Objective**

71. What is "structured logging"?
    - A) Writing logs in a random diary
    - B) Formatting logs (often in JSON) so they are easily searchable by machines
    - C) Printing only error messages to the console
    - D) Disabling logs in production

72. A debugger allows you to:
    - A) Automatically fix all your code
    - B) Compile your code
    - C) Pause execution and inspect the state of the program
    - D) Format your code

**Code Interpretation**

73. Compare these two log styles:

```
# Log A
"Error occurred"

# Log B
{ "level": "error", "timestamp": "2026-03-29T10:45:00Z", "route": "/api/login", "message": "Invalid credentials", "userId": null }
```

   a. Which log is structured, and why is it more useful in production?
   b. What information does Log B provide that Log A does not?

**Debugging**

74. A developer placed a `console.log` in the wrong location and cannot figure out why a variable is undefined. Identify the issue:

```
function processOrder(order) {
    console.log("Processing:", item);
    const item = order.item;
    const total = item.price * order.quantity;
    return total;
}
```

**Code Completion / Modification**

75. Add structured JSON logging to this function so that both successful responses and errors are logged with a timestamp, level, and message:

```
function handleRequest(req, res) {
    try {
        const data = processData(req.body);
        // Log success here
        res.json(data);
    } catch (err) {
        // Log error here
        res.status(500).json({ error: "Internal server error" });
    }
}
```

---

### Session 16: Project 2 — Basic Web Server

**Objective**

76. What is "routing" in a web server?
    - A) The process of connecting to a Wi-Fi router
    - B) Mapping incoming request URLs to specific handler functions
    - C) Encrypting the server's hard drive
    - D) Sending an email to the administrator

77. Why is structured error handling important in a web server?
    - A) It provides consistent error messages to the client
    - B) It prevents the user from seeing any errors
    - C) It makes the code run faster
    - D) It is required by the internet service provider

**Code Interpretation**

78. What does this Express server do? List every route it handles and what each returns:

```
const express = require("express");
const app = express();
app.use(express.json());

app.get("/", (req, res) => res.send("Welcome"));
app.get("/health", (req, res) => res.json({ status: "ok" }));
app.post("/echo", (req, res) => res.json(req.body));
app.use((req, res) => res.status(404).json({ error: "Not found" }));

app.listen(3000);
```

**Debugging**

79. This server always returns `"Not found"` even for the `/health` route. Find and fix the bug:

```
app.use((req, res) => res.status(404).json({ error: "Not found" }));
app.get("/health", (req, res) => res.json({ status: "ok" }));
```

**Code Completion / Modification**

80. Complete this Express server so it accepts a `POST /greet` request with a JSON body `{ "name": "Ada" }` and responds with `{ "message": "Hello, Ada!" }`:

```
const express = require("express");
const app = express();
app.use(express.json());

app.post("/greet", (req, res) => {
    const name = __________;
    res.json({ message: __________ });
});

app.listen(3000);
```

---

## Module 3: RESTful APIs & Application Layer Design

---

### Session 17: Introduction to Web Frameworks

**Objective**

81. What is "middleware" in a web framework?
    - A) The database used by the application
    - B) Functions that execute during the request-response cycle before the final handler
    - C) The CSS used for the frontend
    - D) The hardware the server runs on

82. Framework architecture provides:
    - A) A structured skeleton and tools to build applications efficiently
    - B) A replacement for a programming language
    - C) A way to bypass security protocols
    - D) An automated way to write marketing copy

**Code Interpretation**

83. What does this middleware chain do? Describe what happens at each step when a request arrives:

```
app.use((req, res, next) => {
    console.log(`[${new Date().toISOString()}] ${req.method} ${req.url}`);
    next();
});

app.use((req, res, next) => {
    if (!req.headers["x-api-key"]) {
        return res.status(401).json({ error: "Missing API key" });
    }
    next();
});

app.get("/data", (req, res) => {
    res.json({ value: 42 });
});
```

**Debugging**

84. A developer's middleware never passes control to the route handler. Find and fix the issue:

```
app.use((req, res) => {
    console.log("Request received:", req.method);
});

app.get("/users", (req, res) => {
    res.json([{ id: 1, name: "Ada" }]);
});
```

**Code Completion / Modification**

85. Add a middleware function that logs the response time for every request. Fill in the blanks:

```
app.use((req, res, __________) => {
    const start = Date.now();
    res.on("finish", () => {
        const duration = __________ - start;
        console.log(`${req.method} ${req.url} — ${duration}ms`);
    });
    __________();
});
```

---

### Session 18: Routing and Resource Modeling

**Objective**

86. Which REST principle suggests that every resource should have a unique identifier?
    - A) Uniform Interface (Resource Identification)
    - B) Statelessness
    - C) Cacheability
    - D) Layered System

87. Which URI follows REST best practices for "getting all books"?
    - A) `/get-all-books`
    - B) `/admin/query?type=books`
    - C) `/books`
    - D) `/books/all/data`

**Code Interpretation**

88. Review this route definition:

```
app.get("/users/:userId/posts/:postId", (req, res) => {
    const { userId, postId } = req.params;
    res.json({ userId, postId });
});
```

   a. What URL pattern would match this route?
   b. What would the response be for a request to `/users/5/posts/12`?

**Debugging**

89. A developer designed the following routes for a blog API. Identify which routes violate REST conventions and suggest corrections:

```
POST   /createUser
GET    /getPostById?id=5
DELETE /posts/remove/3
PUT    /posts/update
```

**Code Completion / Modification**

90. Complete the route definitions to create a RESTful set of endpoints for a `products` resource:

```
app.get("__________", getAllProducts);           // Get all products
app.get("__________", getProductById);          // Get a single product
app.post("__________", createProduct);          // Create a product
app.put("__________", updateProduct);           // Update a product
app.delete("__________", deleteProduct);        // Delete a product
```

---

### Session 19: Middleware and Request Processing Pipelines

**Objective**

91. A "cross-cutting concern" handled by middleware might include:
    - A) Defining a variable
    - B) Authentication and logging
    - C) Writing a SQL query
    - D) Installing a new OS

92. What is a "validation layer" used for?
    - A) Checking if the incoming request data meets specific requirements
    - B) Checking if the server has enough RAM
    - C) Formatting the HTML output
    - D) Speeding up database queries

**Code Interpretation**

93. Trace the execution of this pipeline for a request that has a valid token but sends an empty body:

```
app.use(logRequest);        // Logs method and URL
app.use(authenticate);      // Checks Authorization header
app.use(validateBody);      // Ensures body is not empty
app.post("/submit", handleSubmit);
```

   a. Which middleware functions will execute?
   b. At which point will the pipeline stop, and what response will the client receive?

**Debugging**

94. This authentication middleware is supposed to block requests with invalid tokens, but it lets everything through. Find and fix the bug:

```
function authenticate(req, res, next) {
    const token = req.headers.authorization;
    if (token !== "secret-token") {
        console.log("Invalid token");
    }
    next();
}
```

**Code Completion / Modification**

95. Complete this middleware so it adds a `requestId` to every incoming request (using `Math.random()`) and passes it on:

```
function attachRequestId(req, res, next) {
    req.requestId = __________;
    __________();
}

app.use(__________);
```

---

### Session 20: Input Validation and Data Integrity

**Objective**

96. What is "sanitization" in the context of user input?
    - A) Deleting the user's account
    - B) Cleaning input to remove potentially harmful characters (e.g., script tags)
    - C) Checking if the user's email is valid
    - D) Saving the input to a database

97. "Boundary enforcement" ensures that:
    - A) Data stays within defined limits (e.g., character length, value ranges)
    - B) The server does not communicate with other countries
    - C) The API is only accessible from a specific IP
    - D) The code is written inside a specific folder

**Code Interpretation**

98. What will this validation function return for each of these inputs?

```
function validateUser(data) {
    if (!data.name || data.name.length < 2) return { valid: false, error: "Name too short" };
    if (!data.email || !data.email.includes("@")) return { valid: false, error: "Invalid email" };
    if (!data.age || data.age < 18) return { valid: false, error: "Must be 18+" };
    return { valid: true };
}
```

   - Input A: `{ name: "A", email: "ada@test.com", age: 25 }`
   - Input B: `{ name: "Ada", email: "adatest.com", age: 25 }`
   - Input C: `{ name: "Ada", email: "ada@test.com", age: 16 }`

**Debugging**

99. This validation allows a dangerous input through. Identify the vulnerability and fix it:

```
function createUser(req, res) {
    const username = req.body.username;
    const query = `INSERT INTO users (username) VALUES ('${username}')`;
    db.run(query);
    res.json({ success: true });
}
```

**Code Completion / Modification**

100. Add validation to this route handler so it rejects requests where `price` is not a number or is less than zero:

```
app.post("/products", (req, res) => {
    const { name, price } = req.body;

    if (__________ || __________) {
        return res.status(400).json({ error: "Invalid price" });
    }

    createProduct({ name, price });
    res.status(201).json({ message: "Product created" });
});
```

---

### Session 21: Centralized Error Handling and Response Standards

**Objective**

101. What is the benefit of centralized error handling?
     - A) It makes the program stop immediately
     - B) It ensures all errors are caught and returned in a consistent format
     - C) It hides all bugs from the developer
     - D) It automatically fixes the code

102. "Error propagation" refers to:
     - A) Passing an error up the call stack until it is handled
     - B) Spreading a virus through a network
     - C) Copying and pasting an error into a chat
     - D) Deleting the error log

**Code Interpretation**

103. What happens when this route throws an error, and how does Express route it to the error handler?

```
app.get("/fail", (req, res, next) => {
    try {
        throw new Error("Something broke");
    } catch (err) {
        next(err);
    }
});

app.use((err, req, res, next) => {
    console.error(err.message);
    res.status(500).json({ error: err.message });
});
```

**Debugging**

104. This error handler is never invoked when errors occur in routes. Identify the problem:

```
app.use((err, res) => {
    res.status(500).json({ error: err.message });
});
```

**Code Completion / Modification**

105. Complete the centralized error handler so it returns a `404` for `NotFoundError` instances and `500` for everything else:

```
class NotFoundError extends Error {}

app.use((err, req, res, next) => {
    if (err instanceof __________) {
        return res.status(__________).json({ error: err.message });
    }
    res.status(__________).json({ error: "Internal server error" });
});
```

---

### Session 22: API Design & Documentation Best Practices

**Objective**

106. What is "pagination" used for in an API?
     - A) Securing the API with a password
     - B) Breaking down large datasets into smaller chunks (pages)
     - C) Translating the API into different languages
     - D) Changing the API version

107. Which tool/standard is widely used for API documentation?
     - A) Microsoft Word
     - B) JPEG
     - C) OpenAPI (Swagger)
     - D) PNG

**Code Interpretation**

108. Review this API endpoint:

```
GET /api/v1/articles?page=2&limit=10&sort=created_at&order=desc
```

   a. What does each query parameter do?
   b. How many total articles would be skipped to get to page 2?

**Debugging**

109. A developer designed this versioned API route. Identify the problem and suggest a fix:

```
app.get("/api/articles", getArticlesV1);
app.get("/api/articles", getArticlesV2);  // Updated version
```

**Code Completion / Modification**

110. Complete this OpenAPI-style summary comment for the `POST /users` endpoint:

```
# Complete this OpenAPI description:
/users:
  post:
    summary: __________
    requestBody:
      required: true
      content:
        application/json:
          schema:
            type: object
            properties:
              name:
                type: __________
              email:
                type: __________
    responses:
      '201':
        description: __________
      '400':
        description: __________
```

---

### Session 23: API Testing and Automation

**Objective**

111. What is "unit testing"?
     - A) Testing the entire application at once
     - B) Testing the smallest individual parts (units) of the code in isolation
     - C) Testing the API over the internet
     - D) Testing the hardware of the server

112. "Integration testing" focuses on:
     - A) Testing a single function
     - B) Testing how different components or services work together
     - C) Checking the spelling in the documentation
     - D) Calculating the cost of hosting

**Code Interpretation**

113. Read this unit test and answer the questions below:

```
test("calculate discount returns correct value", () => {
    const result = calculateDiscount(200, 0.1);
    expect(result).toBe(180);
});

test("calculate discount throws when rate is invalid", () => {
    expect(() => calculateDiscount(200, 1.5)).toThrow("Invalid discount rate");
});
```

   a. What two behaviours is this test suite verifying?
   b. What should the `calculateDiscount` function do when the rate is greater than 1?

**Debugging**

114. This test always passes even when the function is broken. Explain why and fix it:

```
test("getUser returns a user object", async () => {
    getUser(1).then(user => {
        expect(user).toHaveProperty("name");
    });
});
```

**Code Completion / Modification**

115. Complete this integration test for a `POST /users` endpoint using a testing library like `supertest`:

```
const request = require("supertest");
const app = require("./app");

test("POST /users creates a new user", async () => {
    const response = await request(app)
        .__________("/users")
        .__________({ name: "Ada", email: "ada@example.com" });

    expect(response.status).toBe(__________);
    expect(response.body).toHaveProperty(__________);
});
```

---

### Session 24: Project 3 — CRUD API

**Objective**

116. What does the acronym "CRUD" stand for?
     - A) Copy, Read, Unite, Delete
     - B) Create, Read, Update, Delete
     - C) Create, Run, Undo, Debug
     - D) Compile, Read, Use, Deploy

117. In a CRUD API, which HTTP method is typically used for the "Update" operation?
     - A) GET
     - B) POST
     - C) PUT or PATCH
     - D) DELETE

**Code Interpretation**

118. Review this CRUD route and identify what operation it performs, what it expects in the request, and what it returns:

```
app.patch("/tasks/:id", authenticate, validateBody, async (req, res, next) => {
    try {
        const task = await Task.findByIdAndUpdate(
            req.params.id,
            { $set: req.body },
            { new: true }
        );
        if (!task) return res.status(404).json({ error: "Task not found" });
        res.json(task);
    } catch (err) {
        next(err);
    }
});
```

   a. What is the difference between `PUT` and `PATCH`? Why is `PATCH` used here?
   b. What does the `{ new: true }` option do?

**Debugging**

119. This DELETE endpoint always returns `200 OK` even when the item doesn't exist. Fix it:

```
app.delete("/items/:id", async (req, res) => {
    await Item.deleteOne({ _id: req.params.id });
    res.status(200).json({ message: "Deleted" });
});
```

**Code Completion / Modification**

120. Complete this full CRUD route set for a `notes` resource. Fill in the HTTP methods and status codes:

```
// Get all notes
app.________("/notes", async (req, res) => {
    const notes = await Note.find();
    res.status(__________).json(notes);
});

// Create a note
app.________("/notes", async (req, res) => {
    const note = await Note.create(req.body);
    res.status(__________).json(note);
});

// Update a note
app.________("/notes/:id", async (req, res) => {
    const note = await Note.findByIdAndUpdate(req.params.id, req.body, { new: true });
    res.status(__________).json(note);
});

// Delete a note
app.________("/notes/:id", async (req, res) => {
    await Note.findByIdAndDelete(req.params.id);
    res.status(__________).send();
});
```

---
