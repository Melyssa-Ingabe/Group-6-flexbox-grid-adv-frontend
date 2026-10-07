# Level 2 Reflection 

For Level 2, I built a webpage with a header, nav bar, main content, sidebar, and footer. On big screens the main content takes up about 70% and the sidebar about 30%. On smaller screens they stack so it's easier to read.

With Flexbox, I used display: flex to put the main content and sidebar side by side. I used flex-basis for the 70/30 split and flex-wrap so they can drop to the next line when there's no room. For mobile, I made both 100% wide so they sit one under the other.

With Grid, I used display: grid and grid-template-columns: 7fr 3fr for the same 70/30 split. I also used grid-template-areas to name the main and sidebar sections. On small screens I switched it to one column so the main content shows first.

I learned that both Flexbox and Grid can make responsive layouts, just in different ways. Flexbox is great for lining things up in one direction, like a row or column. Grid works better when you need rows and columns together. I found Flexbox easier at first, but Grid was really helpful for setting up the page structure because the named areas make it easy to follow.

Overall, this level helped me understand how to make a layout that works on both desktop and mobile. I also learned there isn't just one right way to do it, since both tools can solve the same problem.


