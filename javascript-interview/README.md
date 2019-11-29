# Javascript Interview Questions

### Table of Contents

| No. | Questions |
| --- | --------- |
|   | **Javascript Interview** |
|1  | [How's singleton design pattern work in javascript ?](#singleton-pattern-in-javascript) |
|2  | [Call/Apply/Bind/Curring Example ?](#call-apply-bind-curring) |

1. ### singleton pattern in javascript?

```javascript
var SingletonFactory = (function(){
    function SingletonClass() {
        //do stuff
    }
    var instance;
    return {
        getInstance: function(){
            if (instance == null) {
                instance = new SingletonClass();
                // Hide the constructor so the returned object can't be new'd...
                instance.constructor = null;
            }
            return instance;
        }
   };
})();
var test = SingletonFactory.getInstance();
```
2. ### call apply bind curring?

```javascript
<!DOCTYPE html>
<html>

<body>
    <script>
        var person = {
            firstname: "Rahul",
            lastname: "Agrawal",
            getFullName: function () {
                var fullname = this.firstname + ' ' + this.lastname
                return fullname;
            }
        }
        var collectInfo = function (lang1, lang2) {
            console.log("full name===========" + this.getFullName());
            console.log("lang1=================" + lang1);
            console.log("lang2=================" + lang2)
        }
        var myInfo = collectInfo.bind(person);  //After using bind method [Inside collectInfo function this will refer to person Object]
        // myInfo();
        // myInfo.call();    // we can call any function using call method also
        //collectInfo.call(person, "en","es");  // we pass parameters as a comma seperated
        //collectInfo.apply(person, ["en", "es"]);  // we pass parameters as a array

        // function multiply(a,b){
        //     return a*b;
        // }
        //var multiplyByTwo = multiply.bind(this,2) // second parameter is permanent value which will used in multiply function as a first parameter
        //console.log(multiplyByTwo(3)); // 6
        //var multiplyByTwo = multiply.bind(this,2,4) // second and third parameter are permanent value which will used in multiply function as a first and second parameter
        //console.log(multiplyByTwo(3)); // 8  output will be 8 because of default value weither we pass anything
        function multiply(a) {
            return function (b) {
                return a * b;
            };
        }
        console.log(multiply(2)(3));   // function curring example
    </script>
</body>

</html>
```
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
            console.log("inner func:  this.foo = " + this.foo); //this will be represent to myObject. Because this refer to only one level
            console.log("inner func:  self.foo = " + self.foo);
        }());
    }
};
myObject.func();
```
