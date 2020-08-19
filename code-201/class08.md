# Read08
### Building Blocks
CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.
- Block-level elements :start on a new line.
- Inline elements : flow in between surrounding text.

- Containing Elements:
If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.

### positioning schemes
- Normal flow
position:static
Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit side-byside, they will not appear next to each other. This is the default behavior (unless you tell the browser to do something else) .

- Relative Positioning
position:relative
This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.

- Absolute positioning
position:absolute
This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.

- Fixed Positioning 
position:fixed
This is a form of absolute positioning that positions the element in relation to the
browser window, as opposed to the containing element. Elements with fixed positioning do not affect the position of surrounding elements and they do not move when the user scrolls up or down the page.

- Floating Elements
Floating an element allows you to take that element out of normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.