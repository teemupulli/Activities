# synchronous (sync) file read and write

**Step 1**

1. In your project directory, 
- create a JavaScript file (e.g., `synchronous.js`) where you'll perform the tasks in this lab.
- Create a  `sample.txt` file and add some text to it.

2. import the `fs` module:

```javascript
const fs = require('fs');
```

3. Synchronously read the contents of a `sample.txt` using `fs.readFileSync()`. Handle errors, if any, and log the content to the console:

<details>
<summary>How to</summary>

```javascript
try {
  const data = fs.readFileSync('sample.txt', 'utf8');
  console.log('File contents (Synchronous Read):', data);
} catch (err) {
  console.error('Error reading file:', err);
}
```
</details>

4. Synchronously write data to a new file using `fs.writeFileSync()`. Handle errors, if any, and confirm the data has been written:

<details>
<summary>How to</summary>

```javascript
try {
  fs.writeFileSync('output.txt', 'This is some sample data (Synchronous Write).');
  console.log('Data written to output.txt (Synchronous Write)');
} catch (err) {
  console.error('Error writing file:', err);
}
```
</details>

**Step 5: Operating System Information**

1. Import the `os` module and access various pieces of information about the operating system:

```javascript
const os = require('os');
```

2. Print the hostname using `os.hostname()`:

```javascript
console.log('Hostname:', os.hostname());
```

3. Display the OS platform with `os.platform()`:

```javascript
console.log('OS Platform:', os.platform());
```

4. Determine the available CPU cores with `os.cpus()`:

```javascript
console.log('CPU Cores:', os.cpus());
```

**Step 6**

Use `fs.writeFileSync()` to log `os.hostname()` and `os.platform()`.


<details>
<summary>Sample solution</summary>

```js
const fs = require('fs');
const os = require('os');


const info = `Hostname: ${os.hostname()}\nPlatform: ${os.platform()}`;

// Write the information to a file
try {
  fs.writeFileSync('system_info.txt', info);
  console.log('System information has been written to system_info.txt');
} catch (err) {
  console.error('Error writing system information:', err);
}
```

</details>

**Step 7**

Run Your Program and observe the results.