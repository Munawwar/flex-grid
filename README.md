# flex-grid
Grid system using CSS3 flexbox (inspired from bootstrap)

grid.less gives a 12-column grid system like Bootstrap. Also allows to reorder elements in mobile.

### Usage
The CSS is meant to be used along with [flex-helper](https://github.com/Munawwar/flex-helper).

First add flex-helper.css and then grid.less.

### Syntax

CSS classes defined are as follows:
```
col-mo-1 to col-mo-12 - Makes element a column of size 1 to 12, for all size, unless overridden by tablet or desktop column class.
col-ta-1 to col-ta-12 - Makes element a column of size 1 to 12, for tablet size (>=768px), unless overridden by desktop column class.
col-de-1 to col-de-12 - Makes element a column of size 1 to 12, for desktop szte (>=992px).

order-mo-1 to order-mo-12 - Order of element would be 
```

### BUGS!

One notable bug in IE 10-11, is that using min-height/min-width along with flex box doesn't work as expected.

There are other bugs documented at [flexbox-bugs](https://github.com/philipwalton/flexbugs).
Note: However flex-grid doesn't use all of the flexbox syntax, so some of there are not relevant.
