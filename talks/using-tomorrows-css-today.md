# Using Tomorrow's CSS Today

The glaring thing that Back to the Future missed about 2015 was The Web.

## Text Documents

The web was mostly for medical information. Nothing styled. Just text.

* Tables
* ...then absolute positioning and floats
* ...and finally Flexbox and Grids

## CSS in 2016 is Amazing

### Where have we been? How did we get here?

There is No CSS3!

> Despite the popularity of the "CSS3" buzzword, there is actually no spec defining such a thing. - Lea Verou

*Look up Secrets by Specification `xiii`*

Fun new things:

* Animation
* Typography
* Shapes
* Grids

#### "CSS is not a real language"

*Problems with CSS*

1. Cross-browser compatibility issues
2. Vendor prefixes
3. No variables
4. No nested selectors
5. No scoping
6. No functions
7. No color manipulation
8. No basic arithmetic

### Things That Make Our Lives Easier

Do more in less time and in more organized and efficient ways.

## Rise of the Preprocessors.

How we filled the gaps.

* **Sass**
* **Less**
* **Stylus**

Developer writes code in preprocessor's syntax, a task runner notices that changes and spits out the standards-based CSS.

### Do preprocessors solve the problem?

They add overhead, but get us much farther along than just using vanilla CSS (at least historically).

However, they Perpetuate another problem. They add more abstraction on top of the core CSS language.

#### Problems

* Not real front-end code
* Proprietary syntax
* Often written in non front-end languages
* Not as easily extensible
* Must be compiled
* Compile times can be slow
* The CSS Spec & Browsers are catching up!

## Preprocessors?

Where we're going, we don't need preprocessors.

**The Future of CSS is Now!**

* Variables (available in most evergreen browsers today)
* Mixins/Extensions
* Color manipulation
* Nesting
* Custom Media Queries

### What is available now?

And what about the future?

### Custom Properties (Variables)

```css
:root {
  --color-blue: blue;
  --color-blue-dark: darkblue;
}

.element {
  color: var(--color-blue);
}
.element:hover {
  color: var(--color-blue-dark);
}
```

> Just because you may like Sass variable syntax more does not mean that you should just forsake the new spec.
>
> \- Jake Albaugh

> Variables lose their value if you have to constantly track down what they represent.
>
> \- Ryan Heap

### @Apply (Mixins/Extends)

```css
:root {
  --clearfix: {
    display: table;
    clear: both;
    content: '';
  }

  .element:after {
    @apply --clearfix;
  }
}
```

Still mostly in draft and only supported behind flags in Chrome and Opera.

### Color Module Level 4 (Color Functions)

```css
:root {
  --blue: #1982C5
}
.element {
  color: var(--blue);
}

.element--modifier {
  color: color(var(--blue) tint(40%));
}
.element--shade {
  color: color(var(--blue) shade(40%));
}
```

* Tints and Shades
* RGBA Adjustment
* HSL/HWB Adjustment
* Color Blending (blend & blenda)
* Guarantee Contrast

#### Color Palatte

```css
:root {
  --color-text: var(--color-orange);
  --color-text-light: color(
    var(--color-text)
    tint(40%)
  )
  --color-text-dark: color(
    var(--color-text)
    shade(40%)
  )
}
```

#### Nesting

```css
.element {
  color: blue;

  // Current Draft. It looks dumb
  {&.modifier { color: red; }}
}
```

Be careful how you use nesting. Don't have it look too much like an arrow. 2-3 levels is a good rule-of-thumb not to go past.

```css
// Reasonable order of nesting
.selector {
  property: value;
  &:before  { //... }
  element   { //... }
  .selector { //... }
}
```

#### Custom Selectors

```css
@custom-selector --small (min-width: 30em);

@media (--small) {
  .element {
    font-size: 1.5rem;
  }
}

@custom-selector --headerin h1,h2,h3,h4,h5,h6;

--heading {
  /* styles for all headings */
}

--heading + p {
  /* styles for all headings with a 'p' tag after it */
}
```

#### Media Query Range Context

```css
@media (width <= 30em) {
  // small
}
@media (30em <= width <= 60em) {
  .element {
    font-size: 1.5rem;
  }
}
@media (60em >= width) {
  // large
}
```

## Supporting the Future

* [Autoprefixer](https://github.com/postcss/autoprefixer) - Specify which browser you have to support
* [PostCSS](https://github.com/postcss/postcss) - CSS Transpiler

```
=> Write (Draft) Spec CSS
=> Task Runner Executes
=> Valid CSS for supported browser's features
```

* Write CSS using CSS
* Use CSS3 wotihout worry
* Even use CSS4
* Modular (Use only what you need)
* Node based (front-end language for front-end transpiling)
* Tons of existing plugins
* Can't find a plugin? Write one in javascript

## PostCSS Ecosystem

* Autoprefixer
* PostCSS-nested
* PostCSS-color-function
* etc.

## One Day...

*Let's Get as Close As We Can To The Real Thing*
