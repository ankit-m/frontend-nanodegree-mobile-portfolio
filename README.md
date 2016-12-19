## Website Performance Optimization portfolio project

### Part 1: Optimize PageSpeed Insights score for index.html

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

#### Optimizations

1. Minify `index.html` using online HTML minifiers
2. Add media attributes to appropriate CSS link tags
3. Add async attribute to appropriate analytics scripts
4. Inline `style.css`
5. Reduce the size (resolution) of `pizzeria.jpg`
6. Inline Google fonts by copying the CSS into inlint `style` tags.

### Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js.

#### Optimizations

1. Remove FSL (Forced Synchronous Layouts) in two loops
2. Reduce the number of pizzas from 200 to 24
3. Add `transform: translateZ(0);` in `.mover` class to trigger GPU.
