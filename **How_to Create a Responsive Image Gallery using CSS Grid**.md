---
title: How to Create a Responsive Image Gallery using CSS Grid
tags: javascript, web-development, programming-blogs
cover: https://images.unsplash.com/photo-1626968361222-291e74711449?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwzNDExMjB8MHwxfHNlYXJjaHw4fHxzZXR1cHxlbnwwfHx8fDE2Nzg3OTgxMDI&ixlib=rb-4.0.3&q=80&w=1080
domain: satyanchal.hashnode.dev
--- 
**How to Create a Responsive Image Gallery using CSS Grid**

If you're a web developer, you know that designing a responsive image gallery can be a challenge. However, with the advent of CSS Grid, it has become easier and more efficient to create a responsive grid for images. In this blog post, we'll walk you through the steps on how to create a responsive image gallery using CSS Grid.

## Step 1 - Set Up Your HTML

To get started with creating a responsive image gallery, you'll need to set up your HTML file. Here's an example of what your HTML code should look like:

```html
<section class="gallery">
  <img src="image1.jpg" alt="Image 1"/>
  <img src="image2.jpg" alt="Image 2"/>
  <img src="image3.jpg" alt="Image 3"/>
  <img src="image4.jpg" alt="Image 4"/>
  <img src="image5.jpg" alt="Image 5"/>
  <img src="image6.jpg" alt="Image 6"/>
</section>
```

In this example, we have an HTML section called "gallery" with six images inside.

## Step 2 - Set Up Your CSS

Now that your HTML is set up, you'll need to write your CSS. Here's what your CSS code should look like:

```css
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  grid-gap: 1rem;
}

.gallery img {
  width: 100%;
  height: auto;
}
```

In this example, we set our "gallery" section to display as a grid. We then defined our grid-template-columns using the repeat and minmax functions. The repeat function tells the grid to repeat a certain number of columns, and the minmax function tells the grid to use a minimum and maximum width for each column. In this case, we've told the grid to repeat as many columns as possible, with a minimum width of 250px, and a maximum width of 1fr (which means it will take up the available space in the grid). We've also set a grid-gap of 1rem to give some space between the images.

We've also given our gallery images a width of 100% and a height of auto. This will ensure that the images always fill their respective grid cells while maintaining their aspect ratios.

## Step 3 - Add Media Queries

To make our image gallery truly responsive, we need to add media queries. Here's what our updated CSS code should look like:

```css
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  grid-gap: 1rem;
}

.gallery img {
  width: 100%;
  height: auto;
}

@media screen and (min-width: 768px) {
  .gallery {
    grid-template-columns: repeat(3, 1fr);
  }
}
```

In this example, we've added a media query that targets screens with a width of 768px or more. In this query, we change the grid-template-columns property to repeat three columns, each taking up 1fr of the available space.

## Conclusion

Creating a responsive image gallery using CSS Grid is an efficient and effective way to display your images on your website. By following these simple steps, you can create a beautiful and responsive gallery that looks great on any device.
