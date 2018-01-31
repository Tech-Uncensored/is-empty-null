/// Is empty or null 

## Simple example for how to publish npm packages for discord channel

### code is simple
---

```javascript
// Main package function
function isNullOrEmpty(input) {
  // Returns true if the input is either undefined, null, or empty, false otherwise
  return input === undefined || input === null || input === ""
}

// Make the main function available to other packages that require us
module.exports = isNullOrEmpty
```
### and then
---
```javascript
// Change './index' to 'is-null-or-empty' if you use this code outside of this package
const isNullOrEmpty = require("./index")

console.log(isNullOrEmpty("")) // true
console.log(isNullOrEmpty(null)) // true
console.log(isNullOrEmpty(undefined)) // true

console.log(isNullOrEmpty("Hello World")) // false
