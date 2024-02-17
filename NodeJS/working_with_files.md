In Node.js, there are built-in modules such as fs, path, util, stream, etc.

## fs module

The **"fs"** module provides a set of functions for interacting with the file system, allowing you to perform various file-related operations such as reading from or writing to files, creating directories, and more.

**fs** contains both sync and async methods.

## Importing fs module and its functions

```jsx
// how to import fs 👇
const fs = require('fs');

or 

import _ from 'fs'
```

## **Reading from a file**

```jsx
const filePath = path.join(__dirname, 'fileName');

const fs = require('fs');
fs.readFile(filePath, 'utf-8', callback(err, data) {
	if(err) {
		console.log(err)
} else {
		console.log(data)
	}
});
```

## Writing to a file

writeFile() does not take ‘utf-8’ thing. instead it takes data which needs to be written.

also the callback doesnt take data.

```jsx
const filePath = path.join(__dirname, 'fileName');
const dataToWrite = "Data to write";

fs.writeFile(filePath, dataToWrite, function(err) {
	try {
		console.log('Success Message!');
	} catch(err) {
		console.log(err);
	}
});
```

## Using path module to get the path of the file which you want to read or write to

The usage of `path.join` in the context of file operations, such as reading a file with is often recommended to ensure that the path to the file is constructed correctly. 

The `path.join`function helps create platform-independent paths by handling 
differences in path separators between operating systems (e.g., '/' on Unix systems and '\' on Windows)

```jsx
import join from 'path';

const filePath = path.join(__dirname, 'file')
```

- `__dirname` is a global variable in Node.js that represents the directory name of the current module (i.e., the directory where the current script resides)

---

There is one more better way to get the path of the file:

## Using dirname and fileURLToPath

```jsx
import { dirname } from 'path'
import { fileURLToPath } from 'url'
const __dirname = dirname + fileURLToPath(import.meta.url);

// now you can use it like this;
__dirname + /parentfolder/subfolder/file.txt;
```