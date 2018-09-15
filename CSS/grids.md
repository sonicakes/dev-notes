# CSS Grid

3-dimensional layout, as opposed to 2-d flexbox

## Grid template
to replace ```grid-template-rows``` and ```grid-template-columns``` in one line: ```riw-size/column-size```

## fraction

CSS Grid introduced a new relative sizing unit — fr, like fraction.

By using the fr unit, we can define the size of columns and rows as a fraction of the grid's length and width. This unit was specifically created for use in CSS Grid.

It is possible to use fr with other units as well. When this happens, each fr represents a fraction of the available space.
```
.grid {
  display: grid;
  width: 100px;
  grid-template-columns: 1fr 60px 1fr;
}
```

## Repeat
The properties that define the number of rows and columns in a grid can take a function as a value. repeat() is one of these functions. The repeat() function was created specifically for CSS Grid.
```
.grid {
  display: grid;
  width: 300px;
  grid-template-columns: repeat(3, 100px);
}
```
The repeat function will duplicate the specifications for rows or columns a given number of times. In the example above, using the repeat function will make the grid have three columns that are each 100 pixels wide. It is the same as writing:

grid-template-columns: 100px 100px 100px;

## minmax
to set diffferent sizing if browser is resized
```
.grid {
  display: grid;
  grid-template-columns: 100px minmax(100px, 500px) 100px;
}
```
In this example, the first and third columns will always be 100 pixels wide, no matter the size of the grid. The second column, however, will vary in size as the overall grid resizes. The second column will always be between 100 and 500 pixels wide.

## Grid Gap
there is a CSS property grid-gap that can set the row and column gap at the same time. ```grid-gap: 20px 10px;``` will set the distance between rows to 20 pixels and the distance between columns to 10 pixels. Unlike other CSS grid properties, this shorthand does not take a / between values! 

## Multiple Row And Column Lines
Row grid lines and column grid lines start at 1 and end at a value that is 1 greater than the number of rows or columns the grid has. For example, if a grid has 5 rows, the grid row lines range from 1 to 6. If a grid has 8 columns, the grid row lines range from 1 to 9.

Shorthand:
```
.item {
  grid-row: 4 / 6;
}
```

When using these properties, we can use the keyword span to start or end a column or row relative to its other end. Look at how span is used in the code below:
```
.item {
  grid-column: 4 / span 2;
}
```

## Grid Area
We've already been able to use grid-row and grid-column as shorthand for properties like grid-row-start and grid-row-end. We can refactor even more using the property grid-area. This property will set the starting and ending positions for both the rows and columns of an item.
```
.item {
  grid-area: 2 / 3 / 4 / span 5;
}
```
grid-area takes four values separated by slashes. The order is important! This is how grid-area will interpret those values.

grid-row-start
grid-column-start
grid-row-end
