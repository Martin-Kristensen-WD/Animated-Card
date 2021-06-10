# Animated Card 

Live view: https://martin-kristensen-wd.github.io/Animated-Card/

## Table of contents

  - [Screenshot](#screenshot)
  - [Links](#links)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)


### Screenshot

![](./images/Screenshot1.png)
![](./images/Screenshot2.png)


### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)


### Built with

- HTML
- CSS 


### What I learned

# Learned about CSS Custom Properties. 

I have learned how to create custom properties in CSS and use them in the selectors. 

Code Example: 

:root {
  --clr-neutral-900: hsl(207, 19%, 9%); 
  --clr-neutral-100: hsl(0, 0%, 100%); 
}


# Learned about local variables and calc(). 

I have learned how to created local variables and use the calc() function.

Code Example:

.card-content {
  --padding: 1.5rem; 
  padding: var(--padding);
  background: linear-gradient(
    hsl(0 0% 0% / 0), 
    hsl(0 0% 0% / 1)
  ); 
}

.card-title::after {
  content: "";
  position: absolute;
  height: 3px; 
  background: rgb(66, 245, 132);
  left: calc(var(--padding) * -1); 
  width: calc(100% + var(--padding));
  bottom: 0; 
}


# Learned about operators: * & :not()

I have learned how to use the * operator to select ALL and the :not() function to not select a selector

Code Example: 

.card-content > *:not(.card-title) {
  opacity: 0;
  transition: opacity 500ms linear;
}


# Learned about prefered-reduced-motion 

I have learned how to use the prefered-reduced-motion if a users have turned off animation on their machine. 

Code Example:

@media (prefers-reduced-motion: reduce) {
  *,
  *::before, 
  *::after{
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
    transition-delay: 0ms !important;
  }
}


### Useful resources

- [Custom CSS properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [Calc Function](https://developer.mozilla.org/en-US/docs/Web/CSS/calc())
- [Not Function](https://developer.mozilla.org/en-US/docs/Web/CSS/:not)
- [Prefers-reduced-motion](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion)
