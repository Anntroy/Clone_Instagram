# Clone_Instagram

This project is just a mock copy of the login and main page of instagram using SASS.

Theoretical part
The following questions will be answered with my own words to check the understanding of the main SASS concepts:

What is SASS? What does SASS stand for?
SASS short for Syntactically Awesome Stylesheets. It is a preprocessor scripting language that is interpreted or compiled into Cascading Style Sheets

What is a CSS pre-processor?
It is an intermediate process of translation of a language

What does a pre-processor have to do with SASS?
Browser understands CSS but not SASS, so SASS need to be compiled into CSS.

Why use SASS?
The advantages of SASS are: 1) Pre-processor compiles to CSS just the styles you are using, not all. 2) You can use variables, loops, inheritance  and more tools witch makes smaller your code.

SASS has disadvantages? Which are?
The time pre-processor takes to compile code to CSS. Once the code is compiled you can't change values of variables.

What is a SASS Variable? Explain why are useful
Variable is a placeholder, so we can assign the value we need in each moment. We can reuse it multiple times, and save space.

Explain the SASS variables property with an example
You can define only  CSS values using SASS variables.

$font-primary: 'Oswald', sans-serif;
$color-grey: rgb(216, 215, 215);

What is a mixin? Why is it important? Give an example
Mixin is a piece of code which you supose to reuse several times. It saves us from writing more code lines.

What is SCSS? Give an example
It is a new version of SASS. It has it's own extension .scss and it is compatible with CSS.

What is the difference between .scss and .sass syntax.
SCSS use brackets like CSS, while SASS use tabs. SCSS needs to have ; at the end.

In which cases would we use SCSS? And in which cases would we use SASS?
Use of SCSS is more usual while combine with CSS.

Explain how traditional CSS and Preprocessed CSS workflows are different
SASS can override traditional CSS workflow using loops and variables.

Can we create functions with SASS? If it is true, give an example
You can create in SASS mixins

@mixin respond($breackpoint) {
  @if $breackpoint == 'phone' {
    @media only screen and  (max-width: 37.5em){@content}; // 600px
  }
}

What is nesting? Is it useful? Give an example of nesting
Nesting is that you can specify child elements scss rules inside parent rules area.

.footer {
  @extend %flex-column;

  &__nav {
    @extend %flex-row;
    justify-content: center;


    & li {
      list-style-type: none;
      padding: 0.5rem;
    }
  }

  &__language {
    margin-right: 2rem;
    border: none;
    outline: none;
  }
}

Why use @import?
We use it to import one file content to another. Now @import is deprecated, better use @use and @forward.

How can we import other CSS/SASS files in SASS? Give an example
@import '../abstracts/extends';

Explain the concept of inheritance in SASS
We can use @extend to inherit other element rules, so we reduce our code.

Why use @extend? Give an example
We can implement inheritance using @extend:

  &__item4 {
    @extend .post__item3;
    margin-top: 0;

    &-likes{
      margin-bottom: 1rem;
    }

    &-comment{
      @extend .post__item4-likes;
    }
  }
