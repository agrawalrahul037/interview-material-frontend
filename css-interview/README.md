# CSS Interview Questions

### Table of Contents

| No. | Questions |
| --- | --------- |
|   | **CSS Interview** |
|1  | [How's we will align a horizontal and vertical center div css ?](#horizontal-and-vertical-center-div) |
|2  | [Grid classes in bootstrap 4 ?](#Grid-classes-in-bootstrap-4) |


## Core React

1. ### Horizontal and Vertical center div?

  ```javascript
<!DOCTYPE html>
<html>
   <head>
      <style>
         .inner-div {
         position:absolute;
         width:100px;
         height:100px;
         border:1px solid red;
         left:0;
         right:0;
         top:0;
         bottom:0;
         margin: auto ;
         }
      </style>
   </head>
   <body>
      <div>
         <div class="inner-div">
         </div>
      </div>
   </body>
</html>
  ```
2- ### Grid classes in bootstrap 4
The Bootstrap 4 grid system has five classes:
  ```javascript
.col- (extra small devices - screen width less than 576px)
.col-sm- (small devices - screen width equal to or greater than 576px)
.col-md- (medium devices - screen width equal to or greater than 768px)
.col-lg- (large devices - screen width equal to or greater than 992px)
.col-xl- (xlarge devices - screen width equal to or greater than 1200px)
```
The classes above can be combined to create more dynamic and flexible layouts.
