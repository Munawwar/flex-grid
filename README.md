UNMAINTAINED: I don't recommend anymore, the bootstrap (and this repo's) approach of pre-creating 100s of CSS classes whether it ultimately used or not. Please check out my newer and copact approach https://github.com/Munawwar/flexbox-simplified

# flex-grid

Grid system using CSS3 flexbox (inspired from bootstrap)

grid.less gives a 12-column grid system like Bootstrap. Also allows to reorder elements in mobile site.

NOTE: Bootstrap 4 is going to use CSS3 flexbox. So..this project is soon going to be obsolete and redundant.

### Usage
The CSS is meant to be used along with [flex-helper](https://github.com/Munawwar/flex-helper).

First add flex-helper.css and then grid.less.

### Syntax

Note: The device/viewport naming is like bootstrap (i.e. xs, sm and md). And the viewport cut-off sizes are defined like bootstrap as well (i.e sm is>= 768px and md >= 992px).

Just like bootstrap the CSS priority is "mobile first". i.e. if you apply f-col-xs-12, on an element, then it applies to all device widths unless another higher-width CSS is applied (like f-col-md-6).

CSS classes defined are as follows:
```
f-col-xs-1 to f-col-xs-12     - Makes element a column of size 1 to 12, for all sizes, unless
                                overridden by tablet or desktop column class.

f-col-xs-auto                 - Makes column width auto.

f-order-xs-1 to f-order-xs-12 - Order of element would be explicitly set for mobile size and above.

f-hidden-xs-up                - Makes element hidden on mobile an above.

Corresponding classes for tablets (sm) and desktop (md) are also defined.
```

In addition to the grid classes, the follow classes are modified versions of flex-helper.
i.e. I've added 'f-' prefix (to be same like the above CSS classes) and xs,sm & md suffix like bootstrap.

```
f-vbox-xs          - Stack child items vertically (the "main axis" for child items is now
                     the vertical axis)
f-hbox-xs          - Stack child items horizontally (the "main axis" for child items is now
                     the horizontal axis)
f-flex-xs          - Stretch item along parent's main-axis
f-auto-xs          - Fit item to inner content along parent's main-axis, except when there is
                     no space available (making inner content overflow).

f-main-start-xs    - Stack child items to the main-axis start
f-main-center-xs   - Stack child items to the main-axis center
f-main-end-xs      - Stack child items to the main-axis end

f-cross-start-xs,
f-cross-center-xs,
f-cross-end-xs     - Similar to the 'main' counterparts, except that
                     these decide the stacking of child items along the cross-axis.
f-cross-stretch-xs - Stretch child items along the cross-axis

f-stretch-self-xs  - Stretch item along parent's cross-axis. Overrides any cross-* class behavior
                     on parent.
f-center-self-xs   - Centers item along parent's cross-axis. Overrides any cross-* class behavior
                     on parent.

f-wrap-xs          - Wrap child items to next line on main-axis. hbox wraps by default so no need to
                     add this classes for hbox.
f-nowrap-xs        - Prevent wrapping of items to next line on main-axis.

All of the above are for mobile. Corresponding classes for tablets (sm) and desktop (md) are also defined.
```

### Examples

See [examples.html](https://munawwar.github.io/flex-grid/examples.html).

### RTL support

Setting CSS `direction: rtl;` on body tag should cause all rows to be reversed in order. This is part of the flexbox specification. Nothing special needs to be done. If you have any case where row shouldn't be reversed, then set dir="ltr" on the hbox div.

### BUGS!

One notable bug in IE 10-11, is that using min-height/min-width along with flex box doesn't work as expected.

There are other bugs documented at [flexbox-bugs](https://github.com/philipwalton/flexbugs).
Note: However flex-grid doesn't use all of the flexbox syntax, so some of them are not relevant.

### Credits

Thanks to [Umar](https://github.com/w3debugger) for reviewing and helping.
