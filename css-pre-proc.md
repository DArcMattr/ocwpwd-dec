# Intro to CSS Preprocessors

XXX Public URL goes here XXX

* * *

## Who I am

More developer than designer; artisan, not artist;

I carry this perspective into my web work

* * *

## What's a preprocessor?

A program that takes a more compact CSS-like file, and turns it into
full-fledged CSS.

* If you already know and work with CSS, you'll be in familiar territory

* Can copy/paste valid CSS into a preprocessor

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

These give you DRY-ness

```SCSS
$tardis-blue: #003b6f;

$base-font-size: 15px;

$line-height: 1.2 * $base-font-size;

html {
  font-size: $base-font-size;
  line-height: $line-height;
  background-color: complement( $tardis-blue );
}

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
```

* * *

This becomes the following CSS...

```CSS
html {
  font-size: 15px;
  line-height: 18px;
  background-color: #6f3400; }

a:link {
  color: #003b6f; }
a:visited {
  color: #0b3a64; }
a:hover, a:focus {
  color: #0071d5; }
a:active {
  color: #ffc490; }
```

* * *

### Mixing, Extending, Including

Reuse of code is a key benefit of going with a preprocessor.

In this example, I'm loading Compass, a popular SASS library of mixins, along
with some of my own pieces:

```SCSS
@import 'normalize';
@import 'sizing';
@import 'compass';

$base-font-size = 1rem;
$lh = 1.2 * $base-font-size;

%clearfix { ... } /* placeholder class */
.branding { ... }

body {
  @include rem( padding, $lh );
  ...
  > header {
    ...
    @extend .branding;
    @include rem( margin, 0 $lh );
  }
  > footer {
    ...
    @extend %clearfix;
  }
}
```

* * *

## "That's fine, I guess, but can I use it without using the command line?"

These utilities were born in the command-line, coder-driven world, but there are
ways to use these without having to venture to the command line.

* CodeKit, for Mac <http://incident57.com/codekit/>

* Prepros, for Mac & Windows <http://alphapixels.com/prepros/>

* * *

These packages streamline front-end development work, however I do not use them.
I can only pass on what their selling points are:

* Automagic processing &amp; browser refreshing For javascript & CSS work

* Also uglifies stylesheets & javascripts for you

* * *

## Try before you install

Various online sandbox sites out there, like

* <http://procssor.com/> ProCSSor

* <http://codepen.io> CodePen

* * *

## More reading & eye candy

### <http://css-tricks.com> CSS-Tricks

Chris Coyier has plenty of articles about preprocessor uses

### <http://sassme.arc90.com/> SassMe

Interactive on-line SASS color playground

### <http://colorschemedesigner.com/> done in SASS

* Color Schemer library for SASS: <https://github.com/Team-Sass/color-schemer>

### Bootstrap Without all the Debt <https://coderwall.com/p/wixovg>

* Using Bootstrap's LESS mixins to keep the benefits, but none of the clutter
from using the classes

### Example CodePen, thebabydino: <http://codepen.io/thebabydino>

## More front-end frameworks, and the preprocessors they use

<http://usablica.github.io/front-end-frameworks/compare.html>

* * *

THEND
