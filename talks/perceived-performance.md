# Perceived Performance

Eli - I make weird stuff on the internet

### Today I'll be shrieking about

* Why focusing on perceived performance is smart
* How humans perceive time
* Techniques to manage passive waiting time

## Why Perceived Performance Matter

Web performance is all about time. Metrics are time-based metrics. Mbps, milliseconds to first ping

Time is funny thing

**Objective time vs Subjective time**

Objective time is easy to measure. We have clocks. We optimize for objective time. Doing this isn't efficient. This results in "just noticable difference".

But no one browses the internet with a stopwatch around.

Time differences of **20%** or less are imperceptible.

**Active phase vs Passive phase**

Humans tend to overestimate passive waits by **36%**.

### What we can do

* Respond to users immediately
* Give users a sense of certainty
* Occupy their attention
* Render minimum visible layout

### Respond to users immediately

#### Takes ~1 second for flow to be disrupted

Let's pack as much loading into that 1 second as possible.

*Mousedown event vs Click event*

Mousdown event give you a **100-150ms** head start! This little change gives users a perceived sense of performance.

Stay `:active`, kids! Animation duration sweet spot if **150-200ms**.

### Give Users Certainty

Uncertain waits feel longer. Progress bar.....rs!

### Don't overdo it

* < 1s? Don't bother.
* ~ 1-3s? Stick to the basics.
* ~ 3-10s? Time to get fancy. Tell them something.

> Animation plays a big role here. It can contribute considerably to certainty.

#### But what about spinners?

Meh.

### Video Games

Injects text between levels because loading assets takes a long time.

### If this feels like cheating, that's because it is.

You dirty cheaters, you.

## Minimum Viable Layout

Rather than hasten passive phase, increase active phrase's share.

* Indentify what your users interact with first.
* Use predictive design to trick users to think that people

### Predictive Design

* Users aren't snowflakes.
* Behavior follows patterns.

If we can predict what users will do, why not preload their next action before they take it?

Doesn't have to be crazy complicated.

#### Example: Multi-step Form

1. Step one, as fields are filled out load the next step.
2. After they have filled out the fields, load the next step.

Surrounding buttons with a "hitbox" that loads content will speed up perceived response.

Predictive design is a very powerful tool. **Use it _wisely_.**

Mitigate risk with data.

Think about how you want to distribute resources. If you can achieve a 30% improvement quickly, **do it!** But if there is going to be unreasonable resources needed to accomplish this, tackle perceived performance first.

Rely on data to make sound desicions.

https://eli.wtf/fun - Link to the slides
