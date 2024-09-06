# Frontend Mentor - FAQ accordion solution

This is a solution to the [FAQ accordion challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-wyfFdeBwBz). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- Hide/Show the answer to a question when the question is clicked
- Navigate the questions and hide/show answers using keyboard navigation alone
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

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
- [React](https://reactjs.org/) - JS library
- [Next.js](https://nextjs.org/) - React framework
- [Styled Components](https://styled-components.com/) - For styles

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

**HTML**
I learned how to create an accordion dropdown type of area! 
  1. create a div for the entire accordion, where all the questions and answers are placed.
  2. create a div for each of the question and answer pairs
  3. use a text element like heading or paragraph, or even a button, and enter the questions. 
    - Give it a class of "question" or something by which you will reference it.
  4. enter the text for the answer in a text element like a <p> or <h3> and give it a class for referencing it in CSS.
  
```html
<div class="accordion-body">
  <div class="accordion">
    <h1>Frequently Asked Questions</h1>
    <hr>

    <div class="container">
      <div class="label">What is HTML</div>
      <div class="content">Hypertext Markup Language (HTML) is a computer language that makes up most web pages and online applications. A hypertext is a text that is used to reference other pieces of text, while a markup language is a series of markings that tells web servers the style and structure of a document. HTML is very simple to learn and use.</div>
    </div>

    <hr>

    <div class="container">
      <div class="label">What is HTML</div>
      <div class="content">Hypertext Markup Language (HTML) is a computer language that makes up most web pages and online applications. A hypertext is a text that is used to reference other pieces of text, while a markup language is a series of markings that tells web servers the style and structure of a document. HTML is very simple to learn and use.</div>
    </div>
  </div>
</div>
```


**CSS**
How to use the ::before and ::after pseudo-element (I used it to add the purple plus and black minus icons to the end of each question in the accordion). 

```css
/* Positions the plus sign 5px from the right. Centers it using the transform property. */
.accordion .label::before {
  content: '+';
  color: black;
  position: absolute;
  top: 50%;
  right: -5px;
  font-size: 30px;
  transform: translateY(-50%);
}

/* Changes from plus sign to negative sign once active */
.accordion .container.active .label::before {
  content: '-';
  font-size: 30px;
}
```


**JS**
How to toggle the active attribute to make the answer show when the question is clicked on!

```js
const accordion = document.getElementsByClassName('container');

for (i=0; i<accordion.length; i++) {
  accordion[i].addEventListener('click', function () {
    this.classList.toggle('active')
  })
}
```
### Continued development
I want to continue focusing on functional CSS transitions and transforms, as well as mastering CSS positioning since I had a difficult time positioning the card in the center and adding space to the bottom of the screen when the questions expanded the answers.

### Useful resources
- [ MDN Web Docs ](https://developer.mozilla.org/en-US/docs/Web/CSS/::before) - This helped me learn how to use the ::before and ::after pseudo-elements. 
- [ Free Code Camp ](https://www.freecodecamp.org/news/build-an-accordion-menu-using-html-css-and-javascript/) - This is an amazing article which helped me understand how accordions work. I'd recommend it to anyone still learning this concept.

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/moonji-spoonji)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
