# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

View the optimal layout for the site depending on their device's screen size (mobile and desktop).

### Screenshot

![Screenshot of the testimonials grid section solution](/images/screenshot.png)

### Links

- Solution URL (GitHub): https://github.com/Segarur21/testimonials-grid-section-main
- Live Site URL: https://segarur21.github.io/testimonials-grid-section-main

## My process

### Built with

- Semantic **HTML5 markup** 
- CSS Custom Properties 
- **Flexbox** for internal elements structure and mobile layout
- **CSS Grid** for desktop layout
- **Mobile-first** workflow

### What I learned

During this project, I reinforced my knowledge of **CSS Grid** using `grid-template-areas` to manage responsive design intuitively, as well as positioning decorative background elements effectively.

1. **Clean Semantic Structure:**
   Using `<blockquote>` inside `<article>` elements to maintain proper accessibility and semantics.

2. **CSS Grid Areas:**
   Using explicit grid areas to distribute testimonial cards on desktop layouts:

```css
@media screen and (min-width: 48rem) {
  .testimonials {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-areas:
      "daniel   daniel   jonathan kira"
      "jeanette patrick  patrick  kira";
    gap: 2.4rem;
  }
}
```

3. **Decorative Images with Pseudo-elements:**
   Positioning the giant quotation SVG pattern as a `::before` pseudo-element with a negative `z-index` to keep the HTML markup clean:

```css
.testimonial-1 {
  position: relative;
  z-index: 1;
}

.testimonial-1::before {
  content: "";
  position: absolute;
  top: 0;
  right: 8rem;
  width: 10.4rem;
  height: 10.2rem;
  background-image: url("./images/bg-pattern-quotation.svg");
  background-repeat: no-repeat;
  background-size: contain;
  z-index: -1;
}
```

### Continued development

In future projects, I want to keep refining:
- Code organization and refactoring.
- Learning more advanced CSS Grid techniques.


### AI Collaboration

I leveraged AI assistance during this project for:
- **Code Refactoring:** Optimizing CSS rules to avoid duplication.
- **Debugging:** Resolving stacking context (`z-index`) issues with the decorative SVG pattern.


## Author

- Frontend Mentor - [@Segarur21](https://www.frontendmentor.io/profile/Segarur21)
- GitHub - [@Segarur21](https://github.com/Segarur21)