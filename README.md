# SASS Basics

## Objectives
- What is SASS? What does it give that out of the box CSS doesn't?
- .sass vs .scss, what are the main differences? 
- How to complie SASS files to plain CSS
- Key SASS functionality & fundamentals
  - Nested Selectors
  - Variables
  - Mixins
  - Extends***
  - Other Functions & functionality
- How to structure SASS files***

## Examples of SCSS and Sass

### [SCSS Section Design](https://codepen.io/janmez/pen/aLdBEJ?editors=0100)
### [SASS CSS Cassette Art](https://codepen.io/janmez/pen/wNKxex)

## Installing Sass Locally & Command Line Compilation

### [Install Sass](https://sass-lang.com/install)
`sass --watch style.css`

## VSCode Plugin for SASS compilation

### [Sass](https://marketplace.visualstudio.com/items?itemName=Syler.sass-indented)
### [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)

## Codepen also for following along
### [CodePen link](https://codepen.io/janmez/pen/ZEQYXxz)

## Nested Selectors
```
/* SASS file */
nav.navigation{
    width: 100%
    ul{
        list-style: none;
        li{
            bakground: #ccc;
        }
    }
}
======
/* Complied CSS file */
nav.navigation{
    width: 100%;
}
nav.navigation ul{
    list-style: none;
}
nav.navigation ul li{
    background: #ccc;
}
```
## Variables
```
$white: #FAF6F6;
$main-color: #FEC3A6;

.section{
    background: $white;
    color: $main-color;
}
```

## Mixins
```
/* SASS file */
@mixin flexbox-base($direction, $align-i, $justify-c){
    display: flex;
    flex-direction: $direction;
    align-content: $align-i;
    justify-content: $justify-c;
}

.selector {
    @include flexbox-base(column, center, center)
}
=====================
/* Compiled CSS file*/
.selector{
    display: flex;
    flex-direction: column;
    align-content: center;
    justify-content: center;
}

```

## Extends
```
/* SASS file */

%light-border{
  border-radius: 6px;
  border: 1px solid #ccc;
}

.selector {
    @extend %light-borders;
}
```

## Other Functions
- `lighten(color, percentage)`
- `darken(color, percentage)`
- `transparentize(color, alpha-amount)`
- `rgba(color, alpha-amount)`


## Resources
- [SASS Documentation](https://sass-lang.com/guide)
- [Medium - SASS Project Structure](https://medium.com/@dannyhuang_75970/sass-project-structure-for-big-projects-8c4a740846ee)