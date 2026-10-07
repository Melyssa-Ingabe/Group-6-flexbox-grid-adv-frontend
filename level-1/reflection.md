Level 1 Reflection

For Level 1, I built a header, a main content area, and a footer twice: once in flexbox-style.css and once in grid-style.css. I used identical HTML in both versions, so the only difference was the CSS technique.

Which was easier to implement?
Both were easy for this layout, but Flexbox felt slightly quicker to start because I only had to think in one direction. I set the body to display: flex with flex-direction: column, gave the header and footer a fixed height of 80px, and added flex-grow: 1 to the main section so it filled the leftover space. The Grid version took about the same effort once I understood that one line, grid-template-rows: 80px 1fr 80px, described the whole page.

Which required less code?
The two files were almost the same length, but Grid was a little tidier in two places. First, all three row sizes were defined in one line on the body, so I did not need to set a height on the header and footer or a grow value on main. In Flexbox, the sizing was spread across three rules. Second, centering the text took one line in Grid (place-items: center) compared with two in Flexbox (align-items and justify-content).

Which was more intuitive?
For this simple layout, Flexbox was more intuitive for me because "stack things in a column and let one part grow" matches how I picture a basic page. Grid asked me to plan the rows in advance, which took a little more thought, but it also made the structure easier to read, since I could see the entire page in one line.

Responsiveness
Neither version needed a media query, because the layout stacks vertically at every screen size. I tested both at desktop, tablet, and mobile widths and they looked identical with no overflow.

In what scenarios would I prefer one over the other?
I would use Flexbox for one-dimensional layouts, such as navigation bars, rows of buttons, or centering content inside a component, especially when the content should decide how much space it takes. I would use Grid for page-level layouts with both rows and columns, such as the layouts with sidebars in Levels 2 to 4, because defining the whole structure in one place is clearer than nesting several flex containers. For Level 1 either works, but if I were building a larger page, I would use Grid for the overall skeleton and Flexbox for the pieces inside it.