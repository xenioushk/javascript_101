# JavaScript 101

A dialy used javascript code repository

## Define functions (3 styles)

### Style 1

```javascript
// regular style.
function helloWorld() {
  console.log('hello world')
}

// call the function
helloWorld()
```

### Style 2

```javascript
// assigned to a constant
const helloWorld = function () {
  console.log('hello world')
}

// call the function
helloWorld()
```

### Style 3

This type of function declaration often use in react application.

```javascript
// arrow function.

const helloworld3 = () => {
  console.log('hello world')
}

// call the function
helloWorld()
```

## Array map

**Example 1**

```javascript
const myArray = ['JS', 'CSS', 'HTML5', 'PHP', 'JAVA']

myArray.map((value, index) => {
  console.log(value)
  console.log(index)
})
```

**Example 2**

```javascript
const myNumbers = [1, 2, 3, 4, 5, 6]

const newMyArray = myNumbers.map((val) => {
  return val * 4
})
```

**Output:** [4,8,12,16,20,24]

## Template literals

**Example: 1**

If `isBlobUrl(url)` returns `true` then output class name will be `my-class-img is-loading`. Else, it outputs `my-class-img`

```javascript
<div className={`my-class-img ${ isBlobUrl(url) ? "is-loading" : "" }`} >
```

## Conditional

**Example: 1**

If `isBlobUrl(url)` returns `true` then the `<Spinner />` component will be excuted.

```javascript
{
  isBlob(url) && <Spinner />
}
```

**Example: 2**

If the URL is true, then application will print `Do something here`.

```javascript
{
  url && <div>Do something here</div>
}
```

## Puppeteer Project Used functions

### Import a node package to JS file

Install the package.

```bash
npm i puppeteer
```

Open the JS file (example.js) and add the following code to import puppeteer.

```javascript
const puppeteer = require('puppeteer')
```

### Better version of settimeout

```javascript
// This script will pause the application for 1 second
await new Promise((resolve) => setTimeout(resolve, 1000))
```

## Export a JavaScript for as CJS module.

Let create a file called common.js. Add the following lines of code into that file.

```javascript
// Define some constants
const APP_NAME = 'My App'
const VERSION = '1.0.0'
const baseDomain = 'https://app.me/'
const baseFolderName = 'app'
const baseDir = `./${baseFolderName}` // Base directory for offline files (Folder name)
const zipFileName = `${baseFolderName}.zip`
const zipFileOutputDir = './' // root directory of the script.
const logDir = `./log`

const dynamicPageUrl = 'https://app.me/mahbub'

// Define a common function
function greet(name = '') {
  return `Hi ${name}, Welcome to ${APP_NAME} v${VERSION}`
}

// Export constants and function
module.exports = {
  baseDomain,
  baseDir,
  baseFolderName,
  zipFileName,
  zipFileOutputDir,
  dynamicPageUrl,
  APP_NAME,
  VERSION,
  logDir,
  greet,
}
```

Open the JS file (example.js) and add the following code to import puppeteer.

```javascript
//Destructuring all the variables and methods
const { baseDomain, baseDir, baseFolderName, zipFileName, logDir, greet } = require('common')
//Use the method of exported file.

const sayHello = greet('Mahbub')
// Will print 'Hi Mahbub, Welcome to My App v1.0.0'
console.log(sayHello)
```

## ESM VS CJS

![ESM VS CJS](/previews/esm_vs_cjs.png)

## Acknowledgement:

[https://bluewindlab.net](https://bluewindlab.net)
