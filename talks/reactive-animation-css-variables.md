# Reactive Animations with CSS

David Khourshid

## Notation

Having a declarative way of writing music, it allows you to write and play more and more expressive and complex pieces. In many ways, this same principle could be applied to animations.

Sound is continuous
Motion is also continuous

Music notation is discrete.
Motion is harder to express in discrete terms.

Describing complex things in discrete, declarative terms makes it much easier to reason about *what* it is doing, not *how*?

## Immutable vs Mutable



## Functional Programming Constraints

Having constraints makes things less powerful, but in the same way we become **more powerful** within our contrained paradigm.

What if? ... I saw cool animations on the internet and did it only in CSS?

> CSS is not powerful. But that is a good thing.

## The Rule of Least Power

**Principle**: Powerful languages inhibit information reuse.

**Good Practice**: Use the least powerful language suitable for expressing information, constraints or programs on the WWW.

# CSS IS AWESOME

## What are Reactive Animations?

**NOT REACT**

Reactive animations are animations that happen when you do something. They can come from any input. From anywhere. And these inputs cause discrete actions in the form of animations.

JS will connect to the stream of events and sends values over to CSS in the form of properties (CSS variables).

## CSS Variables

```
:root {
  --my-color: white;
}

button {
  background-color: var(--my-color), blue);
}

button.special {
  --my-color: red;
}

<!-- WILL BE RED -->
<button class="special">MY BUTTON</button>
```

## Javascript Events

```
const docStyle = document.documentElement.style;
const someElement = document.querySelector(...)
document.addEventListener('mousemove', (e) => {
  someElement.style.transform = `
    translateX(${e.clientX}px)
    translateY(${e.clientY}px)
  `;
})
```

* It just works
* Detached element?
* CSS overrides (media queries)?
* Overwritten properties

How about this?

```
const docStyle = document.documentElement.style;

document.addEventLIstener('mousemove', (e) => {
  docStyle.setProperty('--mouse-x', e.clientX);
  docStyle.setProperty('--mouse-y', e.clientY);
})

.ball {
  transform:
    translateX(calc(var(--mouse-x) * 1px))
    translateY(calc(var(--mouse-y) * 1px));
}
```

Better, but still very imperative.

What if... we had a way to connect various streams to end up in CSS properties?

## JS Observables

Arrays - A collection of things.
Streams - A collection that gives you each of it's items over time.

Observables are like *arrays* that are *async*, *immutable*, and *subscribable*.

Animations are data over time, so it's a stream.

[RxJS](https://github.com/Reactive-Extensions/RxJS)

```
Rx.Observable
  .from([1,2,3,4,5])

Rs.Observable
  .FromEvent(document, 'mousemove');

const ball = document.querySelector("#ball");
conxt hBall = new Hammer(ball)

Rx.Observable
  .fromEventPattern((handler) =>
    hBall.on("pan", handler))
```

#### Operators

Observable Operators

```
.filter(ball => ball.color === 'green')
```

```
.map(ball => makeSquare(ball))
```

```
.throttle(1000);
```

```
.scan((a, b) => a + b, 0)
```

Think of RxJS as Lodash for Observables

**What if we could model observalbe events as CSS variables?**

> A "reactive animation" is one involving **discrete changes**, due to **events**.
>
> By allowing programmers to express the "what" of an interactive animatin, one can hope to then automate the "how" of its presentation.
>
> \- Conal Elliot and paul Hudak, 1997

Rx.Subject => A producer, essentially an **observable** and an **observer**. Can receive observable events and also send data on to other observers.

## Why animate with CSS Variables?

* Easily debuggable
* No excessive DOM manipulation
* DOM node independent
* Full power of CSS
* Theming & media queries
* **calc()** is your new best friend
* They work in SVG!

## What if?

* Constraint Layouts
* Shared element transitions
* Physics modeling
* Complex animations
* Choreography
* Configurability
* Canvas, WebGL
* Much, much more!
