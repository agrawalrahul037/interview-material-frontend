# interview-material-frontend
all interview material related to front end

# IMPORTANT PROGRAMS FOR INTERVIEW
1- Palindrome Program

```javascript
function mypalindrom(str){
var i = 0;
var j = str.length-1;
while(j>0){
 if(str[i++] != str[j--]){
   console.log("it is not palindrom");
   return;
 }
}
 console.log("it is palindrom");
}
mypalindrom("aabaa");

```

# Sapient Coding Test

1- find Longest match of Palindrome ina string after that if this Palindrome string length is prime or not?
   if It's prime then return "YES" else "NO"
   
   Solution->
   ---------
   
   ```javascript
   function solution(str1) {
    var max_length = 0,
        maxp = '';

    for (var i = 0; i < str1.length; i++) {
        var subs = str1.substr(i, str1.length);

        for (var j = subs.length; j >= 0; j--) {
            var sub_subs_str = subs.substr(0, j);
            if (sub_subs_str.length <= 1)
                continue;

            if (is_Palindrome(sub_subs_str)) {
                if (sub_subs_str.length > max_length) {
                    max_length = sub_subs_str.length;
                    maxp = sub_subs_str;
                }
            }
        }
    }
    if (isPrime(maxp.length)) {
        return "YES"
    } else {
        return "NO";
    }
}

function is_Palindrome(str1) {
    var rev = str1.split("").reverse().join("");
    return str1 == rev;
}

function isPrime(n) {
    if (n === 1) {
        return false;
    } else if (n === 2) {
        return true;
    } else {
        for (var x = 2; x < n; x++) {
            if (n % x === 0) {
                return false;
            }
        }
        return true;
    }
}
solution("random12121mrando")
   
   ```

# Nagarro coding test programs

1- Suppose i have two variables having same name and we are wrting in c++ and java then we will write it like below. <br>
   this_is_a_variable        // if we are wrting it in c++  <br>
   thisIsAVariable          // if we are writing it in java <br>
   
   Solution->
   ----------
   
   ```javascript
   function myprogram(str) {
    var newStr = "";
    var underPosition = str.indexOf("_");
    var underPositionNext = 0;
    if (underPosition > 0) {
        for (var i = 0; i < str.length; i++) {
            if (str[i] !== "_") {
                newStr += (underPositionNext > 0) ? str[i].toUpperCase() : str[i];
                underPositionNext = 0;
            } else {
                underPositionNext = i + 1;
            }
        }
    } else {
        for (var j = 0; j < str.length; j++) {
            if (str.charCodeAt(j) > 90) {
                newStr += str[j];
            } else {
                newStr += "_"
                newStr += str[j].toLowerCase();
            }
        }
    }
    return newStr;
}
var a = myprogram("this_is_a_variable");
console.log(a);   // output thisIsAVariable
var b = myprogram("thisIsAVariable");
console.log(b)   // output this_is_a_variable
```
              
