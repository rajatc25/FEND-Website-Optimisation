## Website Performance Optimization portfolio project

## Goals and Expectations from this Mobile Portfolio Project 

This project is the part of Udacity Front-end Web Developer Nanodegree. The requirement for this project is to optimize the online portfolio for speed! 

### Getting started

### Requirements for completing the project

#### Part 1: Optimize PageSpeed Insights score for ```index.html```
##### Goal
- [x] Achieve 90+ page speed score for Mobile.
- [x] Achieve 90+ page speed score for Desktop.

#### Part 2: Optimize Frames per Second in pizza.html
##### Goal
- [x] Optimizations made to ```views/js/main.js``` make ```views/pizza.html``` render with a consistent frame-rate at 60fps when scrolling.
- [x] Time to resize pizzas is less than 5 ms using the pizza size slider on the ```views/pizza.html``` page.

****************************************************************************************************************************************************************************************

## Changes made to achieve optimization 
	
### How to Access the site:
1. go to my [Github](https://github.com/rajatc25/FEND-Website-Optimization) repository for the project
2. The site is also being hosted by github at: https://rajatc25.github.io/FEND-Website-Optimization/

### Part 1: Optimize PageSpeed Insights score for index.html

Website Location: https://rajatc25.github.io/FEND-Website-Optimization/

Changes Made to index.html
 - Downloaded all image assets to utilize locally
 - Resized and compressed all images.
 - Used local fonts vs remote fonts.
 - Brought all css to index.html to avoid linking to other files.
 - Placed above the fold CSS in my header and placed other CSS below the body.
 - Added cache control meta tag to leverage browser caching.
 - Placed the links for analytics.js and perfmatters.js below the body.

PageSpeed Insights Scores:

1- Desktop: 94/100
2- Mobile: 92/100

### Part 2: Optimize Frames per Second in pizza.html

Website Location: https://rajatc25.github.io/FEND-Website-Optimization/views/pizza.html

Changes Made:
pizza.html
 - Compressed two(2) images [pizzeria.jpg and pizza.png]

main.js
 - Update function changeSliderLabel() and determineDx ()
     To use documnet.getElementById instead of document.querySelector because it's more efficient accessing the DOM
 - Update changePizzaSizes() to help avoid forced synchronous layout bottle necking	  
	 To use document.getElementsByClassName & is more efficient accessing the DOM instead of document.querySelector
	 Moved reading layout properties outside of the loop and  batch update the styling afterwards
 - Update function updatePositions()
     To use document.getElementsByClassName('mover') is more efficient accessing the DOM instead of instead of querySelectorAll(.'mover')
     Moved all code reading layout property 'scrollTop'  outside of the loop and batch update the styling afterwards
     Reduced the number of pizza images appended to 25.
	 
#### NOTE: To read minified files in their original version, use online tools like CSS,JS,HTML Beautifier/Formatter.
	 
****************************************************************************************************************************************************************************************
	
## Original README content 
	

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

### Getting started

#### Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

#### Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js.

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
