# Activity 2

In this lab, you will explore the Node.js `fs` (File System) and `os` (Operating System) modules to better understand how system calls and file operations work. Additionally, we will discuss the security implications of these operations, emphasizing the importance of proper error handling and security practices.

### Objectives

1. Understand the `fs` and `os` modules in Node.js.
2. Execute system calls and file operations using Node.js.
3. Recognize security implications related to file and system access.


### Part 1: File System Operations

1. In your project directory, create a JavaScript file (e.g., `sys-calls.js`) where you'll perform the tasks in this lab.

2. Import the `fs` module and perform the following file system operations:
- Create a  `sample.txt` file and add some text to it.
- Read the contents of  `sample.txt` file using `fs.readFile()`. Handle errors appropriately and log the content to the console.

    <details>
    <summary>How to</summary>

    ```javascript
    const fs = require('fs');
    fs.readFile('sample.txt', 'utf8', (err, data) => {
        if (err) {
        console.error('Error reading file:', err);
        } else {
        console.log('File contents:', data);
        }
    });
    ```

    </details>

- Write data to a new file (e.g., `output.txt`) using `fs.writeFile()`. Handle errors and confirm the data has been written.

    <details>
    <summary>How to</summary>

    ```javascript
    fs.writeFile('output.txt', 'This is some sample data.', (err) => {
    if (err) {
    console.error('Error writing file:', err);
    } else {
    console.log('Data written to output.txt');
    }
    });
    ```

- Run your program and observe the results. Discuss the potential security risks involved when reading or writing files and the importance of error handling in these operations.

### Part 3: Operating System Information

1. Import the `os` module and access various pieces of information about the operating system.

    <details>
    <summary>How to</summary>

    ```javascript
    const os = require('os');
    ```
    </details>

   a. Print the hostname using `os.hostname()` e.g `console.log('Hostname:', os.hostname());`
   b. Display the OS platform with `os.platform()`.
   c. Determine the available CPU cores with `os.cpus()`.

2. Run your program and discuss the types of information that can be accessed through the `os` module. Consider the potential security implications of disclosing such information.


### Part 4

Use `fs.writeFile()` to log `os.hostname()`, `os.platform()` and  `os.cpus()`

### Part 5: asynchronous operations

In your script, you invoked `fs.readFile()` and `fs.writeFile()`  prior to logging the OS information like `os.platform()`. Explain why the observed output may look as follows:

```sh
Hostname: DESKTOP-DAB97SL
OS Platform: win32
Data written to output.txt
File contents: This is some text
```

<details>
<summary>Explanation</summary>

- **fs.readFile()** and **fs.writeFile()** are asynchronous functions: These file system operations are designed to work asynchronously, which means they don't block the execution of the rest of your code. They initiate file read and write operations in the background and continue with the execution of the subsequent code without waiting for them to complete.

- **Logging with os.platform()**: When you call `os.platform()` to log the information about the operating system, it typically executes immediately since it's a synchronous operation. It provides the OS information in your output.

- **Execution Flow**: Here's the order of execution with the described sequence:

   - The script starts.
   - `fs.readFile()` and `fs.writeFile()` are called. They initiate their respective file operations but don't block the script's execution.
   - Immediately after, `os.platform()` is called, logging the OS information.

- **Potential Output Issues**: The output could have a couple of issues due to the asynchronous nature of file operations:

   - The OS information might be logged before the `fs.readFile()` and `fs.writeFile()` operations complete. This is because these file operations are running concurrently in the background, and there's no guarantee that they will finish before `os.platform()` executes.

   - If your script relies on the data read from a file by `fs.readFile()` or the data being written by `fs.writeFile()`, it may not be available or complete at the point when `os.platform()` executes.

</details>



### Extra

One way to solve part 4 is to use promises. This topic will be dealt with later in the course.

<details>
<summary>Sample solution</summary>

 ```js
const fs = require('fs').promises;
const os = require('os');

async function readFileAndLogOSInfo() {
  try {
    const data = await fs.readFile('output.txt', 'utf8');
    console.log('Data from file:', data);

    const platform = os.platform();
    console.log('OS Platform:', platform);
  } catch (error) {
    console.error('Error:', error);
  }
}

readFileAndLogOSInfo();
```

</details>