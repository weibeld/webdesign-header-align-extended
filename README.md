# Header Align Extended

An example of laying out typical elements in a website header using the CSS3 **[flexbox](https://www.w3schools.com/css/css3_flexbox.asp)** (flexible box) layout mode.

This is an extension of [Header Align](https://github.com/weibeld/webdesign-header-align).

## Live Demo

[Click here](https://weibeld.github.io/webdesign-header-align-extended/)

## Recorded Demo

![Walkthrough](walkthrough.gif)

## Summary

### Define a "left group" and a "right group"

The most important part is to group the elements which need to be aligned on the left or right side, respectively, of the header, so that these groups are immediate children of the header (`#hd-X-left` and `#hd-X-right`).

Then the header itself is declared a **flex container**, and `#hd-X-left` and `#hd-X-right` are its **flex items**. The flex items can be pushed to the left and right edges of the header by [`justify-content: space-between`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_justify-content&preval=space-between):

~~~css
header {
  display: flex;
  justify-content: space-between;
}
~~~

### Align content in each group separately

Then, the content of the two groups at the left and right edge of the header is laid out using a flexbox layout as well.

Note that the default value for [`justify-content`](https://www.w3schools.com/cssref/css3_pr_justify-content.asp) is [`flex-start`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_justify-content&preval=flex-start), which is always fine for our example, so we don't overwrite the default value.

The default value of [`align-items`](https://www.w3schools.com/cssref/css3_pr_align-items.asp) is [`stretch`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_align-items&preval=stretch), which is fine for some cases, for example, if we want the contained links to stretch to the full height of the header (as in `#hd-2-left`).

In other cases, if we want the contained elements to just "float" in the vertical middle, we set [`align-items: center`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_align-items&preval=center).

## References

- Header Align
    - <https://github.com/weibeld/webdesign-header-align>
- Flexbox
    - <https://www.w3schools.com/css/css3_flexbox.asp>
    - <https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout>
    - <https://css-tricks.com/snippets/css/a-guide-to-flexbox/>
- Approaches to center things
    - <https://www.w3.org/Style/Examples/007/center.en.html>
