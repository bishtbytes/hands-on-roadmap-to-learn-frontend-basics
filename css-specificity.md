# Specificity

Browser gives each style specificity rating which can even beat order of occurrence of style.

```css
div > span {
  color: red;
}

span {
  color: yellow;
}

* {
  color: yellow;
}
```

Specificity number consist of three parts:

- A - Count of ID selectors
- B - Count of class and attribute selector
- C - Count of type selectors

  `*`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a=0 b=0 c=0 -> specificity = 0  
   `li`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a=0 b=0 c=1 -> specificity = 1  
   `ul li`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a=0 b=0 c=2 -> specificity = 2  
   `li.red`&nbsp;&nbsp;&nbsp; a=0 b=1 c=1 -> specificity = 11  
   `#content` a=1 b=0 c=0 -> specificity = 100

**NOTE:** The inline style is even more specific to all the above calculations of specificity.
