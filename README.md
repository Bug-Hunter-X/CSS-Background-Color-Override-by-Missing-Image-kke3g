# CSS Background Color Override by Missing Image

This repository demonstrates a subtle CSS bug where the `background-color` is unexpectedly overridden by a missing `background-image`.  The browser, prioritizing the image, ignores the color if the image path is incorrect or the file is missing.  This can lead to unexpected visual results, especially if fallback mechanisms aren't implemented.

The `bug.css` file contains the buggy code. The `bugSolution.css` file offers a solution to this problem.

## Bug
The issue lies in the order of precedence given by browsers when rendering `background-image` and `background-color`.  If an image is specified and fails to load, it can prevent the `background-color` from being displayed. 

## Solution
The solution involves using the `background` shorthand property.  This allows you to set multiple background properties at once and allows for better control over image failure.

## How to reproduce
1. Open `bug.html` in a web browser.
2. Observe that the div does not show the expected red background.
3. Open `bugSolution.html` in a web browser.
4. Observe that the div now correctly displays the red background.