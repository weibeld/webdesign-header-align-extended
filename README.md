# Header Align 

A simple example of aligning items in a website header by using the CSS3 **[flexbox](https://www.w3schools.com/css/css3_flexbox.asp)** (flexible box) layout mode.

## Live Demo

[Click here](https://weibeld.github.io/webdesign-header-align/)

## Recorded Demo

![Walkthrough](walkthrough.gif)

## Flexbox Concepts

The flexbox layout in CSS3 consists of **flex containers** and **flex items**.

A **flex container** is any element that has `display: flex;` set (or `display: inline-flex;`, in which case it becomes an inline element).

A **flex item** is any element that is an immediate child of a flex container.

The **layout of flex items within a flex container** is determined by certain properties that are set for the flex container.

The most important of these properties are:

- [`justify-content`](https://www.w3schools.com/cssref/css3_pr_justify-content.asp): **horizontal alignment** of flex items within the flex container; the possible values are:
    - [`flex-start`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_justify-content&preval=flex-start) *(default value)*
    - [`flex-end`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_justify-content&preval=flex-end)
    - [`center`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_justify-content&preval=center)
    - [`space-between`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_justify-content&preval=space-between)
    - [`space-around`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_justify-content&preval=space-around)
- [`align-items`](https://www.w3schools.com/cssref/css3_pr_align-items.asp): **vertical alignment** of flex items within the flex container; the possible values are:
    - [`stretch`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_align-items&preval=stretch) *(default value)*
    - [`center`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_align-items&preval=center)
    - [`flex-start`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_align-items&preval=flex-start)
    - [`flex-end`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_align-items&preval=flex-end)
    - [`baseline`](https://www.w3schools.com/cssref/playit.asp?filename=playcss_align-items&preval=baseline)


### Scope

The properties set in a flex container affect only the **immediate children** of this flex container (that is, the flex items). Any **content inside the flex items is unaffected** by the flex container and laid out as usual.

### Compatibility

Inside a flex container, a property like `float` has no effect. Thus, if some element is set to `display: flex`, then don't try to apply e.g. `float: right` to its children, as it will not work.

The same applies for properties like `text-align` or `vertical-align` applied to a `display: flex` element: they have no effect. Use `justify-content` and `align-items`.


## Summary

### Align the divs within the header

We first declare the header element to be a flex container:

~~~css
header {
  display: flex;
}
~~~

This applies the following default values:

- `justify-content: flex-start`: that's why all the three divs are aligned to the left of the header
- `align-items: stretch`: that's why all the three divs occupy the full height of the header

The effect of `align-items: stretch` is already what we want. So, we just overwrite the `justify-content` property:

~~~css
header {
  display: flex;
  justify-content: space-between;
}
~~~

This causes the divs to be horizontally pushed as far apart from each other as possible, thus, one at the left edge, one at the right edge, and one in the center.

That's all for the layout of the divs within the header. Now we want to customise the layout of the text within the divs.

### Align the text within the divs

We want the text to be horizontally and vertically centered within the divs. For this, we first declare the divs to be flex containers as well:

~~~css
header div {
  display: flex;
}
~~~

This again applies the default values `justify-content: flex-start` (causing the text to be left-aligned within the div), and `align-items: stretch` (causing the height of the text area to occupy the full height of the div, but the text itself is still aligned to the top).

To horizontally and vertically center the text within the divs, we overwrite the `justify-content` and `align-items` properties:

~~~css
header div {
  display: flex;
  justify-content: center;
  align-items: center;
}
~~~

And that's it.

## References

- Flexbox
    - <https://www.w3schools.com/css/css3_flexbox.asp>
    - <https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout>
    - <https://css-tricks.com/snippets/css/a-guide-to-flexbox/>
- Approaches to center things
    - <https://www.w3.org/Style/Examples/007/center.en.html>
