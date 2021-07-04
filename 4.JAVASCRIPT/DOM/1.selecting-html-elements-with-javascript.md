# In this we will learn how to select and manipulate HTML elements using Javascript
## HTML
``` html
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>My Website</title>
    <link rel="stylesheet" href="styles.css">

  </head>
  <body>

    <h1 id = "title">Hello</h1>

    <input type="checkbox">

    <button class="btn" style=":active color:red;">Click Me</button>

    <ul id="list">
      <li class="item"><a href="https://www.google.com">Google</a></li>
      <li class="item">Second</li>
      <li class="item">Third</li>
    </ul>

  </body>
  <footer>
      <script src="index.js" charset="utf-8"></script>
  </footer>

</html>
```
## CSS
```css
h1 {
  color: red;
}
```
## Javascript

```javascript
document.query
```
## you can select and manipulate items by query selector or get elements let's see how to manipulate using getElementBy:

* we can get elements by:
    * getElementsByTagName
    * getElementsByClassName
    * getElementByID
## getElementBy

### getElementsByTagName
```javascript
document.getElementsByTagName("li");
```
this will fetch all the list and output will be:
```javascript
HTMLCollection(3) [li.item, li.item, li.item]
```
now if we'll write this
```javascript
document.getElementsByTagName("li").style.color="purple";
```
it will give error bcz we are telling compiler to color all th list with purple, to color the list item we have to choose index from the list item, like this:
```javascript
document.getElementsByTagName("li")[2].style.color="purple";
```
this will color the 2nd index i.e the third item of list with purple

some more examples:
* generate the length of the array list
```javascript
document.getElementsByTagName("li").length;
```
output will be
```javascript
3
```
### getElementsByClassName

The same goes with the class, you can't select the whole item and manipulate it, you have to choose the array index, for e.g
```javascript
document.getElementsByClassName("btn").style.color="red";
```
this will give an error because in the above code, there is only one button and in the created array there will be only one element but still you have to choose the index of element, somehting like this:

```javascript
document.getElementsByClassName("btn")[0].style.color="red";
```
this will make the color of the text in the button as red

### getElementByID
We can see that here getElement is singular and not plural(i.e it is not getElements) like others, because we know that there are unique id's in web page

Now let us see how to manipulate html elements using getElementByID 

```javascript
document.getElementById("title").innerHTML = "Good Bye;
```
this will change the Hello into Good Bye because 


## Query selector
As we saw that using getElement, we had to specify it differently for classes, id's and tags but in query selector everything will be specified using only one syntax

### for id
```javascript
document.querySelector("#title");
```
we have to use # sign for id


### for class


```javascript
document.querySelector(".btn");
```

### for selecting link inside a list element
select the anchor tag inside the list selector
```javascript
document.querySelector("li a");
```
```javascript
<a href="https://www.google.com">Google</a>
```
as this is hierarchical selector so there will be space between two selectors i.e "li a"

### for selecting element
```javascript
document.querySelector("li a");
```
ouptut
```javascript
<a href="https://www.google.com">Google</a>
```
### for selecting by combining selectors
select class of item having li as element
```javascript
document.querySelector("li.item");
```
as we are combining selectors, therefore things occur in the same elemnt therefore no spaces and hierarchy is same, i.e list item that has class = item
output
```javascript
<li class="item"><a href="https://www.google.com">Google</a></li>
```
### for selecting by combining id and selectors
```javascript
document.querySelector("#list.item");
```
we are looking for an anchor tag that is inside somehting that has an id of list


Now the question is, what if your selctor matches more than one content, for e.g there are many lists with class name as item, then which one will get back, the answer is the first one, yes you will always get the first item in the document that satisfies the selectors. now what if we want all of them which matches selectors, then we have to add something in our code, add "All" inquery selector=


```javascript
document.querySelectorAll("#list.item");
```

Here also you have to specify index to manipulate the data

```javascript
document.querySelectorAll("#list.item")[2].style.color="blue";
```
query selectors are generally used because they allow more complex queries as we are able to able to specify queries, ide class, element, class name, which helps us to target particularly whatever we want and it is difficult in other cases. 

task: color the google link:
we can color the google link using any of below

```javascript
document.querySelector(".item a").style.color="blue";
```

```javascript
document.querySelector("li a").style.color="blue";
```
```javascript
document.querySelector("#list a").style.color="blue";
```



if you will try to select the first list item i.e
```javascript
document.querySelector("li").style.color="blue";
```
then it will only change the color of the bullet point, and not the anchor tag, because anchor tag is different element






