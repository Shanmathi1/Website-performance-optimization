Website Performance Optimization Project

About: 
The objective for this project was to optimize Cameron Pittman's portfolio(https://github.com/gosukiwi/web-performance-portfolio) page for speed. The strategy was to optimize the critical rendering path, making the page render as quickly as possible, using techniques learnt in the Website Performance Optimization Course(https://www.udacity.com/course/ud884).

Page load speed optimization:
- Minify CSS/JS: All CSS and JS files were minified to ensure faster downloading. 
- Media CSS:  A media attribute was added to print stylesheet to ensure that it would only be downloaded when printing.
- Inline CSS: Critical above-the-fold content styles are inlined and applied to the document immediately vs. blocking loading. 
- Compress Images: Images were rescaled and resized to the final layout dimensions.
- Async attribute was added to execute the script asynchronously.

Frame rate optimization:
- Loop optimization: unnecessary JS operations were pulled out of for loops where possible, in views/js/main.js.
- Debouncing: scroll events were 'debounced' to decouple the animations and only reflow/repaint when needed.
- Changed all querySelector to getElementById.
- In addEventListener, loop through 32 (8 per row x 4 rows) times instead of 200 times
