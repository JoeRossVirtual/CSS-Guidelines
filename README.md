# CSS Guidelines


This repo contains the CSS guidelines for Virtual as well as the company wide CSS used on client sites.  The live documentation for the company CSS can be found in the `index.html` file.  When writing CSS for clients stick to the following guidelines.

## Structure
Indentation: 4 spaces
When using multiple sectors, place each on its own line for example...
```css
.selector-one,
.selector-two {
    color: blue;
}
```
Every major section should have a comment heading to describe the contents of the block.  Regular comments can be used to explain smaller sextions
```css
/* ----- Example Section ----- */
.example-section-selector-one {
    ...
}
/* This is for changing how ... */
.example-section-selector-two {
    ...
}
```

## Selectors
* Try to stay as general as possible.
* Avoid over-qualified selectors.
* Use dashes to separate words (not camelCase).
* Use classes rather than element selectors (adds flexibility, but adds redundancy)


## Properties
For colors, use hex unless transparency is needed.
Prefixes (probably should use some sort of autoprefixer) generally ordered from longest (-webkit-) to shortest (no prefix)

Property ordering: WordPress core suggests
* Display
* Positioning
* Box model (padding, margin, border…)
* Colors and Typography
* Other


## Media Queries
Media queries generally go at the bottom of the document.  We should probably just use a couple breakpoints and fit all the necessary code into them rather than writing new breakpoint code each time we need new responsive styles (like on the NFC site).  Section headers should be used the same as specified above with the same name of the related section so code can be understood quickly.


## Avada
Try to avoid page specific CSS except for quick fixes that will have no use anywhere else.
When working on new features use the Custom CSS section of the Avada settings until you have completed development.  Then move your code to the child theme using git push.