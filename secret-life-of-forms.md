# Secret Life of Forms

Ivan Wilson - http://innateagency.com

## Multilayered

HTML - Semantic Layer
CSS - Presentation Layer
JavaScript - Behavior Layer

## What's a **form**?

A form is a...

* ~~series of instructions~~
* ~~a process~~
* ~~process that contains a series of instructions~~

No, it's **IKEA**!

-> Multiple steps that provide the right tools for the right job.

For forms, this are inputs. We are dealing with two considerations: 

1. Business requirements - What information do you want to collect?
2. Data collection - How do you want to save the data?

We are inbetween those two considerations in building forms.

## Complexities

##### Zip/Postal Codes

* US: Five digits, starting with "0" for New Enland

##### Dates

* US: mm/dd/yyyy format
* Everyone else: dd/mm/yyyy format

When is it the right time to use this particular input? Should we use a number or a select for dates? Text with alidation limitations?

```<input type="number" />```

> The hardest thing [and the easiest thing to misunderstand] for people who work with HTML is that it's not a *visual* language. It's an **informative** language.

**HTML** is a language and it has **superpowers**

### What about CSS?

There is only so much we can do (regarding forms) to control styling. What the focus should be on is how to enhance the user's experience rather than define (px for px) what it looks like.

Labels are your best friends.

> The number one benefit of information technology is that it empowers people to do what they want to do. It lets people be creative. It lets people be productive. It lets people learn things they didn't think they could learn before, and so in a sense it is all about potential. - Steve Ballmer
