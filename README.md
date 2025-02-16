# Uncommon HTML Bug: Accessing DOM Element Before Rendering

This repository demonstrates a common yet often overlooked error in HTML and JavaScript: attempting to access a DOM element before the browser has finished rendering it.  This typically leads to a `null` value or a runtime error, preventing the intended modifications from taking effect.

## The Problem

The `bug.html` file shows an example where JavaScript attempts to modify the content of an element that does not yet exist in the DOM. This happens because the browser hasn't fully parsed and rendered the HTML before the script attempts to access the element.

## The Solution

The `bugSolution.html` file demonstrates the correct approach: using an event listener (e.g., `DOMContentLoaded` or `load`) to ensure that the script executes only after the DOM is fully ready.

This ensures that the JavaScript code always interacts with valid DOM elements, preventing errors and ensuring consistent behavior across different browsers and devices.