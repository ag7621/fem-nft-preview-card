# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![Desktop preview image for QR code component challenge](/images/desktop-preview.png "Desktop preview")
![Mobile preview image for QR code component challenge](/images/mobile-preview.png "Mobile preview")

### Links

- Solution URL: [Solution](https://github.com/ag7621/fem-nft-preview-card)
- Live Site URL: [Live Site](https://ag7621.github.io/fem-nft-preview-card/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

This challenge was a nice bump in scale and difficulty for me to continue learning BEM and perfecting a CSS variables methodology I enjoy using. It allowed me many opportunities to name my html components in a simple, but hopefully understandable way. I also experimented with using utility classes to handle some of the resuable flex items in my code, although I'm unsure if this is ideal or permisible while using BEM.

For my CSS variables I took advice from a previous challenge, as well as additional research, to try and use 2 layers of naming. I started initially with using easier to understand (for me) color names for my variables, followed by a second layer of naming at the component level with my color variables in place. This allowed the best of both worlds I felt in finding my colors easier as well as assigning them at the component level with little confusion. Whether this will become a hassle or a complication in the future is something I eagarly await.

```html
<article class="card">
    <div class="card__img">
        <img src="images/image-equilibrium.jpg" alt="Image of NFT">
        <div class="card__overlay">
            <img src="images/icon-view.svg" alt="">
        </div>
    </div>
    <h2 class="card__title"><a href="#">Equilibrium #3249</a></h2>
    <p class="card__description">Our Equilibrium collection promotes balance and calm.</p>
    <div class="card__info">
        <div class="flex-group">
            <img src="images/icon-ethereum.svg" alt="">
            <span class="card__price">0.041 ETH</span>
        </div>
        <div class="flex-group">
            <img src="images/icon-clock.svg" alt="">
            <span class="card__time">3 days left</span>
        </div>
    </div>
    <div class="flex-group">
        <img class="card__avatar" src="images/image-avatar.png" alt="Avatar image">
        <p class="card__author">Creation of <a href="#">Jules Wyvern</a></p>
    </div>
</article>
```
```css
:root {

  /* Colors */

  --cyan-400: hsl(178, 100%, 50%);
  --cyan-400-a: hsla(178, 100%, 50%, 0.5);
  --soft-blue-100: hsl(215, 51%, 70%);

  --dark-blue-800: hsl(217, 54%, 11%);
  --dark-blue-700: hsl(216, 50%, 16%);
  --dark-blue-600: hsl(215, 32%, 27%);

  --white-100: hsl(0, 0%, 100%);
  --black-900: hsla(0, 0%, 0%, 0.1);

  /* Component */

  --clr-main-bg: var(--dark-blue-800);
  --clr-card-bg: var(--dark-blue-700);
  --clr-accent: var(--dark-blue-600);
  --clr-box-shadow: var(--black-900);

  --clr-text-primary: var(--soft-blue-100);
  --clr-text-accent: var(--cyan-400);
  --clr-text-title: var(--white-100);

  /* Font size */
  --fs-300: 0.9375rem;
  --fs-400: 1rem;
  --fs-500: 1.1rem;
  --fs-600: 1.375rem;

  /* Font weight */

  --fw-light: 300;
  --fw-regular: 400;
  --fw-bold: 600;

}
```

### Continued development

My hopes is to continue to refine my understanding of CSS variables to allow for something versatile, understandable, and easily employable without causing complications further down the road. I enjoyed trying something new and will further experiment with the process.

As for BEM, I hope to continue refining my use of the methodology with more coding practice and feedback. I'm still not 100% confident on my use as I feel with projects scaling in scope will only further complicate its use.

### Useful resources

- [BEM cheat sheet](https://9elements.com/bem-cheat-sheet/) - This helped me understand the basics of how BEM looks and how to name classes.
- [Kevin Powell Youtube](https://www.youtube.com/@KevinPowell) - Amazing channel by veteran web developer Kevin Powell which helped me to understand CSS much better.
- [Josh W Comeau CSS reset](https://www.joshwcomeau.com/css/custom-css-reset/) - A CSS reset referred to in a video by Kevin Powell.

## Author

- Frontend Mentor - [@ag7621](https://www.frontendmentor.io/profile/ag7621)

## Acknowledgments

At times I found myself finding myself overcomplicating my solution with too much fine tuning, resulting in a few odd behaviors. The following individuals solutions gave me inspiration in resolving those issues, and slimming my code down for easier understanding (I hope!).

- [Kevin Powell - Responsive Product Preview Card Component](https://youtu.be/B2WL6KkqhLQ) - Although a walkthrough of a different, but similar Frontend Mentor challenge, his process allowed me to rethink on how to restructure my own code and allow the responsiveness to do most of the heavy lifting. 
- [msienkowiec](https://msienkowiec.github.io/nft-preview-card-component-main/) - Inspiration on how to better handle the active states and links.
- [Olumide2596](https://olumide2596.github.io/nft-preview-card-component-main1/) - Inspiration on active states as well as transitions.
