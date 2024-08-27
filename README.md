# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```

# Answer 08/27/2024
This is a recursive function that takes an array as an input, and finds the largest number in that array.
It does so by slicing the array until there is only one element in it.
Each instance of a string being sliced down by one element is saved in the call stack.
When the base case is reached, the function unwinds and iterates over every sliced string, and compares them to eachother to eventually find the largest number.
