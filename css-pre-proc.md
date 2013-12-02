# Intro to CSS Preprocessors

XXX Public URL goes here XXX

* * *

## Who I am

More developer than designer; artisan, not artist;

I carry this perspective into my web work

* * *

## What's a preprocessor?

A program that takes a more compact CSS-like file, and turns it into
full-fledged CSS

* * *

## Why use a preprocessor?

DRY - Don't Repeat Yourself

Reusability - all preprocessors have ways to tie up common CSS operations into
smaller pieces

* * *

## What preprocessors are out there?

### LESS <http://lesscss.org>

* Famous for being the engine behind Bootstrap <http://getbootstrap.com/>

### SASS <http://sass-lang.com>

* Engine behind Zurb Foundation <http://foundation.zurb.com/>

* 2 variants, counting SCSS, which is more CSS-like; will use SASS/SCSS
  interchangeably, but SASS is easier to pronounce

### Stylus <http://learnboost.github.io/stylus/>

* Engine behind Roots <http://roots.cx/>

* * *

## What a preprocessor gives you

Examples are in SASS, because that's what I know best

### More compact expression through nesting

```CSS
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
```

* * *

Equivalent to:

```SCSS
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
```

* * *

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

* * *

## That's fine, I guess, but how do you use it?

These utilities were born in the command-line, coder-driven world, but there are
ways to use these without having to venture to the command line.

* CodeKit, for Mac <http://incident57.com/codekit/>

* Prepros, for Mac & Windows <http://alphapixels.com/prepros/>

* * *

These packages streamline front-end development work, however I do not use them.
I can only pass on what their selling points are:

* Automagic processing &amp; browser refreshing For javascript & CSS work

* Also "uglifies" stylesheets & javascripts for you

## More reading

### <http://colorschemedesigner.com/> done in SASS

* Color Schemer library for SASS: <https://github.com/Team-Sass/color-schemer>

### Bootstrap Without all the Debt <https://coderwall.com/p/wixovg>
* * *
