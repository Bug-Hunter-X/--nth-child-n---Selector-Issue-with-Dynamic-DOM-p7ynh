# :nth-child(n) Selector Issue with Dynamic DOM

This repository demonstrates a common issue where the CSS `:nth-child(n)` selector fails to function properly after the DOM is dynamically updated.  The problem is often encountered when dealing with JavaScript frameworks or libraries that modify the page's structure after initial rendering.

The `bug.css` file contains the incorrect CSS rule, while `bugSolution.css` shows the corrected approach.

## Steps to Reproduce

1. Clone the repository.
2. Open `index.html` in your web browser.
3. Observe the initial rendering; the incorrect styling is applied.
4. Interact with the button to trigger DOM manipulation.
5. Observe the incorrect selection persistence.
6. View `bugSolution.css` for the resolved implementation.

## Solution

The solution involves using JavaScript to re-apply the styles after the DOM is updated, ensuring the `:nth-child(n)` selector correctly targets the elements in their new positions within the DOM. This avoids reliance on automatic recalculation which may not occur consistently across all browsers.