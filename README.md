# Flex Practice

# Building a Website Landing Page Using HTML and CSS

![Flexbox Website Screenshot](https://github.com/techcodedu/flexpractice/blob/main/flexboxwebsite.png)


## Introduction
In this exercise, you will learn how to build a website landing page using HTML and CSS. You will create the different parts of the website such as the header, navigation, and main content. The design will heavily use CSS flexbox and positioning properties.

## Prerequisites
- Basic understanding of HTML and CSS

## Project Overview
In this tutorial, you will be creating the following parts of the website:
1. **Header**: This will contain the brand name and the navigation links.
2. **Navigation**: This will contain links to the different sections of the website.
3. **Main Content**: This will contain a call to action section and a card section.

Now, let's get started!

### Step 1: Setting Up the Boilerplate HTML
File Structure
````markdown
project-folder/
│
├── css/
│   └── webdesignusingflex.css
└── index.html
````

Start by creating a new HTML file called `index.html`. This file will contain the structure of your website. Copy the following HTML code into your `index.html` file.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Landing Page</title>
    <link
      href="https://fonts.googleapis.com/css2?family=Raleway:wght@300;400;700&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="css/websitewithflex.css" />
  </head>

  <body>
    <div class="container">
      <div class="overlay"></div>
      <header>
        <h1>Brand Name</h1>
        <nav>
          <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Action</a></li>
            <li><a href="#">Drop</a></li>
          </ul>
        </nav>
      </header>
      <main class="content">
        <section class="column">
          <h2>Call To Action</h2>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Repellendus, totam harum! Soluta alias mollitia quaerat placeat
            asperiores voluptate error atque!
          </p>
          <button class="cta-button">Button</button>
        </section>
        <section class="column">
          <article class="card-container">
            <img
              src="https://images.pexels.com/photos/16457381/pexels-photo-16457381/free-photo-of-city-dawn-sunset-eiffel-tower.jpeg"
              alt="Card image"
            />
          </article>
        </section>
      </main>
    </div>
  </body>
</html>


```

This is the boilerplate HTML file that you will use as the starting point for your website design.

### Step 2: Creating the CSS Folder and File
Create a folder named `css` and inside the `css` folder, create a new file named `webdesignusingflex.css`.

### Step 3: Linking the CSS File
In your `index.html` file, link the `webdesignusingflex.css` file by adding the following line of code inside the `<head>` tag.

```html
<link rel="stylesheet" href="css/webdesignusingflex.css" />
```

### Step 4: Styling the Body and HTML
In this step, we will target the `body` and `html` of the markup and assign the following rules:

```css
body, html {
    height: 100%;
    margin: 0;
    font-family: "Raleway", sans-serif;
}
```

As a result of these rules, all margins will be reset to 0, the font-family will be set to "Raleway", and the height of the `body` and `html` will be set to 100%.

### Step 5: Styling the Container
Next, let's style the `container` class. This class is responsible for holding the entire content of the website. Add the following CSS rules:

```css
.container {
    position: relative;
    height: 100vh;
    background-image: url("https://images.pexels.com/photos/16457381/pexels-photo-16457381/free-photo-of-city-dawn-sunset-eiffel-tower.jpeg");
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    box-sizing: border-box;
    padding: 20px;
}
```

The `container` class will have a background image, its size will cover the entire viewport, it will display its children using flexbox, and it will have white text color.

### Step 6: Adding an Overlay
To add an overlay to the background image, add the following CSS rules:

```css
.overlay {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: rgba(0, 0, 0, 0.5);
}
```

The `overlay` class will have a black background with 50% opacity, and it will cover the entire `container`.

### Step 7: Styling the Header
Now, let's style the `header` element. Add the following CSS rules:

```css
header {
    position: fixed;
    top: 20px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-sizing: border-box;
    padding: 0 20px;
    max-width: 1200px;
    margin: auto;
}
```

The `header` element will be fixed at the top of the page, will have a maximum width of 1200px, and will display its children using flexbox.

### Step 8: Styling the Navigation
Next, let's style the `nav` element and its children. Add the following CSS rules:

```css
nav ul {
    display: flex;
    gap: 20px;
    list-style-type: none;
    padding: 0;
    margin: 0;
}

nav a {
    color: white;
    text-decoration: none;
    font-size: 16px;
    transition: color 0.3s ease;
    text-transform: uppercase;
}

nav a:hover {
    color: #3498db;
}
```

The `nav ul` element will display its children using flexbox, and the `nav a` elements will have white text color, no text decoration, and will change color on hover.

### Step 9: Styling the Main Content
Now, let's style the `main` element and its children. Add the following CSS rules:

```css
main {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: flex-start; /* Align items to the top */
    width: 100%;
    max-width: 1200px;
    margin: auto;
    gap: 20px;
    padding-top: 100px;
}
.column {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    height: 100%; /* new */
}
```

The `main` element will display its children using flexbox, and the `column` class will display its children in a column using flexbox.

### Step 10: Styling the Call to Action Section
Next, let's style the call to action section. Add the following CSS rules:

```css
.column h2 {
    font-size: 48px;
    margin: 0 0 10px;
    font-weight: 700;
    line-height: 1.2;
}

.column p {
    font-size: 24px;
    margin: 0 0 20px;
    line-height: 1.8; /* adjusted */
}

.cta-button {
    padding: 10px 20px;
    background: transparent; /* No background */
    border: 2px solid #e67e22; /* Orange border */
    color: white;
    font-size: 24px;
    cursor: pointer;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    transition: border-color 0.3s ease, color 0.3s ease;
}

.cta-button:hover {
    border-color: #d35400; /* Darker orange border on hover */
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
    color: #d35400; /* Darker orange text on hover */
}
```

The `column h2` and `column p` elements will have a specific font size, margin, and line height. The `cta-button` class will have

 a transparent background, orange border, white text color, and will change border color and text color on hover.

### Step 11: Finally,Styling the Card Section
Next, let's style the card section. Add the following CSS rules:

```css
.card-container {
  display: flex;
  justify-content: center;
  align-items: center;
  background: rgba(255, 255, 255, 0.9); /* Semi-transparent white background */
  padding: 10px;
  border-radius: 10px; /* Rounded corners */
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1); /* Shadow */
  margin: 20px 0;
}

.card-container img {
    width: 100%;
    height: auto;
    border-radius: 10px;
}

.card-container h3 {
    font-size: 36px;
    margin: 0 0 10px;
}

.card-container p {
    font-size: 16px;
    margin: 0 0 10px;
    line-height: 1.8;
}
```

## Conclusion
Congratulations! You have successfully created a website landing page using HTML and CSS. You learned how to use the flexbox and positioning properties.
