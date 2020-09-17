# More Css

## Controlling the Position of Elements
CSS has the following *positioning* schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute
positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property.

- **Normal flow -** Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit side-byside, they will not appear next to each other. This is the default
behavior (unless you tell the browser to do something else).
- **Relative Positioning -** This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.
- **Absolute positioning -** This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.

To indicate where a box should be positioned, you may also need to use *box offset* properties to tell the browser how far from the top or bottom and left or right it should be placed. 
    - (You will meet these when we introduce the positioning schemes on the following pages.)

- **Fixed Positioning -** This is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the containing element. Elements with fixed positioning do not affect the position of surrounding elements and they do not move when the user scrolls up or down the page.
- **Floating Elements -** Floating an element allows you to take that element out of normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.

*When you move any element from normal flow, boxes can overlap. The z-index property allows you to control which box appears on top.*

- ```position: static```: the syntax for a normal flow 
- ```position: relative```: moves an element in relation to where it would have been in normal flow.
- ```position:absolute```: the box is taken out of normal flow and no longer affects the position of other elements on the page
    - they act like it's not there
-```position:fixed```:  a type of absolute positioning that requires the position property to have a value of fixed

*The z-index is sometimes referred to as the stacking context (as if the blocks have been stacked on top of each other on a z axis)*

```float```: The float property allows you to take an element in normal flow and place it as far to the left or right of the containing element as possible.

## Clearing Floats
The clear property allows you to say that no element (within the same containing element) should touch the left or righthand sides of a box

- ```life``` - The left-hand side of the box should not touch any other elements appearing in the same containing element.
- ```right``` - The right-hand side of the box will not touch elements appearing in the same containing element.
- ```both``` - Neither the left nor right-hand sides of the box will touch elements appearing in the same containing element.
- ```none``` - Elements can touch either side.

### Parents of Floated Elements: Problem
If a containing element only contains floated elements, some browsers will treat it as if it is zero pixels tall.

### Parents of Floated Elements: Solution
- The ```overflow``` property is given a value ```auto```.
- The ```width``` property is set to ```100%```

**[🠴 RETURN](README.md)**