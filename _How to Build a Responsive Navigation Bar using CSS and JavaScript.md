---
title: # How to Build a Responsive Navigation Bar using CSS and JavaScript
tags: javascript, web-development, programming-blogs
cover: https://www.freelancinggig.com/blog/wp-content/uploads/2017/10/Programming-Language-for-Future.png
domain: satyanchal.hashnode.dev
--- 
# How to Build a Responsive Navigation Bar using CSS and JavaScript

A navigation bar is one of the most important components of any website. Not only does it provide a roadmap for your website visitors, but it also helps in improving the user experience. Thus, creating a responsive navigation bar that looks good on all devices is extremely important. In this post, I’ll guide you on how to build a responsive navigation bar using CSS and JavaScript.

## Step 1: HTML Markup

First, we start by creating the HTML markup for our navigation bar. It is a standard `<nav>` element that contains an unordered list with a few list items that will serve as menu items. Here is the code:

```html
<nav class="navbar">
  <ul class="menu">
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Services</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```

## Step 2: Styling

Next, we move on to styling the navigation bar using CSS. We’ll use flexbox to create a horizontal navigation bar with each menu item evenly spaced out. We’ll also add a background color, and a hover effect on the menu items.

```css
.navbar {
  background-color: #333;
}

.menu {
  display: flex;
  justify-content: space-evenly;
  list-style: none;
  margin: 0;
  padding: 0;
}

.menu li {
  margin: 5px;
}

.menu li a {
  color: #fff;
  text-decoration: none;
  transition: all 0.3s ease;
}

.menu li a:hover {
  color: #d6d6d6;
}
```

## Step 3: Mobile Menu

Now we need to make our navigation bar responsive for smaller devices. One way to do this is by hiding the menu on smaller devices and displaying a button that shows the menu when clicked. Here is the code:

```html
<nav class="navbar">
  <ul class="menu">
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Services</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
  <button class="menu-btn">&#9776;</button>
</nav>
```

```css
.menu-btn {
  background-color: #333;
  border: none;
  color: #fff;
  cursor: pointer;
  display: none;
  font-size: 25px;
  margin: 0;
  padding: 10px 15px;
  text-align: center;
}

@media screen and (max-width: 600px) {
  .menu {
    display: none;
    flex-direction: column;
    margin-top: 50px;
  }
  .menu li {
    margin: 0;
    text-align: center;
    width: 100%;
  }
  .menu-btn {
    display: block;
  }
}
```

## Step 4: JavaScript

Finally, we’ll use JavaScript to show and hide the menu when the button is clicked. Here is the code:

```js
const menuBtn = document.querySelector(".menu-btn");
const menu = document.querySelector(".menu");

let showMenu = false;

menuBtn.addEventListener("click", toggleMenu);

function toggleMenu() {
  if (!showMenu) {
    menu.classList.add("show");
    showMenu = true;
  } else {
    menu.classList.remove("show");
    showMenu = false;
  }
}
```

## Conclusion 

In this tutorial, we learned how to build a simple responsive navigation bar using CSS and JavaScript. You can customize the navigation bar according to your needs and add more features as required. Remember, a navigation bar is an important element of your website, and a responsive one can really make a positive impact on your user experience.
