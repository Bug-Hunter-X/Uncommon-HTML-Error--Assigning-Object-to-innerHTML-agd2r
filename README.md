# Uncommon HTML Error: Direct Object Assignment to innerHTML

This repository demonstrates a subtle error that can occur in HTML when working with JavaScript and the `innerHTML` property.  The error arises from attempting to directly assign a JavaScript object to the `innerHTML` property of an HTML element. This is not supported; `innerHTML` expects a string.  The solution showcases the correct way to handle object data within HTML by converting it into a string representation.

## Bug Description
The bug involves incorrect usage of `innerHTML`.  The JavaScript code attempts to directly assign a JavaScript object to `innerHTML`.  This results in an error because `innerHTML` requires a string value.  Browsers usually handle this by logging a console error and simply not doing anything. This makes the bug somewhat difficult to spot.

## Solution
The solution involves converting the object into a string representation using `JSON.stringify()` before assigning it to `innerHTML`.  This converts the JavaScript object into a valid string that can be parsed and displayed in the HTML element.  It provides a workaround to insert JSON data into HTML