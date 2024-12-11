# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

What are the main differences between Flexbox and Grid layouts? Describe scenarios where each layout system would be more suitable.

### Response 1

The main difference between Flexbox and Grid layouts is that Flexbox is primarly designed for one-dimensional layouts (arranging items in a row or column), while the grid is designed for two-dimensional layouts, allowing precise control over placing items in both rows and columns simultaneously, this makes flexbox ideal for simpler alignments with a single direction.

## Prompt 2

What is the difference between `justify-content` and `align-items` in Flexbox? How does each property control the positioning of flex items within the container?

### Response 2

The difference between `justify-content` and `align-items` in Flexbox is the axis that it controls the alignment of items on. The `justify-content` property controls the alignment and positioning of flex items on the main axis within the container, while the `align-items` property controls the alignment and positioning of flex items on the cross axis.

The main axis is the primary direction in which flex items are laid out, determined by the `flex-direction` property. For example:

- If `flex-direction` is `row` (default), the main axis runs horizontally from left to right.
- If `flex-direction` is `column`, the main axis runs vertically from top to bottom.

The `justify-content` property controls the alignment and spacing of flex items along the main axis. It can align items to the start, center, or end of the main axis, or distribute them evenly with spacing options like space-between, space-around, or space-evenly.

The cross axis is perpendicular to the main axis. If the main axis is horizontal (`flex-direction: row`), the cross axis runs vertically, and if the main axis is vertical (`flex-direction: column`), the cross axis runs horizontally.

- The align-items property controls the alignment of flex items along the cross axis. For example, it can align items to the start, center, or end of the cross axis, or stretch them to fill the container's cross-axis space.

## Prompt 3

Describe the difference between `grid-template-areas` and `grid-template-columns`/`grid-template-rows`. When might you prefer one approach over the other?

### Response 3

In CSS Grid, `grid-template-areas` and `grid-template-columns/grid-template-rows` are tools for defining the structure of a grid layout, but they serve different purposes and are used in different scenarios

`grid-template-areas`
Purpose: Defines a layout by assigning named areas to specific cells or groups of cells in the grid.
How it works: You specify a template using a text representation of the grid, where each name corresponds to an area.

`grid-template-columns` and `grid-template-rows`
Purpose: Directly defines the size and structure of the grid's columns and rows.
How it works: You explicitly specify the size of each column and row.

Prefer `grid-template-areas`:

When readability and maintainability are priorities.
For layouts that might be rearranged frequently (e.g., responsive designs).
When naming regions of the layout enhances understanding and debugging.

Prefer `grid-template-columns`/`grid-template-rows`:

When you need fine-grained control over column/row dimensions.
For simpler layouts or when you don't need named areas.
In cases where the grid's alignment and spacing (gaps) are more critical than the semantic naming of areas.

## Prompt 4

Explain the `min-width` and `max-width` keywords in media queries. How do they help create responsive breakpoints for different screen sizes?

### Response 4

The `min-width` and `max-width` keywords in media queries are features that allow us to apply specific styles to a webpage based on the screen width of a user's device.

- The `min-width` media query applies styles to a webpage only when the screen width is **greater** than or **equal** to a certain minimum width value.
- The `max-width` media query applies styles to a webpage only when the screen width is **less** than or **equal** to a certain maximum width value.

These keywords help us create responsive breakpoints for different screen sizes, allowing websites to adapt gracefully to different devices, such as desktops, tablets, and mobile phones, for a better user experience.

## Prompt 5

Imagine you are teaching a brief lesson on **mobile first design**. Your lesson should include the following information:

- An explanation of mobile first design and a few of the benefits of this approach
- A CSS code example demonstrating how to use media queries to adjust the layout of a container from mobile to desktop with either Flexbox or Grid (choose one).
- An explanation of the code example.

### Response 5

Here’s a mobile-first approach to styling a container that adjusts from a single-column layout on mobile to a two-column layout on larger screens.
Lesson: Introduction to Mobile First Design
What is Mobile First Design?
Mobile First Design is a design philosophy that prioritizes creating a seamless user experience on mobile devices before scaling up to larger screens like tablets or desktops. This approach involves designing layouts and features for smaller screens first and progressively enhancing the design for larger viewports using techniques like media queries.
Benefits of Mobile First Design:
Improved User Experience: Ensures that the core functionality is optimized for mobile users, who often form the majority of web traffic.
Faster Load Times: Smaller screens force you to prioritize content and optimize performance, leading to faster loading times.
Scalability: Designs are more adaptable when built from small screens up, ensuring that content flows logically as screen size increases.
SEO Benefits: Search engines, like Google, favor mobile-friendly sites in their rankings, improving visibility.
CSS Code Example: Mobile First Layout Using Flexbox
Below is an example of a layout that starts with a mobile-friendly single-column layout and adjusts to a two-column layout on larger screens using media queries.
html
Copy code

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mobile First Design</title>
  <style>
    /* Base (mobile-first) styles */
    .container {
      display: flex;
      flex-direction: column; /* Stacks items vertically */
      gap: 1rem;
      padding: 1rem;
    }
    .item {
      background-color: #F0F0F0;
      border: 1px solid #ccc;
      padding: 1rem;
      text-align: center;
    }
    /* Desktop styles: two-column layout */
    @media (min-width: 768px) {
      .container {
        flex-direction: row; /* Arranges items horizontally */
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
  </div>
</body>
</html>
Explanation of the Code
Mobile-First Base Styles:
The .container uses display: flex with flex-direction: column, stacking items vertically by default.
A gap property ensures spacing between items, and padding provides breathing room inside the container.
These base styles cater to mobile users, ensuring the layout is simple and legible on small screens.
Media Query for Larger Screens:
The @media (min-width: 768px) rule applies styles for devices with a viewport width of at least 768 pixels (e.g., tablets and desktops).
flex-direction: row changes the layout to arrange items horizontally in a two-column layout, better utilizing the available screen space.
Responsive Design in Action:
As users access the site on larger screens, the layout automatically adjusts, providing an optimized experience without sacrificing the mobile-first approach.
