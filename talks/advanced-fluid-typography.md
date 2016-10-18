# Advanced Fluid Typography

Mike Riethmuller

### An alternative approach to responsive design

Put @media queries and advanced CSS techniques aside. Try to think differently.

**Relative units are just an abstraction of pixels!!!**

If the base font size is 16px...

|CSS value|What does it mean?|Actual value|
|---|---|---|
|1.25rem| 1.25 x Base font size|20px|
|1.5em| 1.5x current font size|24px|
|125%| 1.25 x current font size|25px|

We keep a tally in our heads like the above table.

Relative units like percentages don't change. It's still linear.

**Limitations shape our thinking**

*Perceived limitations* can also shape our thinking

Break the paradigm of pixels!

But first, let's learn more about...

### Unit types & values

:(

How many unit types are there in CSS? 27. How many do we typically use? 3-4.

THERE IS SO MUCH POTENTIAL THERE!

How can a browser understand this?

```css
2px 2px rgba(80%, 80%, 80%, .25);
```

```
.example {
  font-size: 24px;
  width: 80%;
  text-align: left;
}

```

#### Computed value

> The computed value resolves the specified value as far as possible without layout out the document or performing other expensive or hard-to-parallelize operations, such as resolving network requests or retrieving values...

#### Used value

This is the value that is used when actually rendering the page.

* Spcified value - What we've written
* Computed value - Computed value as much as possible
* Used value - Final value used

## Understanding `calc()`

You can add or subtract units with a similar type.

```css
font-size: calc(10px + 2rem);
```

You can multiple & divide CSS units by real numbers (but not by relative units)

```css
font-size: calc(3 * 2rem);
```

|Expression|Is that valid?|
|---|---|
|`calc(10px + 1rem)`|yes|
|`calc(2rem * 3)`|yes|
|`calc(2rem / 5)`|yes|
|`calc(10px - 3)`|no|
|`calc(2rem * 3rem)`|no|
|`calc(2rem / yellow)`|no|

## Responsive Typography

Existing responsive typography techniques are not ideal.

**Viewport units are different**. They are easy to understand

* `vh`
* `vw`
* `vmin`
* `vmax`

Just using viewport units have limitations. On really small sizes, it's almost illegible.

#### Min font-size

```css
html {
  font-size: calc(18px);
}

@media (min-width: 600px) {
  html {
    font-size: 3vw;
  }
}

@media (min-width: 800px) {
  html {
    font-size: 24px;
  }
}
```

## Advanced Fluid Typography

```css
/* 16px min font size */
/* 24px max font size */
/* 800 max screen width */
/* 400 min screen width */
font-size: calc(16px + (24-16) * (100vw - 400px) / (800 - 400));
```

## Fluid Module Scales

Typography and headings are often examples of a module scale.

Calculating a module scale is easy. Go to http://type-scale.com and put the selected values into a table.

Plug them into a mixin.

## It's not just typography!

Since we have `calc()` and relative units can be applied to any properties, you can use fluid types to adjust the styles.

## The future of fluid typography

* Search for "Live font interpolation on the web".
* Maybe a `map()` function for creating these bouding scales?

http://madebymike.com.au/writing/fluid-type-calc-examples
