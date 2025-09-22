# Frontend Mentor - Bento grid solution

This is a solution to the [Bento grid challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/bento-grid-RMydElrlOj). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size

### Screenshot

- On Desktop:

![Screenshot on desktop resolution](./screenshots/desktop.png)

- On Mobile:

![Screenshot on mobile resolution](./screenshots/mobile.png)

### Links

- [Solution Repo (GitHub)](https://github.com/lucarl07/bento-grid)
- [Live Site (GitHub Pages)](https://lucarl07.github.io/bento-grid/)

## My process

### Built with

- **HTML 5** (with semantic markup)
- **CSS 3** (with CSS grid, global variables, @media queries, etc.)

### What I learned

I started this project feeling rather stuck and without knowing how to progress. This feeling was due to my initial insistence on using flexbox display, with led to my HTML file being littered with divs (div hell, *per se*?). After realizing how inefficient this approach would be, and me knowing it would be horrible to determine, one by one, the size of each grid item, I chose to face an old obstacle of mine, CSS Grid.

All I can say is that, for some reason, I had a stigma with CSS Grid and as far as I can remember, some of my implementations just *didn't work at all*. Maybe because I've tried using it for HTML tables, maybe because I was dealing with image grids (let's be real, images are painful to handle) or simply because I thought you needed to put the values for `grid-area` in braces. That being said, it worked way more neatly than I expected and with little interference from other margins or paddings.

```css
.grid {
  display: grid;
  height: 100%;
  padding: 6vh 22vw;
  gap: 2rem;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: 1.2fr .3fr .5fr 1fr;
  grid-template-areas: 
    "cardG cardA cardA cardD"
    "cardG cardB cardC cardD"
    "cardH cardB cardC cardD"
    "cardH cardF cardE cardE";
}

/* ... */

.grid .item:nth-child(2) {
  grid-area: cardB;
  justify-content: space-between;
  background-color: var(--white);
}
```

### Continued development

Since I've barely have any experience with CSS Grid, I guess there is room for improvement in this matter. I still want to play more with properties such as `grid-template-columns` or `grid-template-rows` and its values, especially to make the items of the Bento grid more responsive and pixel-perfect.

### Useful resources

- [How to Use Bento Grids Design in Your Web Projects (David Jaja, freeCodeCamp)](https://www.freecodecamp.org/news/bento-grids-in-web-design/) - An article which dives in depth about the usage of Bento Grid, from the design philosophy to the implementation via CSS Grid (that's what made me choose this approach).
- [W3 Schools's CSS Reference](https://www.w3schools.com/cssref/index.php) - W3 Schools always with their amazing, reliable, easy-to-understand material helped me be more confident while using CSS Grid.

## Author

- GitHub - [Luiz Carlos Jr.](https://github.com/lucarl07)
- Frontend Mentor - [@lucarl07](https://www.frontendmentor.io/profile/lucarl07)
