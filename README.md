Running the Application:
-Put this address in the search bar of browser: https://jennylynn89.github.io/frontend-nanodegree-mobile-portfolio/
-Open in browser

Optimizations to achieve Page Speed score at or above 90:
-In index.html:
	*commented out google fonts
	*added async to google analytics
	*added media="print" for print.css
	*inlined styles.css
	*resized pizzeria and profile pics (used optimized version from PageSpeed Insights)
-Results: 
	*Score of 95 for mobile
	*Score of 97 for desktop

Optimizations to main.js to reach 60 fps:
-Line 535: reduced number of pizzas to 24
-Moved calculations for scrolling out for loops and put into vars
-Replaced document.querySelectorAll with document.getElementsByClassName where appropriate
-Replaced document.querySelector with document.getElementById where appropriate
-Created var phraseArray to avoid accessing the DOM with each scrolling
-Moved phase calculation out of for loop 
-Reduced painting time by adding backface-visibility: hidden to .mover class in css
-Refactored changePizzaSizes to simplify and reduce accessing DOM