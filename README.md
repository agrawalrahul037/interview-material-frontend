# interview-material-frontend
all interview material related to front end

# IMPORTANT PROGRAMS FOR INTERVIEW

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
              
