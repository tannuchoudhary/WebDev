# In this we will learn how to select and manipulate HTML elements using Javascript

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
## you can select and manipulate items by query selector or get elements let's see how to manipulate using getElement:

* we can get elements by:
    * getElementsByTagName
    * getElementsByClassName
    * getElementByID

## getElementsByTagName:
```javascript
document.getElementsByTagName("li");
```
this will fetch all the list
output:
```javascript
HTMLCollection(3) [li.item, li.item, li.item]
```














