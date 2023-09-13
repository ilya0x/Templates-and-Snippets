# SCSS Notes

<h3> Table of Contents</h3>

- <b>[SCSS vs SASS](#scss-vs-sass)</b>
- <b>[Generated Files using Live Sass Compiler extension](#generated-files-using-live-sass-compiler-extension)</b>
- <b>[SCSS Variables](#scss-variables)</b>
- <b>[Maps](#maps)</b>
- <b>[Nesting](#nesting)</b>
- <b>[Separating files - modularizing your SCSS files](#separating-files---modularizing-your-scss-files)</b>
- <b>[Functions](#functions)</b>
- <b>[Mixin](#mixin)</b>
- <b>[Extend](#extend)</b>
- <b>[Math Operations](#math-operations)</b>
<br>
<br>
<br>

## SCSS vs SASS

- SCSS - Sassy CSS, SCSS Syntax: uses curly braces & semicolons same as CSS
- original Sass: Indented Syntax: uses indentation, .sass extension

> I will be using `*.sass` file extension as it allows use of indentation rather
> then brackets, which is more Pythonic...

## Generated Files using Live Sass Compiler extension

- creates the .css file and .css.map file:
  - do not edit the generated .css as it gets overwritten every time its compiled.
  - .css.map file:
    - `"sources":["main.scss","main.css"]` points to original source files that
      were used to generate the CSS. These paths are relative to the location of
      the source map file.
    - `"file":"main.css"` name of CSS file the source map corresponds to.

## SCSS Variables

`$variable-one: #000000;`<br>
`$variable-two: pink;`

`body {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`background: $variable-one;`<br>
`}`

## Maps

Using a variable, assign key-value pairs in parentheses:

Example:

`$font-weights: (`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`"regular": 400,`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`"medium": 500,`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`"bold": 700,`<br>
`);`

`body {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`font-weight: map-get(#font-weights, regular)`

## Nesting

- styling an html element that is inside a main html element, making the style
  apply only within that element, not globally.

Example:

`.main {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`width: 80%;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`margin: 0 auto;`<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;`/* "&" = the parent (ie .main).`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`Use interpolation with "#" to wrap "&" to get
everything before it */`<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;`#{&}__paragraph {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`font-weight:
map-get(#font-weights, bold);`<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&:hover {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`color: $variable-two;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`}`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`}`<br>
`}`<br>

## Separating files - modularizing your SCSS files

- a partial SCSS file is indicated by name starting with `underscore`.
- separate resets and variables into their corresponding partials files.

> Do NOT use `@import './file-name';` to include partials files.

- use `@use './file-name';` to include partials files.
  - it prevents collisions by requiring specified namespace:<br>
  `file-name.$style-name` rather than just `$style-name`

<i>Note:</i> does NOT need file extension.

## Functions

- Compute and return values

Example:

`@function weight(&weight-name) {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`@return map-get($font-weights, &weight-name);`<br>
`}`<br>

- using function and passing in the `font-weight` choice (from `_variables.scss`
  partial file):

  `font-weight: weight(bold);`

## Mixin 

- Define Styles
- use `@mixin` to create snippets of css that can be "mixed into" any style

Example:

`@mixin flexCenter {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`display: flex;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`align-items: center;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`justify-content: center;`<br>
`}`<br>

`.main {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`@include flexCenter;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`//! "mixes in" flex related snippet of style`<br>

&nbsp;&nbsp;&nbsp;&nbsp;`width: 80%;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`margin: 0 auto;`<br>
`}`<br>

Example: choosing between a light and dark theme

`@mixin theme($light-theme: true) {` (assign Boolean value to variable)<br>
&nbsp;&nbsp;&nbsp;&nbsp;`@if $light-theme {` (if light-theme is true)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(light theme styles:)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`background: lighten($variable-one, $amount: 100%);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`color: darken($variable-two, $amount: 100%);`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`}`<br>
`}`<br>

`.light {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`@include theme($light-theme: true);`<br>
`}`<br>

Example: Media Query - change layout depending on window size

added `$mobile: 800px;` to `_variables.scss`

`@mixin mobile {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`@media (max-width: $mobile) {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`@content;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`}`<br>
`}`<br>

`.main {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`...`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`@include mobile{`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`flex-direction: column;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`}`<br>
`}`<br>

## Extend

- extend a class with `@extend` to have its properties applied to the parent class

Example:

`.main {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`...`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`#{&}__paragraph1;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`font-weight: weight(bold);`<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&:hover {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`color: pink;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`}`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`}`<br>

&nbsp;&nbsp;&nbsp;&nbsp;`#{&}__paragraph2;`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`@extend .main__paragraph1;`
extends all styles from __paragraph1<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`&:hover {`<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`color:
blue;` supersedes the extended style<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`}`<br>
&nbsp;&nbsp;&nbsp;&nbsp;`}`<br>

## Math Operations

- does NOT need `calc()` function
- has to be same type (%, px, etc.)
- SCSS passes through only the result
- if using `calc()` function, SCSS will pass through the whole thing including operation