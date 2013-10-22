css-slider
==========

This is a CSS Slider that I designed as a specificity exercise.

It uses CSS3's ability to make non-adjacent sibling selections to display different navigation arrows and change the style of the "indicator" labels.

I also make use of SCSS for the ease of creating the logic loops.

With SCSS you can create logical loops using OOCSS principles:

```
@for $i from 1 through 10 {
  #slide#{$i}:checked ~ .frame .slides {
    margin-left:(-#{($i - 1)*100%});
    -webkit-transition:all ease .7s;
    -moz-transition:all ease .7s;
    -o-transition:all ease .7s;
  }
}
```

Here is an example of the logic I used to display the <label> that leads you to the next slide.

```
//
@for $i from 1 through 10 {
  #slide#{$i}:checked ~ .controls label[for="slide#{$i + 1}"] {
    display:block;
    float:right;
    ...
  }
```

