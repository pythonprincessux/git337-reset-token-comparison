# Reset and Token Comparison Record

## No Reset

### Useful browser defaults observed
1. Unordered lists displayed visible bullets and useful indentation.
2. Links were underlined, making them recognizable as links.
3. Keyboard focus remained visibly identifiable when tabbing through interactive elements.
4. Headings had a clear visual hierarchy between heading levels.
5. Form controls were visually recognizable as interactive controls.

### Defaults that conflicted with the design
1. Default heading margins created more vertical spacing than I wanted.
2. The browser's default button appearance did not match the visual style of the page.

## Broad Reset

Using the broad reset removed several useful browser defaults.

1. Heading hierarchy was visually flattened because `font: inherit` removed the browser's default heading typography.
2. List indentation and spacing were reduced because margins and padding were reset to zero.
3. Figure and surrounding content spacing became tighter because the default margins were removed.

The text link remained underlined, and I confirmed that keyboard focus was still visible during browser testing.

## Selective Reset

I chose a short selective reset instead of removing all browser defaults.

- `box-sizing: border-box` makes sizing more predictable by including padding and borders within an element's declared dimensions.
- `body { margin: 0; }` removes only the browser's outer page margin so the project can control page spacing.
- Responsive image rules keep images from becoming wider than their containers while preserving their proportions.

This approach preserved useful defaults such as heading hierarchy, list bullets, recognizable links, and keyboard focus while removing only defaults that conflicted with the project.

## Token Comparison

I identified repeated values in `component-styles.css` and replaced them with reusable custom properties for color, spacing, radius, and typography.

Semantic color tokens included values for:
- text
- surface
- border
- action
- action text

Repeated spacing, radius, and typography values were also converted to reusable tokens.

The `.theme-alt` selector overrides the semantic token values rather than duplicating the component rules. This allows the alternate card to use a different surface, text, border, and action treatment while the default cards continue using the original token values.