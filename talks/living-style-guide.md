# Creating a Living Style Guide

## Setup

`kss-node`

* KSS - a Spec for docs
* kss-node - A preprocessore & JS API

### Architecture

* `site` - Generated site for the styleguide
* `src` - Sass, partials, what drives everything, versioned
* `styleguide` - Generated styleguide
* `styleguide-theme` - A Theme for the KSS node styleguide builder
* `styleguide.scss` - Themes for styleguide
* `styles.scss` - The actual Styles
* `homepage.md` - The first page you run into

## What should I document?

* Colors
* Tokens/Variables - e.g. how color variables are *used*
* Mixins/Functions - How to use functions that can be used
* Base Elements/Classes - Images, links, lists, headings, etc
* Patterns - e.g. "Speaker", "Polaroid", "Site Logo"
* Layouts - grids, helper classes
* Vendor Libraries - **What** you're using and why

## Documenting Patterns

* It needs a name
* What does it do?
* Example markup
* Status: "stable", "experimental"
* In the hierarchy, where does this fit?

## Generation and Deployment

* Gulp, Grunt, npm, any of these would work
* Generates a static styleguide. HTML, CSS, and JS. Nothing else

## Tricky Parts

* Colors vs Color tokens. "Colors" are the names and what they look like. "Color tokens" are how the "Colors" are used in a particular context.
* Defining Sections - How to split documentation within the CSS files. In each file vs a "table of contents" headings.scss file from kss.
* Custom Styleguide Theme/Builder - Branding, styles, fonts, for the styleguide itself.

## How do you keep a living styleguide alive?

* NEEDS TO BE A PART OF THE WORKFLOW!
* Cross-browser testing (just HTML/CSS, so fast and simple)
* Visual Regression Testing
* Make it easy to access/update/contribute.
* Version releases (Semantic Versioning)
* CHANGELOG - Keep track of the changes/additions/bugfixes/deprecations.
* Release Promotion - Tell the world about it! Don't just publish it and leave it alone.
