<!---
{
  "id": "ec2d7d19-c8cc-423a-874c-eeacf71d7ab6",
  "depends_on": ["2c7334b3-b07d-48d6-a562-79072d8e166e"],
  "author": "Stephan Bökelmann",
  "first_used": "2025-06-04",
  "keywords": ["SVG", "markup", "graphics", "vector graphics"]
}
--->

# Introduction to SVG Pictures and Markup Editing

> In this exercise you will learn how to create and edit SVG (Scalable Vector Graphics) files by directly writing SVG markup. Furthermore we will explore how to structure simple SVG files, understand their syntax, and preview the graphics you generate.

## Introduction

Scalable Vector Graphics (SVG) is an XML-based markup language for describing two-dimensional vector graphics. Unlike raster images such as JPEG or PNG, SVG images are resolution-independent, meaning they can be scaled to any size without loss of quality. This makes them ideal for web design, technical illustrations, and many forms of digital art.

An SVG file consists of tags that describe shapes such as lines, circles, rectangles, polygons, and paths. It also allows embedding text and applying transformations and styling through CSS or inline attributes. Since SVG is plain text, it can be written and edited directly in any plain text editor.

In this exercise, you will edit SVG files directly by modifying their markup. You will work directly on the file content, adding shapes and attributes by writing XML-style elements and previewing your results in a web browser. This approach helps you deeply understand the structure of SVG files and the meaning of each tag and attribute.

After completing this exercise, you will be able to:

* Understand basic SVG structure.
* Create simple shapes with SVG elements.
* Use attributes such as `stroke`, `fill`, and `transform`.
* Modify and refine SVG files by editing the markup.
* Preview your SVG creations in a web browser.

### Further Readings and Other Sources

* [W3C SVG Specification](https://www.w3.org/TR/SVG2/)
* [MDN Web Docs on SVG](https://developer.mozilla.org/en-US/docs/Web/SVG)
* [A Beginner's Guide to SVG on YouTube](https://www.youtube.com/watch?v=HZv8YHYU3xE)

## Tasks

### Task 1: Create Your First SVG File

1. Create a new SVG file and open it for editing. Name the file:

   ```bash
   simple_drawing.svg
   ```
2. Insert the following minimal SVG skeleton into the file:

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <svg xmlns="http://www.w3.org/2000/svg" width="400" height="400">
       <rect x="50" y="50" width="300" height="300" stroke="black" fill="none" stroke-width="3"/>
   </svg>
   ```
3. Save the file.
4. Open the file in any modern web browser to preview your rectangle.

### Task 2: Add a Circle and a Line

1. Open the file for editing again.
2. Below the `<rect>` element, insert the following elements:

   ```xml
   <circle cx="200" cy="200" r="100" stroke="blue" fill="lightblue" stroke-width="2"/>
   <line x1="50" y1="50" x2="350" y2="350" stroke="red" stroke-width="2"/>
   ```
3. Save and preview your updated SVG file.

### Task 3: Apply Transformations

1. Add a rotated rectangle inside the SVG:

   ```xml
   <rect x="150" y="150" width="100" height="100" stroke="green" fill="yellow" stroke-width="2" transform="rotate(45 200 200)"/>
   ```
2. Notice how the rectangle rotates around its center point `(200, 200)`.
3. Save and refresh your browser to see the transformation effect.

### Task 4: Add Text and Group Elements

1. Insert a group (`<g>`) to organize your elements:

   ```xml
   <g>
       <text x="200" y="390" font-size="24" text-anchor="middle" fill="black">My First SVG</text>
   </g>
   ```
2. Save your file and preview the added text label.

### Task 5: Create a Polygon Shape

1. Below your existing shapes, insert a polygon element:

   ```xml
   <polygon points="100,100 300,100 200,300" stroke="purple" fill="violet" stroke-width="2"/>
   ```
2. This creates a triangle by connecting the given coordinate points.
3. Save and refresh your browser to view the polygon.

### Task 6: Add an Ellipse

1. Insert an ellipse element:

   ```xml
   <ellipse cx="200" cy="200" rx="80" ry="50" stroke="brown" fill="orange" stroke-width="2"/>
   ```
2. This creates an ellipse centered at `(200, 200)` with horizontal and vertical radii.
3. Save and preview the result.

### Task 7: Draw a Polyline

1. Insert a polyline element:

   ```xml
   <polyline points="50,350 150,300 250,350 350,300" stroke="darkgreen" fill="none" stroke-width="3"/>
   ```
2. This creates a zig-zag line connecting the listed points.
3. Save and preview your updated SVG file.

## Advice

By directly editing SVG markup, you gain full control over how your vector graphics are structured and displayed. This approach teaches you how each SVG element and attribute contributes to the final visual result. Start by experimenting with simple shapes and basic attributes. As you become more confident, explore more advanced features such as paths, gradients, and filters. If you make mistakes, simply edit the markup and refresh your browser to see the changes immediately. With time, you will build an intuitive understanding of how vector graphics are described and rendered.
