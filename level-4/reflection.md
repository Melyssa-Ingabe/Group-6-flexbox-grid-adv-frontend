Level 4 Reflection: Flexbox vs. Grid
Holy Grail layout with a fixed header, collapsible sidebars, card reflow and four breakpoints
Overview
For Level 4 we built the same Holy Grail page twice: once with Flexbox (flexbox-style.css) and once with CSS Grid (grid-style.css). Both versions share one HTML structure and one small script that toggles a class to collapse the sidebars. Building both side by side showed us where each system is strong and where it needs extra work.
Which was easier to implement?
Grid was easier for the page structure. We declared three columns once, and the header, navigation, content and footer all lined up with them. Subgrid let the footer's three sections sit directly under the left sidebar, main content and right sidebar without repeating any measurements. Flexbox needed a separate flex container for each row, and we had to keep their widths consistent by hand using shared variables.
Flexbox was easier for the smaller pieces. Pushing the user menu to the right of the header with margin-left: auto, and spacing the navigation links with gap and flex-wrap, took one or two lines each.
Which required less code?
The two files ended up close in length, but Grid needed less code for the responsive behaviour. The card area reflows with a single repeat(auto-fit, minmax(...)) declaration and no media query. At the tablet breakpoint, Grid only needed a new grid-template-areas value, while Flexbox needed flex-wrap plus order and flex-basis changes on three elements.
Which was more intuitive?
Flexbox felt more intuitive at first, because it works along one line and is easy to picture. Grid took longer to learn, but once we understood named areas the layout was easier to read. Looking at grid-template-areas: "left main right" tells you what the page looks like. Reading the Flexbox version meant tracing flex shorthand values across several rules.
Collapsing the sidebars worked well in both. Changing one custom property was enough, and the sidebar width animated in either system.
When would we prefer one over the other?
We would choose Grid for the overall page layout, where rows and columns need to line up, and for card galleries that should reflow without media queries. We would choose Flexbox for components that flow in one direction, such as navigation bars, toolbars, button groups and header contents, where the content decides the size.
One limitation we found with Grid is that a position: fixed header cannot be a grid item, so we had to repeat the column variables on it.
Conclusion
The two systems work best together. Grid gave us the page skeleton, and Flexbox would be the natural choice for the components inside it. Building the same layout twice showed us that the better choice depends on whether the layout is one-dimensional or two-dimensional.
