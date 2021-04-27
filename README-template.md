# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it. 

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow


### What I learned

1. How to use picture tag to make image tag responsive, below snippet shows how to manage images based on screen size

```html
      <picture class="preview__card__header">
        <source srcset="./images/image-header-desktop.jpg 768w">
        <source srcset="./images/image-header-mobile.jpg 320w">
        <img src="./images/image-header-mobile.jpg" alt="team meeting">
          </picture>    
```


2. Continuation of above,Adding overlay for picture tag, picture tag is inline so it doesnt have its own height and width, changing display to block and using relative positioning with ::after selector to assign overlay background does the tricks.
```css
  .preview__card {
    &__header {
      display: block;
      position: relative;
      img {
        position: relative;
        object-fit: cover;
        width: 100%;
        max-height: 100%;
        display: block;
      }     
      &::after {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: linear-gradient(var(--color-primary-light), var(--color-primary-light));
      }
    }
  }
```



If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.


### Continued development
Understand responsive images in a better way

### Useful resources

- [Overlay Color / Tinted Effec](https://css-tricks.com/tinted-images-multiple-backgrounds/) - This helped with understanding how achieve the tinted effect using css
- [Using picture html5 tag for responsive images](https://www.smashingmagazine.com/2014/05/responsive-images-done-right-guide-picture-srcset/) - Amazing tutorial on how to manage images using html5 tag picture
- [Using object-fit and object-position](https://www.sitepoint.com/using-css-object-fit-object-position-properties/)
-[overlay gradient on image tag]()
- [When to use margin vs padding](https://stackoverflow.com/questions/2189452/when-to-use-margin-vs-padding-in-css)

Leant about text properties
- [text-align](https://css-tricks.com/almanac/properties/t/text-align/)
- [text-justify](https://css-tricks.com/almanac/properties/t/text-justify/)
- [letter-spacing](https://css-tricks.com/almanac/properties/l/letter-spacing/)
- [text-transform](https://www.w3schools.com/cssref/pr_text_text-transform.asp)



## Author

- Website - [Jaymit Desai](https://www.jaymitdesai.com)
- Frontend Mentor - [@jaymitd](https://www.frontendmentor.io/profile/jaymitd)
- Github - [@jaymit123](https://github.com/jaymit123)

