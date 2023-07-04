- [1. this Confusion](#1-this-confusion)

# 1. this Confusion
[React Video Link(25:00)](https://www.youtube.com/watch?v=QLxjMwVu0xY&list=PLHiZ4m8vCp9M6HVQv7a36cp8LKzyHIePr&index=10)
```javascript
const javascript = {
  name: 'JavaScript',
  libraries: ['React', 'Vue', 'Angular'],
  printLibraries: function () {
    this.libraries.forEach(function (library) {
      console.log(`${this.name} loves ${library}`)
    }, bind(this));
  }
}
```
- In this example, `name` in `printLibraries` won't be printed unless `bind(this)` is used. Here the function within the `forEach` is a callback function and this within it returns `window` not the `javascript` object.
- Another solution is to use an `arrow function`. It overcomes the confusion of `this` which is another reason to use it.

```JavaScript
printLibraries: function () {
  this.libraries.forEach( (library) => {
    console.log(`${this.name} loves ${library}`)
  });
}
```