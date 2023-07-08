# css-reset
Aims to ensure rendering consistency across different browsers.

---

## PROBLEM 👎🏼
Inconsistent default stylesheets across web browsers create disparities in how elements like margins, padding, line heights, and font sizes are rendered, compromising web design uniformity and user experience.

## SOLUTION 👍🏼
CSS reset is utilized to standardize these inconsistencies by overriding most default styles with a basic set of rules. This offers developers a clean slate, free from browser-specific defaults, facilitating a more consistent design across all browsers.

---

**NOTE:** This reset is opinionated, reflecting **my** preferred defaults.

---

# CSS Reset Breakdown

## HTML Selector

The root HTML element is selected to define several baseline styles:

- `box-sizing: border-box;`: This changes the CSS box model used by this document and its descendants to include padding and border in an element's total width and height.
- `-webkit-font-smoothing: antialiased;` and `-moz-osx-font-smoothing: grayscale;`: These properties enhance the smoothness of the text. While `-webkit-font-smoothing` is for WebKit browsers like Chrome or Safari, `-moz-osx-font-smoothing` caters to Firefox.
- `-webkit-text-size-adjust: 100%;`: This property prevents the browser, in this case, WebKit-based ones, from automatically resizing the text. It helps maintain the designed text size across various devices.
- `-webkit-tap-highlight-color: rgba(0, 0, 0, 0);`: This removes the highlight that appears when a link or a form element is tapped in WebKit browsers.
- `font-size: 100%;`: This sets the base font size to be the default of the browser, typically 16px. Using percent allows users to adjust their browser settings if needed for accessibility.
- `height: 100%;`: This makes the HTML element take up the full height of the viewport, which can be useful for certain layout designs.

## Universal Selector and Pseudo-elements

The `*`, `*::before`, `*::after` selectors target all elements, including their `::before` and `::after` pseudo-elements:

- `box-sizing: inherit;`: This property makes all elements inherit the `box-sizing` property from their parent element. It ensures consistency in how element dimensions are calculated.

## Body Selector

The body of the document is selected to apply several basic styles:

- `margin: 0;` and `padding: 0;`: These remove default margins and padding applied by the browser, ensuring a consistent starting point for additional styles.
- `font-family: Arial, sans-serif;`, `font-size: 1rem;`, and `line-height: 1.5;`: These properties set the default typography for the document.
- `color: #212529;` and `background-color: #fff;`: These set the default text and background colors.
- `text-align: left;`: This property aligns the text to the left.
- `height: 100%;`: This makes the body element take up the full height of its parent element, in this case, the HTML element.
- `display: flex;` and `flex-direction: column;`: These properties set up a flexbox context for the layout of child elements within the body.

## Input, Button, Textarea, and Select Selectors

The properties applied to these form elements are:

- `font-family: inherit;`, `font-size: inherit;`, `line-height: inherit;`: These properties make sure form elements inherit the font properties from their parent elements, ensuring typographical consistency.

## Button and Input Selectors

The `button` and `input` elements have one specific property:

- `overflow: visible;`: This property ensures that if the content exceeds the bounds of these elements, it will not be clipped and hidden.

## Button and Select Selectors

The `button` and `select` elements have:

- `text-transform: none;`: This property makes sure the text within these elements is not transformed, preventing any unwanted capitalization or lowercase effects.

## Button, Type Button, Type Reset, and Type Submit Selectors

The properties applied to these button types are:

- `-webkit-appearance: button;`: This property makes these types of buttons appear like standard buttons in WebKit browsers. It helps maintain a consistent look across browsers.

## Anchor Selector

For anchor (`a`) tags:

- `text-decoration: none;`: This property removes the default underline style from the links.
- `color: inherit;`: This property makes the link text inherit the color of its parent, ensuring color consistency.

