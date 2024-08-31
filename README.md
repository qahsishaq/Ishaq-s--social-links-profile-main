# Frontend Mentor - Social links profile solution

This is a solution to the [Social links profile challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-links-profile-UG32l9m6dQ). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

-[The challenge](#the-challenge)
-[Screenshot](#screenshot)
-[Links](#links)
-[What I learned](#what-i-learned)
-[Continued development](#continued-development)
-[Author](#author)
-[Acknowledgments](#acknowledgements)
## The challenge
My personal social links profile available for everyone to see, by simply **clicking** or **navigating via keyboard**. A challenge on Frontend Mentory.

### Screenshot
![]()

### Links
- Solution URL: [Solution URL here]()
- Live Site URL: [Live site URL here]()

### What I learned

I familiarised myself with the css pseudo-classes and also learnt how to make keys trigger events; This allows anyone that visits the website to navigate the links by using the keyboard also.

```css
.proud-of-this-css{
	opacity: 0.5;
	transition: 0.6s;
	font-size: calc(0.9rem + 0.2vw);
	cursor: pointer;
	color: hsl(75, 94%, 57%); 
	cursor: progress;
}
```

```js
const proudOfThisFunc = (button, index, buttons) => {
        button.addEventListener('keydown', function(event) {
            // Move focus to the next button when the down arrow is pressed
            if (event.key === 'ArrowDown') {
                event.preventDefault(); // Prevent default scrolling
                if (index < buttons.length - 1) {
                    buttons[index + 1].focus();
                } else {
                    buttons[0].focus(); // Loop to the first button
                }
            }
            // Move focus to the previous button when the up arrow is pressed
            if (event.key === 'ArrowUp') {
                event.preventDefault(); // Prevent default scrolling
                if (index > 0) {
                    buttons[index - 1].focus();
                } else {
                    buttons[buttons.length - 1].focus(); // Loop to the last button
                }
            }
            // Handle Enter or Space key for button click action
            if (event.key === 'Enter' || event.key === ' ') {
                // Perform button action here
                alert(`${this.textContent} link clicked!`);
            }
        });
    }
```
### Continued development
Coming soon: integrating Variable fonts into my code.

## Author
- Frontend Mentor - [@qahsishaq](https://www.frontendmentor.io/profile/qahsishaq)

- Twitter -[@qahs_I_I_shaq](https://x.com/qahs_I_I_shaq)

## Acknowledgements

I couldn't have done it easily without the assistance and inspiration from the Frontend mentor community and some AI tools, when I got stuck. 