# Reading Notes
### class 08


## CSS Layouts

- postioning schemes that allow you to control the layout of a page.

- Normal flow is where every block-level element appears on a new line, causeing each item to appear lower down the page. Even if you see width and height and they appear to be ablt to sit next to each other, they will not

- Relative Positioning moves an element from the position it would be in normal flow, being able to shift it up or down. This will not affect the positioning of the other elements around it.

- Absolute positioning will position the element in relation to its containing element. The element will be taken out of normal flow, all other elements will ignore it positioning to fill its space.

- Fixed positioning is a type of absolute positioning that take the element out of normal flow but keeps it in one spot on the screen. If the browser window moves then the element will stay in its position as if it is attached to the screen.

- Floating elements allows yoiui to take that element out of normal flow and positrion it to either the left or right sides of the browser

- When you move an element out of flow it will also need to have a hight z index to be showen about the other elements.

- To have a responsive layout use liquid rules like em and rem that are percentages of the body font size. That way when the media queury changes the font size ... everything else will update.

- Use a CSS framwork to be provided a style starting ground. It provides you with grid layouts, styling forms, and code for other common task.
