# Exercise 1: HTML

We are going to be creating a personal profile using HTML.

## Set Up

Open up a text editor of your choice and create and navigate to a new empty directory. Then create a file called `index.html`.

```shell
mkdir open-dev-exercise-1
cd open-dev-exercise-1
touch index.html
```

You can then copy the following boilerplate into `index.html`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

> Alternatively, if you are using VS Code, you can use the boilerplate snippet by typing `!` into the empty HTML file. 

## Getting Started

To name our page, we will want to use a `heading 1` tag (`<h1></h1>`). 
This tag indicates the main topic on a web page. We will insert this heading in between our `<body>` tag, which is where a webpages visual content is placed, and write our name between the tags.

```html
...
<body>
    <h1>John Smith</h1>
</body>
...
```

To view our webpages new content, open the directory you created the HTML file in with your computers file finder and manually click on the `index.html` file. This should open a blank page in your default browser. This is your HTML page. You should be able to see a large heading with your name. To see updates to your HTML file, you need to refresh the page.

> Alternatively, you can download the Live Server VS Code extension, right click `index.html` in your file tree in VS Code and then click "Open with Live Server". This prevents you from having to refresh the page on update as Live Server automatically updates the content for you.

## Exercises

### 1. Create a Bio

Try add a short description about yourself under the title. Consider what tag would be most appropriate for this. Give it a heading 2 title. 

<details>
  <summary>Hint</summary>

  Which of the following tags is most suitable for this description:
  
  - `<p>`
  - `<span>`
  - `<h2>`
  - `<section>`
  - `<description>`
</details>

<details>
  <summary>Hint</summary>
  
  The `<p>` tag would be the most appropriate for the description because its use case is for paragraphs. 

  The `<span>` tag is a generic container for inline elements. Inline elements are elements that do not create a new line when placed next to other inline elements. 

  The `<h2>` tag is another heading tag but smaller on the visual hierarchy (smaller font) compared to the `<h1>` tag. Not very suitable for non-heading content. 

  The `<section>` defines a section in a document such as a topic section, such as a heading and its corresponding paragraph content. 

  ```html
  <section>
  <h2>WWF History</h2>
  <p>The World Wide Fund for Nature (WWF) is an international organization working on issues regarding the conservation, research and restoration of the environment, formerly named the World Wildlife Fund. WWF was founded in 1961.</p>
  </section>
  ```

  The `<description>` tag doesn't exist.
</details>

### 2. Sections

Next, create a section for hobbies, skills and one fun fact. Add a relevant image to your fun fact and list your hobbies and skills in an unordered list. Give each section a heading 2.

<details>
  <summary>Hint</summary>

  Use the `<img>` tag and the `<ul>` and `<li>` tag for the list.
</details>

### 3. Content List

Create a content list with quick links to each section (hobbies, skills and fun fact) right below your bio. 

<details>
  <summary>Hint</summary>

  Use `<a>` tags and `<ul>` and `<li>` tags.
</details>

<details>
  <summary>Hint</summary>

  Look into how `<a>` tags can redirect you to specific elements on your page.
</details>

<details>
  <summary>Hint</summary>

  You can use element IDs to link to `<a>` tags.
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
</head>
<body>
    <h1>John Smith</h1>
    <h2>Bio</h2>
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
        aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
        sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
    <h2>Content</h2>
    <ul>
        <li><a href="#hobbies">Hobbies</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#fact">Fun Fact</a></li>
    </ul>
    <h2 id="hobbies">Hobbies</h2>
    <ul>
        <li>Foo</li>
        <li>Bar</li>
        <li>Baz</li>
    </ul>
    <h2 id="skills">Skills</h2>
    <ul>
        <li>Foo</li>
        <li>Bar</li>
        <li>Baz</li>
    </ul>
    <h2 id="fact">Fun Fact</h2>
    <img src="https://www.bigw.com.au/medias/sys_master/images/images/h17/h07/44998281723934.jpg" alt="Crocs image">
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna
        aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
        sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    </p>
</body>
</html>
  ```
</details>