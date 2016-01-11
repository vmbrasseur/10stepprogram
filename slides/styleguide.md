# Slide Styleguide

Just some things I'm finding myself doing as I work on the slides. Figured I'd write 'em down so we can discuss/rev/standardize.

## Slide organization

This is all based off [the outline](https://github.com/vmbrasseur/10stepprogram/blob/master/outline.md).

* File/directory naming
  * "Ordering" elements (high level point number, slide number) are delimited by `-`
  * "Title" elements are lowercase and replace the space characters with '_`
* "Admin" slides are prefixed `00*-`
  * Introduction, title, etc things which aren't content as such
  * Exercises are always titled `$highlevelpointnumber-100-exercises.md`
* "Content" slides are `0*-` and above
  * Each high-level point (each one of the 10 steps) is a directory
    * Directory names are `$highlevelpointnumber-$point_title.md`
    * These are named with prefixes spaced 10 integers apart, to make it easier in the case we need to add new ones
    * The integer prefixes start at 010 and keep going up as far as they need
  * Each sub-point of a high-level point is a file w/in the appropriate directory
    * Filenames are `$highlevelpointnumber-$slidenumber-$slide_title.md`
    * Once in a while a slide has too many items to include on a single slide. In that case it's refactored into multiple slides.
      * These multiple slides are titled `$highlevelpointnumber-${slidenumber}{[a-z]}-$slide_title.md`

## On a slide

* Slide title
  * H2s (## in markdown)
  * First letter of each word capitalized
* Subtitle
  * H3s (### in markdown)
  * Only first word of the subtitle capitalized

