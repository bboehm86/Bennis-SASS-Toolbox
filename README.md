# Bennis Sass Toolbox
It's a tiny collection of the most used mixins and functions in my projects.

## Installation

**Install using Bower:**
```
$ bower install --save bennis-sass-toolbox
```

## Requirements
In order to work the project should use the *most recent* Sass version. So **Ruby Sass 3.4** or **Libsass 3.2** are good to go.

If using [Gulp](http://gulpjs.com/) or [Grunt](http://gruntjs.com/) remember to use the most recent Sass plugins!

## Mixins
**structure helpers**
- `abs-position()` -- `$top`, `$right`, `$bottom`, `$left`
  Position element to *absolute*
  _____
- `element()` or `e()` -- element name
  Build a *element* class from parent elements name. Even works when parent is `:hover`
  _____
- `modifier()` or `m()` -- modifier name
  Build a *modifier* class from parent elements name
  _____
- `centerer()` -- `$h`, `$v`, `$is3d`
  Center element horizontal and/or vertical by using `position: absolute` and `transform: translate`.
  If element is going to be altered by any action promote it to `transform: translate3d`.
  _____
- `my-size()` -- `$size` (list)
  Set `height` and `width` values and convert `px` to `rem` **if** `$useRem: true` *(default)* is set.


## Functions
**general**
- `color-fit()` -- `$makeMeNew`
  Calculate matching contrasting color values. Predefine custom color matches in `$colorMatches` map.
  eg: `$colorMatches: ( #fff: #000 );`
  **NOTE:** DON'T use quotes (",')! The value won't be recognised as `$color`
_____
- `rem()` -- Number or px value
  Calculate `rem` value based on `$baseFontSize`
