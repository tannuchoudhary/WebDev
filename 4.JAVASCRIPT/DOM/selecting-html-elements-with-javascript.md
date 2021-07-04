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
## you can select and manipulate items by query selector or get elements let's see how to manipulate using getElement:

* we can get elements by:
    * getElementsByTagName
    * getElementsByClassName
    * getElementByID

## getElementsByTagName
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
## getElementsByClassName

The same goes with the class, you can't select the whole item and manipulate it, you have to choose the array index, for e.g
```javascript
document.getElementsByClassName("btn").style.color="red";
```
this will give an error because in the above code, there is only one button and in the created array there will be only one element but still you have to choose the index of element, somehting like this:

```javascript
document.getElementsByClassName("btn")[0].style.color="red";
```
this will make the color of the text in the button as red














