## Website Performance Optimization portfolio project

The challenge was to optimize this online portfolio for speed! Optimize the critical rendering path and make this page render as quickly as possible.

To get started, check out the repository and follow the steps to first access portfolio on localhost and then expose it public url.

### Getting started

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

  On windows, install python and add the python directory path to your environment 'path' variable then follow steps in command prompt

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.
  On windows, update path variable for installation.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights!

1. Visit [PageSpeedInsights](https://developers.google.com/speed/pagespeed/insights/) and paste your public URL to analyze the application score on mobile and desktop.


#### Steps taken to improve the performance

## Part 1: Optimize PageSpeed Insights score for index.html
1. Loading external font only for deskop or screens having width at least 500px
1. Adding styles in html instead of making a extra server request.
1. Adding media attribute for print.css link tag.
1. Compressed time consuming images

## Part 2: Optimize Frames per Second in pizza.html
1. First improvement for scrolling: moved document.body.scrollTop property query outside the loop to prevent repetitive query.
1. Second improvement for pizza re-size: removed the need for determining dx, using percentage instead.
