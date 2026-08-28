# AI Assistance Disclosure

I used ChatGPT to help review my CSS reset choices, identify repeated CSS values, organize those values into reusable custom properties, and troubleshoot the scoped alternate theme.

ChatGPT suggested a selective reset using `box-sizing`, removing the default body margin, and responsive image sizing. I tested the reset changes in the browser and compared them with the no-reset and broad-reset versions.

For the token portion, ChatGPT helped identify repeated values and suggested semantic token names for colors, spacing, radius, and typography. I used those suggestions to replace repeated literal values with CSS custom properties and `var()` references.

ChatGPT also suggested using a scoped `.theme-alt` rule to redefine token values without duplicating the component styles. I verified this approach using MDN documentation on CSS custom properties and the `var()` function. MDN explains that custom properties participate in the cascade, can be scoped to selectors, inherit through descendants, and can be referenced using `var()`.

I tested the changes in the browser throughout the process and retained the suggestions that produced the intended layout and theme behavior. I can explain the final reset choices, token hierarchy, and scoped theme implementation.

Finally, Chat helped me polish and organizing raw thoughts and notes for ai-disclosure responsibilities and comparison-record.md. 

## Verification

I verified the AI suggestions using MDN Web Docs and browser testing.

- MDN: Using CSS custom properties (variables)
  - I verified that custom properties can store reusable values, participate in the cascade, inherit from parent elements, and can be scoped to specific selectors.
  - I used this information to verify the `.theme-alt` token overrides.

- MDN: var() CSS function
  - I verified that `var()` inserts the value of a CSS custom property into another CSS property.
  - I used this information to verify the token references in `component-styles.css`.

Browser testing:
- I compared the page using no reset, the broad reset, and the selective reset.
- I tested the page after replacing repeated literal values with custom properties.
- I verified that the default components retained their styling while the scoped alternate theme used the overridden token values.