# Introduction to HTML & CSS Workshop-Day 2
--

## Links:

[Examples Day 2](https://repl.it/@melodyserra/Examples-Day-2)

[Tables](https://repl.it/@melodyserra/Tables)

[Fonts](https://repl.it/@melodyserra/Fonts)

[Overlay](https://repl.it/@melodyserra/Overlay)

[Final Project](https://repl.it/@melodyserra/Final-Project)

## The Grid Layout
- Most modern layouts operate on a standard 12-column grid system.
- If you break down any of the websites you know and love you will notice many variations on the 12 column grid.
- Each column in the grid can contain nested grids itself.
- If you want a larger box, you need to have a greater column offset.
- Here is a good pictorial to help you break it down:

![Grid Pictorial](../img/grid.jpg)

- And [here](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout) is a great resource to introduce you to the grid layout. 

## Linking JS with HTML
- JavaScript enables interaction with the page.
- In order to run external JS you need to link it to the HTML. This usually goes before the closing `body` tag:

```js
<script src="js/script.js"></script>
```

# Responsive Design

## Twitter Bootstrap
- Bootstrap is a front-end framework that incorporates a grid system, UI components, JavaScript widgets and more.
- Let's take a look at the documentation: [http://getbootstrap.com](http://getbootstrap.com/).
- The framework consists of one main CSS file, an optional theme CSS file, and a main JS file.
- Bootstrap requires jQuery to work, which is a JavaScript framework.

## Using Bootstrap
- To use Bootstrap you have to include the three required files.
- Bootstrap files can be linked via the CDN provided, or downloaded locally onto the computer.
- Remember to place your reference to the jQuery library above your reference to the Bootstrap JS code.

## Bootstrap Columns
- Columns are written in this format as a class attribute: col-(breakpoint)-(offset).
- An example of a three-column layout may be to use the class col-sm-4.
- All columns should be wrapped into an element with a class of row.
- So the complete three-column layout may look something like this:

```html
<div class="row">
	<div class="col-sm-4">
		Content Here
	</div>
	<div class="col-sm-4">
		Content Here
	</div>
	<div class="col-sm-4">
		Content Here
	</div>
</div>
```

## Breakpoints
- The way that Bootstrap works is to dynamically reduce column size according to the window size.
- To be mobile-friendly, the columns will break into a stack layout after a minimum width is detected.
- The breakpoints you can select in your columns control at which point this happens.
- Check out their documentation [here](http://getbootstrap.com/css/#grid) to see what these breakpoints are in terms of size.

## CSS3 Media Queries
- Media queries allow you to apply and remove CSS styling based on the screen dimensions.
- This is important to create truly mobile-friendly layouts.
- To use it you have to specify screen resolution thresholds.
- Let's try an example where we want to show a div where the screen size is larger than 700 pixels:

HTML

```html
<div id="my-div"></div>
```

CSS

```css
@media(min-width: 700px) {
	#my-div {
		width:400px;
		height:400px;
		border:#000 1px solid;
	}
}
```

- Now where the screen size is below 700 pixels:

CSS

```css
@media(max-width: 700px) {
	#my-div {
		width:400px;
		height:400px;
		border:#000 1px solid;
	}
}
```

- You can also combine these values to select a range:

```css
@media(min-width: 700px) and (max-width: 900px) {
	#my-div {
		width:400px;
		height:400px;
		border:#000 1px solid;
	}
}
```

- Good news! Bootstrap does this for you!

## UI Elements
- Bootstrap wraps in a myriad of great UI elements that you can drop in anywhere on your site.
- With Bootstrap you can make really pretty things quickly.
- Let's look at some [examples](http://getbootstrap.com/components/).

## Putting it Together
- Let's take a look at some of the bootstrap examples located [here](http://getbootstrap.com/getting-started/#examples).
- We will code together the "Jumbotron Narrow" template located [here](http://getbootstrap.com/examples/jumbotron-narrow/).
- Before we start, let's also plan out our grid system.

## Extra Lab
- For this lab we will be coding from scratch [this Bootstrap template](http://getbootstrap.com/examples/offcanvas/).
- Try not to look at the code through the code inspector. 
- First plan out the grid you will use, then figure out which components you will need.
	- Hint: There is a jumbotron in there.

## CSS Transitions
- Transitions allow you to go between element states smoothly.
- You will often use these for animations with CSS.
- This is the syntax:

```
transition: property duration easing;
```

Let's take a look at an example:

```css
.box {
	width:100px;
	height:100px;
	background-color:blue;
	transition: width 1s ease-in-out;
}

.box:hover {
	width:200px;
	height:200px;
	background-color:red;
	transition: width 1s ease-in-out;
}
```

- You can specify `all` instead of each property to animate the entire state.

## Email Templates 
- Using tables can allow for nesting (tables within tables).
- Gives you control over where you position things. 

![image](../img/shots.jpg)

## Discussion About Animated Web Banners
- HTML is a good option because of its compatibility, it supports multimedia elements, and it is lightweight. 
- [A good read on this:](https://www.disruptiveadvertising.com/graphic-design/animated-banner-ads/)
- [A good tutorial](https://tympanus.net/codrops/2012/01/10/animated-web-banners-with-css3/)
- Since this could involve pretty complex CSS animations and transitions, there are tools such as Bannersnack that could help here.

## Advanced Styling Topics 
### Typography 
- Google Fonts
- Font Awesome
- Linking to fonts
- Text tracking refers to the space between letters, this can be controlled using a CSS property called **letter spacing**

```css

h1 { 
	letter-spacing: −1px; 
}


```
- The text between lines of text is controlled by a CSS property called **line-height**, it is often set as a unitless value so that it is proportional to the font-size. 

```css

p {
    line-height: 1.5;
}
```
- There are various units that can be used when setting a font-size:
	- relative versus absolute 
	- click [here](https://www.w3schools.com/cssref/css_units.asp) to find out more 

### Color
- There are three main ways to use colors in CSS - semantic, HEX values, and RGB(A) values.

##### Semantic:

```css
div {
	background-color:black;
}
```

##### HEX:

```css
div {
	background-color:#000000;
}
```

##### RGBA:

```css
div {
	background-color:rgba(0,0,0,0.5);
}
```

#### CSS Gradients
- CSS gradients were introduced as of CSS3.
- They allow for a gradient of colors to be applied across multiple solid colors.
- These are hard to write via raw CSS, so generators are often used.
- Let's have a look at one [here](http://www.colorzilla.com/gradient-editor/).

### Images
- Background images:
	- Let's have a look at one [here](https://css-tricks.com/perfect-full-page-background-image/).
- Manipulating images:
	- sizing
	- [z-index](https://repl.it/@melodyserra/Examples-Day-2)
	- [masking](https://css-tricks.com/clipping-masking-css/)
	- [overlay](https://repl.it/@melodyserra/Overlay)
	- [opacity](https://repl.it/@melodyserra/Overlay)
	- [hover](https://repl.it/@melodyserra/Overlay)
	- [box shadow](https://www.w3schools.com/css/css3_shadows.asp)
	- [rotating](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/rotate)
	- [responsiveness](https://repl.it/@melodyserra/Examples-Day-2)

## Putting it Together
- For this lab we will be creating a personal landing page using HTML and CSS.
- A starter page has been created for you [here](about_me_starter_website/).
- This is meant to be creative, but make sure to at least do the following:
	- Add the class "fixed-top" to the header to make it stay in place during scroll.
	- Use rgba colors to make the header navbar semi-transparent.
	- Use Google Fonts to implement a font of your choice for the logo.
	- Replace the picture of me with one of you :) You will need to look up the <img> tag to make this happen.
	- Replace the picture of the motorcycle with a background of your choice (Hint: Have a look at the CSS to find out where this background comes from).
	- Make the background of the banner have a parallax effect. Hint: Research the "background-attachment" property in CSS.
	- Change the text throughout the page to reflect your own personal information.
	- Add a gradient to the background of the user-info-text class in CSS.
	- **Bonus:** Implement a small animation using CSS somewhere on the page. You may want to research the `transition` and `transform` CSS properties.
