# Javascript practice tricky program collection from diffent sites
https://www.toptal.com/javascript/interview-questions#note

```javascript
(function(){
  var a = b = 3;
})();

console.log("a defined? " + (typeof a !== 'undefined'));   // false
console.log("b defined? " + (typeof b !== 'undefined'));   // true

solution-> var a = b =3 will be treated as 
           b = 3
           var a = b   // a will not be accessible outside the function
```
