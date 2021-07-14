 
 
 * go to any website and select its heading and inspect elements 
 * e.g javascript wikipedia website
 * select javascript text which is at heading
 * inspect it
 * $0 would be written in front of it
 * go to console 
 * write 
```javascript
$0;
```
* it will give you the heading
* write 
```javascript
$0.innerHTML = "TannuScript";
```
* it will change the heading to TannuScript

* now if we want, we can add event listener to the heading on website using console
```javascript
$0.addEventListener("click", function(){
    console.log("I got clicked");
});
```
* now when we will click the heading , it will give alert I got Clicked
* this was an anonymous function, we can also create function seperately like below
```javascript
$0.addEventListener("click", respondToClick);

function respondToClick(){
    console.log("I got clicked");
}
```

* we can see that the event listener is taking two inputs, first what event shound listen to 
* and second one specifying what it should do once that event gets detected
* we can see that this eventListener function is little bit different, instead of passing 
* integers or characters as parameter, we are passing numbers

* now let us understand the use of passing functions in parameter by taking one more example
```javascript
function add(num1, num2){
return num1 + num2;
}

function multiply(num1, num2){
    return num1*num2;
}

function calculator(num1, num2, operator){
    return operator(num1, num2);
}
```
* i can create a calcultor by adding different functions, and instead of calling different functions
* we will call same function and passing different parameter for different operation
* that parameter will be operator  function and that will get attached in front of called function

* we can go to debugger mode by printing
debugger; //in console and then hold shift and write the function you want to debug, e.g
calculator(3, 4, multiply);
* now click the arrow dot in right side and you can see what values are returned by or asisgned to each var and function by computer

 ----------------------------------------------------------------------------------------------------------
* CONCLUSION : 

"Higher order functions are functions that can take other functions as input"



















