# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [How I did it](#how-i-did-it)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![](./design/desktop-design.jpg)

### Links

- Solution URL: [GitHub repository](https://github.com/AyulaBoyilo/FMfourCardFeature/)
- Live Site URL: [GitHub Pages](https://ayulaboyilo.github.io/FMfourCardFeature/)

## My process

### Built with

- Semantic HTML5 markup
- SCSS
- Flexbox
- Mobile-first workflow

### How I did it

The challenge was really easy. To make the challenge more challenging, so it would be a better exercise for me, I did some essentially unnecessary acrobatics. I played around with pseudo selectors for the card line colors instead of using a simple class solution. Also, after making a required three column layout for the desktop, I took that same 3-column HTML layout and made it a 2-column for the tablets purely through CSS. I know it could be done in a simpler and more efficent way, so a disclaimer: I did it just for the challenge.

```scss
.column:first-child .card {
  border-top: 5px solid $cyan;
}

.column:nth-child(2) {
  .card:first-child {
    border-top: 5px solid $red;
  }

  .card:last-child {
    border-top: 5px solid $orange;
  }
}

.column:last-child .card {
  border-top: 5px solid $blue;
}
```

```scss
.cards {
  position: relative;
  max-width: 710px;
  margin: auto;

  .column {
    .card {
      margin: 0 10px 20px 10px;
    }
  }

  .column:nth-child(2) {
    position: absolute;
    right: 0;
    top: 0;
  }
}
```

## Author

- Ayula Boyilo
