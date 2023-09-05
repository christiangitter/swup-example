# Create nice page transitions wihth swup

## Pre-requisites
make sure you have node installed:
```bash
node -v
```
if not, install it:
```bash
choco install nodejs
```

## Installation
To install swup, run the following command in your terminal:
```bash 
npm i swup
```
then, import the js file in your html file:
```html
<script src="./node_modules/swup/dist/Swup.umd.js"></script>
<script src="./node_modules/swup/dist/Swup.modern.js"></script>
<script src="./node_modules/swup/dist/Swup.module.js"></script>
```

## Usage
To use swup, you need to create a new instance of swup in a seperate js file and pass it the options you want to use.
```js
const swup = new Swup();
```

You need to create the transition in a css file. You can use the following code as a template:
```css
html.is-changing .transition-fade {
    transition: opacity 0.25s;
    opacity: 1;
}

/* Define the styles for the unloaded pages */
html.is-animating .transition-fade {
    opacity: 0;
}
```

Now you need to create the section which you want to transition to. You can use the following code as a template:
```html
<section class="transition-fade" id="swup">
    <h1>Page 2</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.</p>
</section>
```