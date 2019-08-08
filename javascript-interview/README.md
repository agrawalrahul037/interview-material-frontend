# Javascript practice tricky program collection from different sites
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

``` javascript

var myObject = {
    foo: "bar",
    func: function() {
        var self = this;
        console.log("outer func:  this.foo = " + this.foo);
        console.log("outer func:  self.foo = " + self.foo);
        (function() {
            console.log("inner func:  this.foo = " + this.foo);\\ this will be represent to myObject. Because this refer to only one level
            console.log("inner func:  self.foo = " + self.foo);
        }());
    }
};
myObject.func();
```
