# Frontend Mentor - 3-column preview card component solution

This is a solution to the [3-column preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). Frontend Mentor challenges help you improve your coding skills by building realistic projects.  

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

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot
<div>
  <img src="solution_images/solution_375mobile.jpg" width="auto" height="400" src="solution on mobile view"/>
  <img src="solution_images/solution_1440desktop.jpg" width="auto" height="400" src="solution on desktop view"/>
</div>

### Links

- Solution URL: [My solution URL](https://github.com/MiloosN5/FrontendMentor_StatsPreviewCard_Challenge)
- Live Site URL: [My live site URL](https://miloosn5.github.io/FrontendMentor_StatsPreviewCard_Challenge/)


## My process

### Built with

- Semantic HTML5 markup
- SASS - compiled into the CSS
- BEM
- Flexbox
- Grid
- Mobile-first workflow
- REM (Root EM) & EM (for Responsive)
- Responsive layout
- NPM
- JavaScript
- Webpack 

### What I learned

* Creating hover state on the button. In SASS, you can use "&:hover" inside selector of element to which you want to apply effect. In order to have smooth change between regular and hover states, using transition is recommended.<br/>
**Note** In the code snipper below, you can see usage of mixins (@include ...) & placeholders (@extend ...).

  * button - hover 
    ```scss
        .cars {
            &__section {
                &__button {
                    @include a.container('w-auto', 'mw-none', 'h-auto', 'very-light-gray');
                    @include a.padding('pi-button', 'pb-button');
                    @include a.border('b-button', 'br-button');
                    @include a.transition('0.5s', 'ease-in-out');
                    @extend %text-center;
                    @extend %display_inlineBlock;
                    @extend %capitalize;
                    &:hover {
                        @extend %btn-hover-transparent;
                    }
                }
            }
        }
    ```

* To be sure that you have right font format (eg. uppercase or capitalize) you can use placeholders. In that way, you don't need to take care about if letter is capital or not when you write it in the html. Then you extend style that you made in placeholders.

  * extending placeholder style
    ```scss
        .cars {
            &__section {
                &__title {
                    @include a.margin('mi-0', 'mb-title');
                    @extend %uppercase;
                }
            }
        }
    ```
    defining placeholder
    ```scss
        %uppercase {
            text-transform: uppercase;
        }
    ```    

* BEM (Block Element Modifier) is really helpful when creating styles in .scss files. Block represents an object on a website, element is a component within the block and modifier is used for different element behavior (eg. multiple buttons with diffent background color). This naming convention also help in communication between designers and developers.

  * BEM naming convention
    ```html
        <main class="cars">
            <section class="cars__section cars__section--sedans">
                <a class="cars__section__button cars__section__button--sedans">Learn more</a>
            </section>
            <section class="cars__section cars__section--suvs">  
                <a class="cars__section__button cars__section__button--suvs">Learn more</a>               
            </section>
            <section class="cars__section cars__section--luxury">
                <a class="cars__section__button cars__section__button--luxury">Learn more</a>               
            </section>                
        </main>  
    ```


### Continued development

* In-depth explorating of Webpack & Sass.
* Aspiration to make better responsive layout.
* Aspiration to make better SASS organization.

### Useful resources

- [Webpack Course - Colt Steele (Youtube)](https://www.youtube.com/playlist?list=PLblA84xge2_zwxh3XJqy6UVxS60YdusY8) - Webpack configuration - really helpful to understand difference between 'development' & 'production' configuration. Also, comprehensible explanations and straight to the point.
- [Webpack - Official documentation](https://webpack.js.org/) - Webpack official documentation - everytime you struggle with understanding something about webpack (ex. plugins), there you can found explanation. 
- [BEM](https://en.bem.info/) - BEM naming convention is also really important for any projects, expecially the bigger ones.
- [SASS](https://sass-lang.com/documentation/at-rules) - You can found detailed documentation on the official page of the SASS. Check out for example "at-rules".
- [7-1 pattern SASS](https://sass-guidelin.es/#component-structure) - "7-1" pattern is one of the most used sass organization. It is also very pratical. 
- [Clamp calculator](https://royalfig.github.io/fluid-typography-calculator/) - Since there are so many different devices, desirable is to make your font fluid from one size to another.
- [Media Query](https://css-tricks.com/a-complete-guide-to-css-media-queries/) - A Complete Guide to (CSS) Media Queries.
- [Responsive images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images) - How to make images responsive.
- [Typographic Hierarchy](https://www.toptal.com/designers/typography/typographic-hierarchy) - Understanding your website structure/hierarchy sometimes can be difficult. Determing accurately typography can be half job done. 
- [An Introduction to Block Element Modifiers (BEM)](https://opensenselabs.com/blog/articles/introduction-block-element-modifiers) - Difference between Block, Modifier and Element.
- [Understanding CSS BEM](https://codeburst.io/understanding-css-bem-naming-convention-a8cca116d252) - Examples of how BEM class namings can be done.
- [BEM 101](https://css-tricks.com/bem-101/) - Another source about BEM.

## Author

- GitHub - [MiloosN5](https://github.com/MiloosN5)
- Frontend Mentor - [@MiloosN5](https://www.frontendmentor.io/profile/MiloosN5)



