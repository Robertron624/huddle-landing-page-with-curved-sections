# Frontend Mentor - Huddle landing page with curved sections solution

This is a solution to the [Huddle landing page with curved sections challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/huddle-landing-page-with-curved-sections-5ca5ecd01e82137ec91a50f2). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot
![image](https://user-images.githubusercontent.com/72587880/231843903-50d51380-b282-42a9-b249-8b05f7cf4b25.png)

### Links

- Solution URL: [Solution URL](https://github.com/Robertron624/huddle-landing-page-with-curved-sections)
- Live Site URL: [Live site URL](https://resonant-kitten-e6d94d.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

With this project I learned how to use SVGs and how to scale them to fit the design to add the features section some waves to top and bottom of the content. Also I learn about how SVGs behave(they aren't normal images) for changing its width,height and colors.

Here it's the HTML for the features section:
```html
      <div class="feature-card">
        <div class="top-wave"></div>
        <div class="inner-card">
          <img src="./images/illustration-grow-together.svg" alt="grow together illustration">
          <div class="card-text">
            <h2>Grow Together</h2>
            <p>Generate meaningful discussions with your audience and build a strong, loyal community. 
              Think of the insightful conversations you miss out on with a feedback form.</p>
          </div>
        </div>
        <div class="bottom-wave"></div>
      </div>
```

Here it's the little javascript I used to validate the newsletter form:
```js
    const newsletterInput = document.querySelector('.newsletter form input');

    const errorMessage = document.querySelector('.newsletter form span');

    const newsletterForm = document.querySelector('.newsletter form');

    const emailRegex = /^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/;

    newsletterForm.addEventListener('submit', handleNewsletter)

    function handleNewsletter (e) {
      e.preventDefault();

      // check if email is valid and if it's empty
      if(!emailRegex.test(newsletterInput.value)) {
        errorMessage.classList.remove('inactive');
        newsletterInput.classList.add('input-error');
        return
      }

      errorMessage.classList.add('inactive');
      newsletterInput.classList.remove('input-error');
      console.log("forn submitted!!")
    }
```
### Continued development

I want to keep learning new CSS patterns and work with SVGs more, I think they are a great way to add some style to a website, also I want to work with new figures to separate sections and add some style to the website.

### Useful resources

- [CSS Wave Background | VERY SIMPLE TUTORIAL | HOW-TO](https://www.youtube.com/watch?v=HwnlC_40OzQ) - This video helped me add the shapes to the features cards in a simple way. I'd recommend it to anyone still learning this concept.
- [How to Scale SVG](https://css-tricks.com/scale-svg/) - This is an amazing article which helped me finally understand how to scale and position a SVG, it doesn't behave like a normal .jpg or .png image. I'd recommend it to anyone still learning this concept.

## Author

- Personal Website - [Robert Ramirez](https://robert-ramirez.netlify.app)
- Frontend Mentor User- [@Robertron624](https://www.frontendmentor.io/profile/Robertron624)
- Twitter - [@robertdowny](https://www.twitter.com/robertdowny)

