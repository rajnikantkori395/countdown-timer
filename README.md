# Frontend Mentor - Launch countdown timer solution

This is a solution to the [Launch countdown timer challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/launch-countdown-timer-N0XkGfyz-). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

## Overview

### The challenge

Users should be able to:

- See hover states for all interactive elements on the page
- See a live countdown timer that ticks down every second (start the count at 14 days)
- **Bonus**: When a number changes, make the card flip from the middle

### Screenshot

![Desktop Design](./design/desktop-design.jpg)
![Mobile Design](./design/mobile-design.jpg)

### Links

- Solution URL: [Add your Frontend Mentor solution URL here]
- Live Site URL: [Add your live site URL here]

## My process

### Built with

- **Semantic HTML5 markup** - Clean, accessible structure
- **CSS custom properties** - Consistent color theming with HSL values
- **Flexbox** - For responsive layout and centering
- **CSS 3D transforms** - For the flip card animation effect
- **Vanilla JavaScript** - For countdown logic and DOM manipulation
- **Mobile-first responsive design** - Progressive enhancement approach
- **CSS animations and transitions** - Smooth flip animations
- **Background gradients and SVG patterns** - For the space theme

### What I learned

This project was an excellent opportunity to work with advanced CSS animations and JavaScript timing functions. Here are some key learnings:

**CSS 3D Flip Animation Implementation:**

```css
.flip-card {
  transform-style: preserve-3d;
  transition: transform 0.6s ease-in-out;
}

.flip-card.flipping {
  transform: rotateX(180deg);
}

.flip-card-front,
.flip-card-back {
  backface-visibility: hidden;
}

.flip-card-back {
  transform: rotateX(180deg);
}
```

**Smart Change Detection for Animations:**

```javascript
// Store previous values to detect changes
let previousValues = {
  days: "14",
  hours: "00",
  minutes: "00",
  seconds: "00",
};

// Only trigger flip when value actually changes
if (newDays !== previousValues.days) {
  flipCard("days-card", newDays);
  previousValues.days = newDays;
}
```

**Complex Background Styling:**

```css
body {
  background: url("./images/bg-stars.svg"), linear-gradient(to bottom, var(--very-dark-blue), var(--very-dark-mostly-black-blue));
  background-repeat: no-repeat;
  background-size: cover;
}
```

**Responsive Design with CSS Custom Properties:**

```css
:root {
  --grayish-blue: hsl(237, 18%, 59%);
  --soft-red: hsl(345, 95%, 68%);
  --white: hsl(0, 0%, 100%);
  --dark-desaturated-blue: hsl(236, 21%, 26%);
  --very-dark-blue: hsl(235, 16%, 14%);
  --very-dark-mostly-black-blue: hsl(234, 17%, 12%);
}
```

**Interactive Hover Effects:**

```css
.social-icons img:hover,
.social-icons img:focus {
  filter: hue-rotate(325deg) saturate(5458%) brightness(101%) contrast(101%)
    invert(63%) sepia(54%);
}
```

Key achievements:

- **Performance-optimized animations** - Flip animations only trigger when values actually change
- **Realistic countdown logic** - Accurate time calculations with proper date handling
- **Responsive design** - Seamless experience across mobile (375px) to desktop (1440px+)
- **Accessible design** - Proper focus states and semantic HTML structure
- **Visual polish** - Cut circles, shadows, and gradients for realistic card appearance

### Continued development

Areas I'd like to continue focusing on in future projects:

- **Advanced CSS Animations**: Explore staggered animations and more complex keyframe sequences
- **Performance Optimization**: Implement `requestAnimationFrame` for smoother animations and reduce layout thrashing
- **Accessibility Enhancements**: Add ARIA labels and improve screen reader compatibility
- **State Management**: For larger projects, implement proper state management for countdown data
- **Testing**: Add unit tests for countdown logic and visual regression tests
- **Progressive Enhancement**: Ensure the countdown works even without JavaScript enabled

## Useful resources

- [CSS 3D Transforms](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-style) - Essential for understanding the flip card effect
- [CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties) - For maintaining consistent theming
- [JavaScript Date Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) - Critical for accurate countdown calculations
- [CSS Filter Functions](https://developer.mozilla.org/en-US/docs/Web/CSS/filter) - Used for creating hover effects on social icons
- [CSS Grid vs Flexbox](https://css-tricks.com/snippets/css/complete-guide-grid/) - Helped choose the right layout method
- [Red Hat Text Font](https://fonts.google.com/specimen/Red+Hat+Text) - The typography used in the design

## Author

- Website - [Rajnikant Kori](https://portolio-react-ts.vercel.app)
- Frontend Mentor - [@rajnikantkori395](https://www.frontendmentor.io/profile/rajnikantkori395)
- LinkedIn - [Rajnikant Kori](https://www.linkedin.com/in/rajnikant-kori-mca/)

---

This project was completed as part of the Frontend Mentor challenges to improve my frontend development skills. The design and requirements were provided by Frontend Mentor, and the implementation was done from scratch using HTML, CSS, and JavaScript.

**Challenge completed:** Launch countdown timer with flip animations
**Technologies used:** HTML5, CSS3, Vanilla JavaScript
**Design system:** Mobile-first responsive design with CSS custom properties
