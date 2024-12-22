# Uncommon HTML Bug: Incorrect Element Selection

This repository demonstrates a subtle bug related to element selection in JavaScript within an HTML document.  The bug arises from an attempt to select an element by class using `document.querySelector` when it should use `document.getElementByClassName`.

## Bug Description
The provided HTML code snippet has a JavaScript section that incorrectly uses `document.querySelector(".myClass");` to select an element with the class "myClass".  This method will only work if there's only one element with that class. If multiple elements share the class, only the first one will be selected, which is not the intended outcome. 

## Solution
The solution involves replacing the incorrect selector with the appropriate method `document.getElementByClassName("myClass")[0];`  This method returns an array of elements; the `[0]` will select the first element within the array. If you are sure there is only one such element with class 'myClass', it would also work to use `document.querySelector(".myClass");`.