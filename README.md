# Unexpected Behavior of :nth-child Selector with Mixed Elements

This repository demonstrates an issue with the CSS `:nth-child` selector when used within a list containing mixed element types. The selector doesn't accurately target every other list item if other elements are interspersed.

The `bug.css` file contains the problematic CSS code, while `solution.css` offers a corrected approach.

## Problem

The initial code uses `li:nth-child(even)` to style every other list item.  However, when elements other than `li` (like `<div>`) are included within the list, the selector incorrectly applies the styling to these other elements as well.  The solution illustrates a more robust method to correctly style every other list item, regardless of other elements' presence.

## Solution

The solution employs the `:nth-of-type` pseudo-class, which only selects every other list item of a specific type, thus avoiding the issues encountered with `:nth-child`.