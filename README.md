# Frontend Mentor - Sunnyside agency landing page solution

![Design preview for the Pod request access landing page coding challenge](./desktop-preview.jpg)

This is a solution to the [Sunnyside agency landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/sunnyside-agency-landing-page-7yVs3B6ef). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The Challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)

## Overview

### The Challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/sunnyside-agency-landing-page-svelte-css-grid-keyframes-B1UGumXV5](https://www.frontendmentor.io/solutions/sunnyside-agency-landing-page-svelte-css-grid-keyframes-B1UGumXV5)
- Live Site URL: [https://fm-sunnyside-landing-page.vercel.app/](https://fm-sunnyside-landing-page.vercel.app/)

## My process

### Built with

- [Svelte](https://svelte.dev/)
- CSS Grid
- Keyframes animation

### What I learned

I utilized a local variable in conjunction with a svelte variable to determine the color of the "underline" in the `LinksUnderlined` component. Not sure if this is best practice as it feels there should be a simpler way to do this, but it works!

This was my first time using the `svelte:window` property, which I used to bind the innerWidth value to a width variable. This was handy in passing another condition to the Svelte `if` statement that determines whether the menu in the `Nav` component is shown or not.

```html
<svelte:window bind:innerWidth={width}/>
...
 {#if active || width >= 800}
    <ul class="menu" ...
```

### Useful resources

- ["px to rem"](https://marketplace.visualstudio.com/items?itemName=sainoba.px-to-rem) VSCode extension - an absolute time saver.
