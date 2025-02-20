# CSS Specificity and !important: An Uncommon Bug

This repository demonstrates an uncommon issue related to CSS specificity and the `!important` declaration.  The bug showcases a scenario where `!important` unexpectedly overrides higher-specificity selectors, leading to unexpected styling results.

## Bug Description

The `!important` flag in CSS is typically used to override styles from other selectors, even those with higher specificity. However, this can lead to unexpected behavior when not managed carefully. The bug presented here involves a scenario where a more specific selector's style is overridden by an earlier, less specific selector with the `!important` declaration. This can be challenging to debug as it goes against the normal rules of CSS specificity. 

## How to Reproduce

1. Clone this repository.
2. Open `bug.css` to see the problematic CSS code.
3. Create an HTML file that applies the classes (`parent` and `child`) and observe the resulting text color (it will be red, not green as intuitively expected).

## Solution

The solution involves understanding the behavior of `!important` and refactoring the CSS to avoid unnecessary `!important` declarations. Refer to `bugSolution.css` for the corrected code. It's almost always best to avoid `!important` altogether and manage styles using proper specificity.

## Conclusion

This example highlights the importance of understanding CSS specificity and using the `!important` declaration judiciously. Unnecessary use of `!important` can lead to maintenance headaches and unpredictable styling.