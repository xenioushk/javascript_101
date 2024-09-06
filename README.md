# JavaScript 101

A dialy used javascript code repository

## Define functions (3 styles)

### Style 1

```javascript
// regular style.
function helloWorld() {
  console.log("hello world")
}

// call the function
helloWorld()
```

### Style 2

```javascript
// assigned to a constant
const helloWorld = function () {
  console.log("hello world")
}

// call the function
helloWorld()
```

### Style 3

```javascript
// arrow function.

const helloworld3 = () => {
  console.log("hello world")
}

// call the function
helloWorld()
```

## Array map

**Example 1**

```javascript
const myArray = ["JS", "CSS", "HTML5", "PHP", "JAVA"]

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

## Acknowledgement:

[https://bluewindlab.net](https://bluewindlab.net)
