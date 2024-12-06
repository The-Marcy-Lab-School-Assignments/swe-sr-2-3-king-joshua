# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

What are the main differences between Flexbox and Grid layouts? Describe scenarios where each layout system would be more suitable.

### Response 1

The main difference between Flexbox and Grid layouts is that Flexbox is primarly designed for one-dimensional layouts (arranging items in a row or column), while the grid is designed for two-dimensional layouts, allowing precise control over placing items in both rows and columns simultaneously, this makes flexbox ideal for simpler alignments with a single direction.

## Prompt 2

What is the difference between `justify-content` and `align-items` in Flexbox? How does each property control the positioning of flex items within the container?

### Response 2

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

### Response 4-

## Prompt 5

Imagine you are teaching a brief lesson on **mobile first design**. Your lesson should include the following information:

- An explanation of mobile first design and a few of the benefits of this approach
- A CSS code example demonstrating how to use media queries to adjust the layout of a container from mobile to desktop with either Flexbox or Grid (choose one).
- An explanation of the code example.

### Response 5

Here’s a mobile-first approach to styling a container that adjusts from a single-column layout on mobile to a two-column layout on larger screens.
