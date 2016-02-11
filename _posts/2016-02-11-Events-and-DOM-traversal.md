---
layout: post
title: Events and DOM traversal
---
`getElementById(id)` - Returns the first element in the document that matches the given ID, id.

`getElementsByClassName(class)` - Returns all elements in the document that match the given class name, class.

`getElementsByTagName(name)` - Returns the elements in the document that have the given tag name, name.

`querySelector(selector)` - Returns the first element in the document that matches the given CSS selector, selector.

`querySelectorAll(selector)` - Returns all elements in the document that match the given CSS selector, selector.


**Events:**
`click`: user clicks on some element

`focus`: an element on the page is focused

`blur`: an element on the page loses focus
submit: a form is submitted

`mouseOver`: user moves the mouse over an element

`mouseOut`: user moves the mouse out of an element
load: an element has loaded (window, image)

`DOMContentLoaded`: DOM is ready to access

<script src="https://gist.github.com/bigappleinsider/89a090d35b6a88b5e3b3.js"></script>

Sources:
1. https://docs.google.com/presentation/d/1-Y5XNfA0u1RCrkpENc6VIPbHPOkchsf6yM7Yk3K_OvU/edit?usp=sharing
2. http://callbackjs.me/
