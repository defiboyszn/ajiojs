# Ajiojs is a promise-based HTTP client for browser

# Installation

### Via npm

```bash
$ npm install ajio
```

### Via cdn (Unpkg)

```html
<script src="https://unpkg.com/ajio"></script>
```

# Usage
## Es modules

```javascript
import ajio from "ajio";

ajio.get("https://jsonplaceholder.typicode.com/comments").then((data) => {
  console.log(data);
});
```


### Get

```javascript
var ajio = require("ajio");

ajio.get("https://jsonplaceholder.typicode.com/comments").then((data) => {
  console.log(data);
});
```

### Post

```javascript
var ajio = require("ajio");

ajio
  .post("https://jsonplaceholder.typicode.com/comments", {
    body: {
      name: "Ajio",
      author: "Tobithealpha",
      version: "v0.1.2-beta",
    },

var ajio = require('ajio');

ajio.post('https://jsonplaceholder.typicode.com/comments',{
  body: JSON.stringfy(`{
    name: "Ajio",
    author: "Tobithealpha",
    version: "v0.1.2-beta"
  }`)
})
  .then(data=>{
    console.log(data)
  })
  .then((data) => {
    console.log(data);
  });
```

### Put

```javascript
var ajio = require("ajio");

ajio
  .put("https://jsonplaceholder.typicode.com/comments", {
    body: JSON.stringfy(`
  {
    "postId": 20,
    "id": 501,
    "name": "Tobithealpha",
    "email": "tobithealpha@gmail.com",
    "body": "Ajiojs has been released 😊😊"
  },`),
  })
  .then((data) => {
    console.log(data);
  });
```

### Delete

```javascript
var ajio = require("ajio");

ajio.delete(`https://jsonplaceholder.typicode.com/comments`).then((data) => {
  console.log(data);
});
```
# Whats new!!!

### baseUrl

```javascript
var ajio = require("ajio");

ajio.baseUrl("https://jsonplaceholder.typicode.com");

// then you can use "/" to the path you want use
ajio.get("/comments").then((data) => {
  console.log(data);
});

// or
// using promise method
const getComments = async () => {
  const req = await ajio.get("/comments");
  const res = await req
  return res
}
```
### Patch

```javascript
var ajio = require("ajio");

ajio
  .patch("https://jsonplaceholder.typicode.com/comments", {
    body: JSON.stringfy(
  {
    "postId": 20,
    "id": 501,
    "name": "Tobithealpha",
    "email": "tobithealpha@gmail.com",
    "body": "Ajiojs has been released 😊😊"
  }),
  })
  .then((data) => {
    console.log(data);
  });
```


We Working On Making Ajio Work on Node :)
