# Pattern Libraries Can Change Your Life

Adam Mccombs -- Twitter: @adammccombs

## What is a pattern library?

> Recurring solutions that solve common design problems - Paul Boag

Other names for pattern libraries:

* Atom Design
* Material Deisign
* Design Languages
* etc.

Helps to develop more quickly and put that information in front of clients.

## What pattern libraries are not

#### Your Framework

Bootstrap, Foundation, Blueprint, etc

#### Static Mockups

PDFs, photoshop docs or [print] style guides. Should not be limited to designers or front-end developers. Everyone should have access to these libraries and should be able to suggest changes

> Technically a pattern library is a simple collection of UI components, but in order for design system users do their best work, a pattern library should also present other important info. - Brad Frost

## Why are pattern libraries necessary?

#### Brief History

* Tables
* Image Maps
* Inline styles

**"Waterfall" process:** *Discovery -> IA/UX -> Graphic Design -> Template Development -> CMS -> Launch*

Throws things over "walls" from one process to the next or back. Let's "bring down that wall!".

#### What about devices?

The web and screens are everywhere and it's a very different world from fixed width styles. Screens are every shape and size you can conceive.

#### Enter the ~~responsive~~ web

> You put water int oa cup it becomes the cup. You put water into a bottle it becomes the bottle. You put it in a teapot, it becomes the teapot. - Bruce Lee

## Why are pattern libraries appearing?

#### Consistency

Colors. They are re-declared everywhere. The Facebook CSS is declared over 200 times across 700 files.

Pattern libraries give us an opportunity to stop the chaos we create for ourselves.

**Clearleft's** [style guide](http://clearleft.com/styleguide/) is an excellent example.

Github's Button documentation is a good example of a documented pattern library. (They even include the `roll="button"` accessibility tag.) In addition, they provide variations on the button with another simple class.

[Google Material's](https://material.google.com/) Dialog pattern library is an excellent example of a pattern library and also how **not** use the patterns.

## Static Waterfull Process

* User Experience - 2.5 hrs/per apge
* Designer - 2.5 hrs/per page
* Front-end Dev - 2.5 hrs/per page
* Back-end Dev - 2.5 hrs/per page

For 5 pages, that's over 5 hours

If these same people used a pattern library, the hour count comes down because the UX, Designer, and Front-end dev hours can be compressed because the work is done once instead of 3 times.

## Pattern Libraries allow you to develop patterns, not pages

[Atomic Design](http://bradfrost.com/blog/post/atomic-web-design/)

> We’re not designing pages, we’re designing systems of components.—Stephen Hay

* **Atoms**
* *..leads to* **Molecules**
* *..leads to* **Organisms**
* *..leads to* **Templates**
* *..leads to* **Pages**

## Why pattern libraries are awesome

#### Build and develop faster

* Automate deployments of updated patterns
* Use tools like Gulp to minify, add browser autoprefixes and polyfills
* Preview patterns using GitHub pages (for free*)
* Allow for buy in by allowing access to everyone to the pattern library
* Integrate tools like *intercom*, and help desks
* Use your pattern library for visual testing (http://github.com/webdriverio/webdrivercss)

## Prototype

Use codepen.io to play around with the patterns and make adjustments.
Accordions, grids, menus, grids, etc for building/updating these libraries.

## The Structure

#### Style
Color. Typograph. Images

#### Layout
Grids, uits & measurements, sturcture

#### Components
Buttons, tables, navigation, lists

#### Patterns
Advanced navigation, filtering, modules, etc

## Interacting with Projects

* **External** - Patterns are externalized but pushes into your project as library.css
* **Internal** _ Patterns are specific to an individual project
* **Isolated** - Patterns can be updated but have no [automatic] effect on the project(s)

> Pattern libraries (and really CSS in general) is one of those things that everyone has an opinion on how to implement because of its low barrier to entry. This can (and likely will) cause strong opinions to form among various members of your team. I've never worked on a team which agreed on everything in terms of a pattern library (which is a good thing—and I hope you're never on one either). - Una Kravets

## Documentation

Example of what a documented pattern library would include

* **1A - Pattern Name**
* **1B - Pattern usage description**
* **1C - Pattern Why?**
* **1D - Patttern How not to use**

#### Pattern Preview

Definitely display an example of the pattern as an example of how it should be used.

#### Markup

Bonus points for copy & paste!

## Maintaining

### Automate. Automate. Automate.

This is how you are going to maintain a pattern library after it has been launched.

> Unless it's a part of your build, you style guide is just more documenation to maintain - Phil ????

### Design system Maturity Model

1. *Inconsistent* - The absense of a design system
2. *Static* - A static PDF of your brand guildelines
3. *Manual* - The pattern library has code snippets
4. *Automatic* - The pattern library is a part of your app build process
5. *Governed* - The pattern library process is built in to your organization

### Working on a team?

* **Standards** - code standards, naming conventions, file organization
* **Tools** - other systems/libraries, gulp, grunt, Github pages
* **Goals** - what are your objectives pattern library timelines post launch maintenance

[3 Years of Pattern Libraries: Lessons Learned](https://una.im/pattern-libs/#💁) - Una Kravets

https://styleguides.io
