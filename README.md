# JavaScript 101

A dialy used javascript code repository

## Template literals

**Example: 1**

If `isBlobUrl(url)` returns `true` then output class name will be `my-class-img is-loading`. Else, it outputs `my-class-img`

```html
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
