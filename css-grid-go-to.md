CSS grid layout

display: grid - uses the grid layout to position the child items. This style is applied to the parent container

grid: row config / column config - this is grid shorthand. It has 2 parts separated by a forward slash. Anything before the slash is row configuration and anything specified after slash is column configuration

grid-template-columns: repeat(3, 1fr) - this as well is applied to the parent container. repeat() function accepts 2 arguments - number of columns and size of each column. In this example, repeat(3, 1fr) means allow 3 columns. Place each child in one column. If more than 3 children are there then repeat the same layout on next row. 1fr suggests each column to occupy 1 fraction of available space. You can also specify fixed width instead of 1fr

grid-template-columns and grid-template-rows also take values (css units and fr) as to how wide or high the column and row needs to be respectively
For eg grid-template-columns: auto 1fr auto; means column 1 and 3 will be sized automatically and column 2 will be allotted the available space

repeat() function definition from [w3c.org](https://www.w3.org/TR/css-grid-2/#repeat-syntax)
repeat( [ <integer [1,∞]> | auto-fill | auto-fit ] , <track-list> )
`auto-fill` and `auto-fit` cannot be combined with intrinsic or flexible sizes. The size should be explicit, e.g 1rem or 20px or minmax(25ch, 1fr)