# Exercise 2: CSS

In this exercise, we are going to style our personal profile we made in exercise 1. 

## Set Up

In the same directory you created your personal profile HTML page, create a `styles.css` file. Then link this file to your HTML page by adding the following line below between the `<head>` tags in the HTML file.

```html
<head>
    ...
    <link rel="stylesheet" href="styles.css">
</head>
```

We have now linked our CSS file to our HTML file.

## Getting Started

Let's clean up some of the default styling that comes with HTML, so we don't have any unexpected behavior, and set some new global defaults of our own. In `styles.css`, use the `*` selector to select all elements on the document. Set all `padding` and `margins` to `0` and add `box-sixing: border-box;` ([more about `box-sizing`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)). We will also change the global font.

```css
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: Arial,
        Helvetica,
        sans-serif
}
```
## Exercises

### 1. Making Space for Heading 1

Let's space out our Heading 1. Make the Heading 1 take up a whole view screen worth of height.

<details>
  <summary>Hint</summary>

  You will need to use a container element to wrap the heading 1 and then set the height of this container element to be the height of the screen.
</details>

<details>
  <summary>Hint</summary>

  To manipulate a specific element's style, give the element a `class` in the HTML and then reference this class in the CSS file using `.class_name` to select it.
</details>

<details>
  <summary>Hint</summary>

  You should use a `<div>` tag as your container element since it is a generic tag and since it is a block element, each `<div>` takes up the whole screen width so they don't collapse side by side.

  A `<span>` is the inline equivalent of `<div>`. Try using `<span>` as the container tag and see what happens to better understand inline vs block elements.
</details>

<details>
  <summary>Hint</summary>

  Use the `height` attribute and the `vh` CSS unit to set the height of each section.
</details>

### 2. Center the Heading 1

Position the heading 1 element in the center of the container.

<details>
  <summary>Hint</summary>

  Search up `display: flex;`
</details>

<details>
  <summary>Hint</summary>

  Search up `justify-content: center;` and `align-items: center;`.
</details>

### 2. Center the sections and spread them out

For each section, give them a width of `1200px` and center them. Spread them

<details>
  <summary>Hint</summary>

  You will need to create a container element for each section and another container element for all sections. Apply flex-box to the outer container.
</details>

<details>
  <summary>Hint</summary>

  To center the sections, look into the `flex-direction` attribute.
</details>

<details>
  <summary>Hint</summary>

  Spread out the sections by giving the section containers margins. 

  Try to make the margin only apply to the top and bottom of the containers.
</details>

### 3. Get rid of the dot points

Get rid of the dot points for the unordered lists. We still want to keep them as `<li>` elements because it is still a list and we want to pick the element with the best corresponding semantic meaning.

<details>
  <summary>Hint</summary>

  Look into the `list-style-type` element.
</details>

<details>
  <summary>Hint</summary>

  You can apply a global `<li>` styling by using the element selector in CSS rather than a class selector.
</details>

### 4. Format fun fact section

Resize the image for the fun fact section and make the fun fact text sit beside it rather than below it.

<details>
  <summary>Hint</summary>

  You can resize the image just by changing its width.
</details>

<details>
  <summary>Hint</summary>

  You can move the text next to the image by using flex box.
</details>

### 5. Smooth scrolling

Change the scrolling behavior of clicking links in the Content section to be smooth.

<details>
  <summary>Hint</summary>

  Search `scroll-behavior`.
</details>

<details>
  <summary><h2>Example Solution</h2></summary>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="heading-container">
        <h1>John Smith</h1>
        
    </div>
    <div class="sections">
        <div class="section-container">
            <h2>Bio</h2>
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
                aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
                Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
                sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            </p>
        </div>
        <div class="section-container">
            <h2>Content</h2>
            <ul>
                <li><a href="#hobbies">Hobbies</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#fact">Fun Fact</a></li>
            </ul>
        </div>
        <div class="section-container">
            <h2 id="hobbies">Hobbies</h2>
            <ul>
                <li>Foo</li>
                <li>Bar</li>
                <li>Baz</li>
            </ul>
        </div>
        <div class="section-container">
            <h2 id="skills">Skills</h2>
            <ul>
                <li>Foo</li>
                <li>Bar</li>
                <li>Baz</li>
            </ul>
        </div>
        <div class="section-container">
            <h2 id="fact">Fun Fact</h2>
            <div class="fun-fact">
                <img src="https://www.bigw.com.au/medias/sys_master/images/images/h17/h07/44998281723934.jpg" alt="Crocs image">
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
                    magna
                    aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
                    consequat.
                    Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
                    sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                </p>
            </div>
        </div>
    </div>
</body>
</html>
```

```css
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: Arial,
        Helvetica,
        sans-serif;
    scroll-behavior: smooth;
}

.heading-container {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.sections {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.section-container {
    width: 1200px;
    margin: 60px 0;
}

li {
    list-style-type: none
}

img {
    width: 400px;
}

.fun-fact {
    display: flex;
}
```
</details>