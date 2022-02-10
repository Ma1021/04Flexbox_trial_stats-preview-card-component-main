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

This one I would like to emphasis the difference between desktop version and mobile version, so I will put both of them up.

Desktop version
![](./04destop_view.png)

Mobile version
![](./04mobile_view.png)


### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

1. Different image for different screen size

I first thought of using display none then show --> but this will load both of the image

Solution provided by changing background image of the div --> no need to load both of the images (cannot print out)
https://stackoverflow.com/questions/30460681/changing-image-src-depending-on-screen-size
May be I will use this one (I am not too familiar with this one)

2. Add filter to the image

First I thought of  filter, but it is using customized filter instead of adding the color filter on my own.
https://developer.mozilla.org/en-US/docs/Web/CSS/filter

Then I use the two layer method, adding opacity to the photo --> but the color is so different??
https://stackoverflow.com/questions/9182978/semi-transparent-color-layer-over-background-image

Put the image in the parent div background image and use the background colour with opacity in the child div.

**How to get the correct colors?**

3. Flex-shrink

https://developer.mozilla.org/en-US/docs/Web/CSS/flex-shrink

https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Controlling_Ratios_of_Flex_Items_Along_the_Main_Ax

4. Extra length in viewport height and width

It is defaulted margin assigned to body by Firefox --> but my normalize file should have set it to zero. Simply solved by setting the margin to zero

5. Mystical left space for list

Another default margin! 

https://stackoverflow.com/questions/9111204/align-list-item-to-the-left-in-unordered-list 


6. Putting footer in the right place 

https://stackoverflow.com/questions/32551291/in-css-flexbox-why-are-there-no-justify-items-and-justify-self-properties/33856609#33856609

https://stackoverflow.com/questions/40890613/remove-space-gaps-between-multiple-lines-of-flex-items-when-they-wrap

before is the first child of selected element
https://developer.mozilla.org/en-US/docs/Web/CSS/::before

7. Centralize the background image

Css property of background-position
https://stackoverflow.com/questions/2643305/centering-a-background-image-using-css

8. Mobile device size, flex will not expand the container

I just re-adjust the height of container, are there better ways to do it?
The content will be hidden if the height is too small (with the overflow: hidden effect for the round corner).

9. Is it better to do it with flex-shrink/flex-grow??????

could they work out without width of child container? --> yes, with the width of the parent instead.

Flex-shrink: 1 to fit everything inside the container (the child div will shrink to fit in, if shrink is larger than 1, it will shrink accroding to the ratio to fit), while flex grow is how much the child will grow according to ratio, default as 0.
They use **flex-basis** to state the flex-item width (similar effect as width) instead: https://www.geeksforgeeks.org/what-are-the-differences-between-flex-basis-and-width-in-flexbox/

But there are little difference between them:
Most important one is that when the flex-direction changes, the flex-basis will have effects on the height instead of the width
https://www.freecodecamp.org/news/flexboxs-flex-basis-explained-83d1a01413b7/


### Continued development

Try new things - flexbox. Continue this with the next task. 

## Author

- Frontend Mentor - [@Ma1021](https://www.frontendmentor.io/profile/Ma0121)
