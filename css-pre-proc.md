# Intro to CSS Preprocessors



## Who I am

Developer, more of an artisan than designer

## What's a preprocessor?

A program that

## Why use a preprocessor?

DRY - Don't Repeat Yourself

Reusability

## What preprocessors are out there?

LESS <http://lesscss.org>

* Famous for being the engine behind Bootstrap <http://getbootstrap.com/>

SASS <http://sass-lang.com>

* Engine behind Zurb Foundation <http://foundation.zurb.com/>

* 2 variants, counting SCSS, which is more CSS-like; will use SASS/SCSS
  interchangeably, but SASS is easier to pronounce

Stylus <http://learnboost.github.io/stylus/>

* Engine behind Roots <http://roots.cx/>

## Installation

* If you're on a Mac, there's

## What a preprocessor gives you

Examples are in SASS, because that's what I know best

### More compact expression through nesting

a {
  ...
}

a:link {
  ...
}

a:visited {
  ...
}

a:hover {
  ...
}

a:focus {
}

a:active {
  ...
}

a img {
  ...
}

Equivalent to:

a {
  ...
  &:link {
    ...
  }
  &:visited {
    ...
  }
  &:hover {
    ...
  }
  &:focus {
    ...
  }
  &:active {
    ...
  }
  img {
    ...
  }
}

### Variables

$tardis-blue: #003b6f;

$base-font-size: 15px;

$line-height: 1.2 * $base-font-size;

a {
  &:link {
    color: $tardis-blue;
  }
  &:visited {
    color: desaturate( $tardis-blue, 20% );
  }
  &:hover, &:focus {
    color: lighten( $tardis-blue, 20% );
  }
  &:active {
    color: invert( $tardis-blue );
  }
}

### Mixins

## More reading

### <http://colorschemedesigner.com/> done in SASS

* Color Schemer library for SASS: <https://github.com/Team-Sass/color-schemer>

### Bootstrap Without all the Debt <https://coderwall.com/p/wixovg>
