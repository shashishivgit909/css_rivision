## For css flex box : Go this docs: https://css-tricks.com/snippets/css/a-guide-to-flexbox/   (recommneded by chai with code).

###     ###################     POSITION       ############
1. VVVVI: to move child div with realtive to parent div we have to give  child div { postion:absolute } and parent div should have  non static position and if no such ancestor found then element move realtive to body .By default every element have position staic so , static positioned div wont get affected by left ,right , top , bottom until other position value given.

2. VVI:position:sticky: <header className="p-3 shadow-xl sticky top-0 z-[9999] bg-white">  : header becomes at top of view port sticky with top of all other lement by z-index

3. 

## Default Flex Direction
    Default Value: row
    Effect: Flex items are arranged in a row, starting from the left.
    Nested Flex Containers
    When you have a parent flex container and a child that is also a flex container, the flex-direction property of the parent does not affect the flex-direction property of the child. Each flex container has its own independent set of flex properties.



## Transition Property:   (By Shradha didi)
=> Elements have different states (eg: active , hover   we can see it in inspect). 


## VVI : Margin Note: 
1. 
{
    width: 70%;
    margin: 0 auto;
}

=> By margin: auto in left right (above ): Browser first calculate the space avaliable in width and then it divides the remaining space equally as left and right margin so element comes in centre.

2. When we give margin then element  make seperation  either from parent of siblings both . if a div is inside a a div and give margin  to inner div to 20px then  it takes  seperation from  parent div . if gives margin negative value it comes outside of that parent div and takes that specified outside that parent div . 

3. margin-left: auto; is a CSS property that automatically sets the left margin of an element. When you use margin-left: auto;, it tells the browser to take up any remaining space on the left side of the element.  In summary, margin-left: auto; is used to push the element to the right by taking up all the available space on the left side.

## VVI: Default behaviour of block level elemnets in flexbox
=> Block level elements in flexbox behavave different than it is being  outside flexbox. In flexbox , child div or other block level elemnts takes only that much space required by its content intstead of full width .


=> inline-block : These elements like button streches in flex to take full availibale width if its width not restricted or given flex-grow:0 or wrap it in block element like div.

## Flex-item property:
1.flex-grow

=> Purpose: Controls how much a flex item should grow relative to the other flex items inside the same container when there is extra space available. It works on main axis .
Default Value: 0 (The item will not grow to fill the available space).
Behavior: When flex-grow is set to a positive value (e.g., 1), the flex item will grow to fill the available space in the container. If multiple items have a flex-grow value, they will grow relative to each other according to their flex-grow values.

2.flex-shrink:

=> Purpose: Controls how much a flex item should shrink relative to the other flex items inside the same container when there is not enough space.It works on main axis .
Default Value: 1 (The item will shrink if necessary).
Behavior: When flex-shrink is set to a positive value (e.g., 1), the flex item will shrink when the container is smaller than the combined size of the flex items. If multiple items have a flex-shrink value, they will shrink relative to each other according to their flex-shrink values.

3. to do grow and shrink in cross axis , use align-items:stretch  // to grow acroos cross axis. but no shrink property in css.
4.  
## note : VVI: 
=>flex-grow: Deals with how items expand in size when there's extra space in the container. Items with higher flex-grow values will take up more space.

=> flex-shrink: Deals with how items reduce in size when the container is too small. Items with higher flex-shrink values will shrink more.

EG: code: 
.container {
  display: flex;
  width: 100%;
}

.item-1 {
  flex-grow: 2;
  flex-shrink: 1;
  background-color: lightblue;
}

.item-2 {
  flex-grow: 1;
  flex-shrink: 1;
  background-color: lightgreen;
}

.item-3 {
  flex-grow: 1;
  flex-shrink: 2;
  background-color: lightcoral;
}

=> Item 1 will grow twice as much as Item 2 and Item 3 when there is extra space, but will shrink at the same rate as Item 2 when space is tight.
Item 2 will grow and shrink evenly compared to others.
Item 3 will grow like Item 2 but will shrink twice as much as Item 1 and Item 2.


## ####################   ####################       ####################    ####################    #################### 
<!--    TAILWIND CSS  -->

1. dist folder goes to production and we write our code to src .
2. when ever we apply property fpr state then we need to apply by "state: property"    eg: hover:text-white  hover:bg-red
3. tailwind follow mobile first Approach : so what ever wee write css that is good for mobile : 




## ############ Layout ##############  Topics:
 1. Aspect Ratio : ratio on width/height of an element:
=> aspect-auto:

a. aspect-ratio: auto;
The aspect ratio is determined automatically based on the intrinsic dimensions of the content.
aspect-square:

b. aspect-ratio: 1 / 1;
The element maintains a square aspect ratio where the width and height are equal.
aspect-video:

c. aspect-ratio: 16 / 9;
The element maintains a 16:9 aspect ratio, commonly used for videos and widescreen displays.


2. .conatiner

=> In Tailwind CSS, the container class is a utility that helps you create responsive designs by setting the maximum width of an element according to the current breakpoint. This behavior is particularly useful when you want your design to adapt to specific screen sizes, rather than adjusting fluidly to any viewport width.

Understanding the Container Class:
Responsive Design Based on Breakpoints:

a. Tailwind CSS has predefined breakpoints (like sm, md, lg, xl, and 2xl) that correspond to different screen sizes. The container class adjusts its max-width depending on the current active breakpoint.
For example, at the sm breakpoint, the max-width might be set to 640px. As the viewport size increases and crosses the md breakpoint, the max-width might increase to 768px, and so on.
This approach allows you to create designs that have fixed widths at certain breakpoints, making it easier to target specific screen sizes.
No Automatic Centering:

b. Unlike some other CSS frameworks (like Bootstrap), Tailwind's container class does not automatically center itself within its parent element.
If you want to center the container, you have to explicitly do so by adding mx-auto (which sets the left and right margins to auto) or another utility class like flex combined with justify-center if using a flexbox parent.
No Built-in Horizontal Padding:

c. Similarly, the container class does not include any built-in horizontal padding. In other frameworks, you might be used to containers having some padding by default, which ensures that the content inside the container doesn't touch the edges.
In Tailwind, if you want padding, you have to add it manually using utility classes like px-4 (padding-left and padding-right set to 1rem) or p-6 (padding on all sides set to 1.5rem), depending on your design needs.

code: <div class="container px-4 mx-auto">
  <!-- Your content here -->
</div>







<!-- NOt NEEDED TO  LEARN THIS , NEED TO HAVE IDEA ABOUT THIS: -->

<!-- Pligins -->

// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      // Customizations here
    },
  },
  plugins: [
    function ({ addUtilities }) {
      const newUtilities = {
        '.text-shadow': {
          textShadow: '2px 2px 4px rgba(0, 0, 0, 0.1)',
        },
        '.text-shadow-md': {
          textShadow: '3px 3px 6px rgba(0, 0, 0, 0.2)',
        },
        '.text-shadow-lg': {
          textShadow: '4px 4px 8px rgba(0, 0, 0, 0.3)',
        },
      }

      addUtilities(newUtilities, ['responsive', 'hover'])
    }
  ],
}


## Topic: linear gradient in css: (read from w3 school)
=> EG: background: linear-gradient(to right, rgba(255, 0, 0, 0.8), rgba(0, 0, 255, 0.5));   // to explain rgba function
=> rgba(255, 0, 0, 0.8): A semi-transparent red color (0.8 represents 80% opacity).
=> rgba(0, 0, 255, 0.5): A semi-transparent blue color (0.5 represents 50% opacity).

where opacity means background not visibility when opacity is 0 then fully tranparent I.e background elemnt is fully visible inspite of top element.

# 📌 Complete Guide to Flexbox (CSS Flexible Box Layout)

Flexbox is a powerful CSS layout model that provides efficient alignment, distribution, and responsiveness for UI components.

---

## 📖 1️⃣ Flexbox Basics

Flexbox organizes elements in a **single-directional flow**: **row** (horizontal) or **column** (vertical).

### **Key Terms**

- **Main Axis** → Defined by `flex-direction` (`row` or `column`)
- **Cross Axis** → Perpendicular to the main axis
- **Main Start/Main End** → Beginning and end of the main axis
- **Cross Start/Cross End** → Beginning and end of the cross axis

---

## 🎯 2️⃣ Flex Container (`display: flex`)

A **flex container** is created by applying `display: flex` to a parent element.

```css
.container {
  display: flex;
}
```

🔹 **By default**:

- The **main axis** is **left to right** (`row`).
- The **cross axis** is **top to bottom**.

---

## 🛠️ 3️⃣ Main Axis Control (`flex-direction`)

The `` property determines the direction of flex items.

| Value            | Main Axis Direction | Cross Axis Direction |
| ---------------- | ------------------- | -------------------- |
| `row` (default)  | Left → Right (↔)    | Top → Bottom (↕)     |
| `row-reverse`    | Right → Left (↔)    | Top → Bottom (↕)     |
| `column`         | Top → Bottom (↕)    | Left → Right (↔)     |
| `column-reverse` | Bottom → Top (↕)    | Left → Right (↔)     |

```css
.container {
  display: flex;
  flex-direction: column-reverse;
}
```

---

## 🎨 4️⃣ Spacing & Alignment

### ✅ **Justify Content (Main Axis)**

| Property                          | Effect                       |
| --------------------------------- | ---------------------------- |
| `justify-content: flex-start;`    | Items align to the start     |
| `justify-content: flex-end;`      | Items align to the end       |
| `justify-content: center;`        | Items align in the middle    |
| `justify-content: space-between;` | Items spread out             |
| `justify-content: space-around;`  | Equal space around each item |
| `justify-content: space-evenly;`  | Equal space between items    |

```css
.container {
  display: flex;
  justify-content: space-between;
}
```

### ✅ **Align Items & Align Content (Cross Axis)**

The `align-items` and `align-content` properties control alignment **along the cross-axis**, which can be adjusted to change the vertical or horizontal positioning of flex items.

#### **Align Items (Single Line Alignment)**
| Property                   | Effect                        |
| -------------------------- | ----------------------------- |
| `align-items: flex-start;` | Items align at the top        |
| `align-items: flex-end;`   | Items align at the bottom     |
| `align-items: center;`     | Items align in the middle     |
| `align-items: stretch;`    | Items stretch to fill  the spaces on cross axis        |
| `align-items: baseline;`   | Aligns items by text baseline |

```css
.container {
  display: flex;
  align-items: center;
}
```

#### **Align Content (Multiple Line Alignment)**
For wrapped content (`flex-wrap: wrap`), `align-content` determines how lines of flex items are positioned.

| Property                      | Effect                        |
| ----------------------------- | ----------------------------- |
| `align-content: flex-start;`  | Lines align at the top        |
| `align-content: flex-end;`    | Lines align at the bottom     |
| `align-content: center;`      | Lines align in the middle     |
| `align-content: stretch;`     | Lines stretch to fill space   |
| `align-content: space-between;` | Equal space between lines    |
| `align-content: space-around;`  | Equal space around lines     |

```css
.container {
  display: flex;
  flex-wrap: wrap;
  align-content: flex-end; /* Moves items towards the bottom */
}
```

🔹 **Cross Axis Direction Control:**
- By default, the cross-axis runs **top to bottom** for `row` or `row-reverse and **left to right** for `column` or `col-reverse`.
- Using `align-items: flex-end` or `align-content: flex-end`, you can **reverse the cross-axis appearance**, making items align **from bottom to top**. for `row , row-reverse`
- Similarly, with `col and col-reverse`, `align-items: flex-start` can **push items to the right** instead of the left.

---

## 🔄 5️⃣ Flex Items Control

### ``** (Handling Overflow)**

| Value              | Effect                      |
| ------------------ | --------------------------- |
| `nowrap` (default) | Items stay in one row       |
| `wrap`             | Items wrap to new rows  in the direction of cross axis   |
| `wrap-reverse`     | Items wrap in reverse direction of cross axis |

```css
.container {
  display: flex;
  flex-wrap: wrap;
}
```

### ``** (Shorthand for Grow, Shrink, Basis)**

```css
.item {
  flex: 1; /* Equal growth for all items */
}
```

### ``** (Item Positioning)**

```css
.item:nth-child(2) {
  order: -1; /* Moves before other items */
}
```

### ``** (Per-Item Cross Axis Alignment)**

```css
.item {
  align-self: flex-end;
}
```

---

## 🎯 6️⃣ Common Flexbox Layout Examples

### ✅ **Centering a Box**

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
```

### ✅ **Equal-Width Columns**

```css
.container {
  display: flex;
}
.item {
  flex: 1;
}
```

### ✅ **Sidebar + Content Layout**

```css
.container {
  display: flex;
}
.sidebar {
  flex: 1;
}
.content {
  flex: 3;
}
```

---

## 📌 **Flexbox Cheatsheet Summary**

| **Property**      | **Main Axis?** | **Cross Axis?** | **Effect**                           |
| ----------------- | -------------- | --------------- | ------------------------------------ |
| `display: flex;`  | ✅              | ✅               | Enables Flexbox                      |
| `flex-direction`  | ✅              | ❌               | Sets row/column direction            |
| `justify-content` | ✅              | ❌               | Aligns items along the main axis     |
| `align-items`     | ❌              | ✅               | Aligns items along the cross axis    |
| `align-content`   | ❌              | ✅               | Aligns multiple rows                 |
| `flex-wrap`       | ❌              | ✅               | Controls wrapping of items           |
| `flex`            | ✅              | ❌               | Sets size and growth/shrink behavior |
| `order`           | ❌              | ✅               | Reorders items in the layout         |
| `align-self`      | ❌              | ✅               | Customizes alignment per item        |

---

## 🚀 **Final Thoughts**

Flexbox is **powerful**, **responsive**, and **widely used** in modern web design. Mastering it allows you to build flexible and adaptable UI layouts effortlessly.

🔹 **Need help implementing Flexbox?** Feel free to ask! 🚀




## # CSS Grid Properties

CSS Grid is a powerful layout system in CSS, allowing you to design responsive and complex layouts. Below is a list of key properties used to define and manage 
grid containers and grid items.

## 1. **Grid Container Properties**

These properties are applied to the **grid container** (the parent element that holds the grid items).

### 1.1 **`display: grid`**
- Defines an element as a grid container, enabling grid behavior for its children.
- **Example**: `display: grid;`

### 1.2 **`grid-template-columns`**
- Defines the number of **columns** in the grid and their respective sizes.
- **Syntax**: `grid-template-columns: <size1> <size2> ... <sizeN>;`
- **Example**: `grid-template-columns: 100px 200px 1fr;` (Creates 3 columns of 100px, 200px, and flexible size).

### 1.3 **`grid-template-rows`**
- Defines the number of **rows** in the grid and their respective sizes.
- **Syntax**: `grid-template-rows: <size1> <size2> ... <sizeN>;`
- **Example**: `grid-template-rows: 50px auto 200px;` (Creates 3 rows with specific heights).

### 1.4 **`grid-template-areas`**
- Defines a **layout template** with named grid areas.
- **Syntax**: `grid-template-areas: "area1 area2" "area3 area4";`
- **Example**:
  ```css
  grid-template-areas: 
      "header header header"
      "sidebar main main"
      "footer footer footer";



# CSS Grid Properties

CSS Grid is a powerful layout system in CSS that helps in creating complex, flexible, and responsive layouts. Below are the essential CSS Grid properties explained in detail.

## 1. **Grid Container Properties**

These properties are applied to the **grid container** (the parent element that holds the grid items).

### 1.5 **`gap` (previously `grid-gap`)**
- Defines the **spacing (gaps)** between grid rows and columns.
- **Syntax**: `gap: <row-gap> <column-gap>;`
- **Example**: `gap: 10px 20px;` (Creates a 10px gap between rows and a 20px gap between columns).

### 1.6 **`grid-auto-columns`**
- Specifies the size of **auto-generated columns** when there are more items than defined columns.
- **Syntax**: `grid-auto-columns: <size>;`
- **Example**: `grid-auto-columns: 100px;` (Auto-generated columns will have a size of 100px).

### 1.7 **`grid-auto-rows`**
- Specifies the size of **auto-generated rows** when there are more items than defined rows.
- **Syntax**: `grid-auto-rows: <size>;`
- **Example**: `grid-auto-rows: 150px;` (Auto-generated rows will have a size of 150px).

### 1.8 **`grid-auto-flow`**
- Controls how the auto-placed items are positioned in the grid. You can specify `row`, `column`, `dense`, or a combination of these.
- **Syntax**: `grid-auto-flow: <value>;`
- **Example**: `grid-auto-flow: row dense;` (Items will fill the grid in rows, and it will be dense, meaning it will try to fill in gaps if items are smaller).

## 2. **Grid Item Properties**

These properties are applied to **grid items** (the children of the grid container).

### 2.1 **`grid-column`**
- Specifies the **horizontal** position of a grid item. Defines where an item should start and end across columns.
- **Syntax**: `grid-column: <start-line> / <end-line>;` or `grid-column: span <n>;`
- **Example**: `grid-column: 1 / 3;` (Starts at column 1, ends at column 3).
- **Example**: `grid-column: span 2;` (Spans 2 columns).

### 2.2 **`grid-row`**
- Specifies the **vertical** position of a grid item. Defines where an item should start and end across rows.
- **Syntax**: `grid-row: <start-line> / <end-line>;` or `grid-row: span <n>;`
- **Example**: `grid-row: 1 / 3;` (Starts at row 1, ends at row 3).
- **Example**: `grid-row: span 2;` (Spans 2 rows).

### 2.3 **`grid-area`**
- A shorthand property for setting **`grid-column`** and **`grid-row`** properties at once. You can also use it with named grid areas.
- **Syntax**: `grid-area: <row-start> / <column-start> / <row-end> / <column-end>;`
- **Example**: `grid-area: 1 / 1 / 3 / 3;` (Spans from row 1, column 1 to row 3, column 3).

### 2.4 **`justify-self`**
- Aligns the grid item **horizontally** within its grid cell.
- **Syntax**: `justify-self: <start|end|center|stretch>;`
- **Example**: `justify-self: center;` (Aligns the grid item to the center horizontally).

### 2.5 **`align-self`**
- Aligns the grid item **vertically** within its grid cell.
- **Syntax**: `align-self: <start|end|center|stretch>;`
- **Example**: `align-self: start;` (Aligns the grid item to the start vertically).

### 2.6 **`place-self`**
- A shorthand for **`align-self`** and **`justify-self`**. Aligns the item both horizontally and vertically.
- **Syntax**: `place-self: <align-self> <justify-self>;`
- **Example**: `place-self: center center;` (Aligns the grid item both horizontally and vertically in the center).

## 3. **Advanced Grid Features**

### 3.1 **`minmax()`**
- Defines a **range of sizes** for a grid column or row, with a minimum and maximum value.
- **Syntax**: `minmax(<min>, <max>)`
- **Example**: `grid-template-columns: minmax(100px, 1fr);` (Columns can be at least 100px wide but will expand up to 1 fraction of available space).

### 3.2 **`repeat()`**
- Repeats a column or row pattern a specific number of times or indefinitely.
- **Syntax**: `repeat(<count>, <size>)`
- **Example**: `grid-template-columns: repeat(3, 1fr);` (Creates 3 columns of equal size).

### 3.3 **`auto-fill` and `auto-fit`**
- **`auto-fill`**: Fills the grid with as many items as possible.
- **`auto-fit`**: Similar to `auto-fill`, but the items will stretch to fill the available space.
- **Example**: `grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));`

### 3.4 **`min-content`, `max-content`, `auto`**
- These are special **keyword values** that can be used to define flexible sizing for columns and rows:
  - `min-content`: Takes the **minimum size** of the content.
  - `max-content`: Takes the **maximum size** of the content.
  - `auto`: Uses the default sizing behavior of the content.
- **Example**: `grid-template-columns: min-content 1fr max-content;`

## 4. **Responsive Grid Layout**

### 4.1 **Using Media Queries with Grid**
You can create **responsive layouts** by changing grid configurations based on the viewport size with **media queries**.
- **Example**:
  ```css
  .grid-container {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
  }

  @media (max-width: 768px) {
      .grid-container {
          grid-template-columns: 1fr 1fr;
      }
  }

  @media (max-width: 480px) {
      .grid-container {
          grid-template-columns: 1fr;
      }
  }


# 🧾 HTML Elements Cheat Sheet

This document lists common HTML elements, grouped by their **display type** and **usage**.

---

## 🧱 1. Block-Level Elements

Block-level elements start on a new line and take up the full width available.

| Element         | Description              |
|-----------------|--------------------------|
| `<div>`         | Generic container        |
| `<p>`           | Paragraph                |
| `<h1>`–`<h6>`   | Headings (H1 to H6)      |
| `<section>`     | Section of a document    |
| `<article>`     | Independent content      |
| `<header>`      | Introductory content     |
| `<footer>`      | Footer content           |
| `<nav>`         | Navigation links         |
| `<aside>`       | Sidebar / related info   |
| `<form>`        | HTML form                |
| `<table>`       | Table                    |
| `<ul>`          | Unordered list           |
| `<ol>`          | Ordered list             |
| `<li>`          | List item                |
| `<main>`        | Main document content    |
| `<hr>`          | Horizontal line          |
| `<figure>`      | Image or diagram block   |
| `<figcaption>`  | Caption for a figure     |

---

## 🧷 2. Inline Elements

Inline elements do not start on a new line and take up only as much width as necessary.

| Element       | Description                  |
|---------------|------------------------------|
| `<span>`      | Generic inline container     |
| `<a>`         | Hyperlink                    |
| `<strong>`    | Important text (bold)        |
| `<em>`        | Emphasized text (italic)     |
| `<b>`         | Bold (non-semantic)          |
| `<i>`         | Italic (non-semantic)        |
| `<u>`         | Underlined text              |
| `<img>`       | Image                        |
| `<label>`     | Form field label             |
| `<abbr>`      | Abbreviation                 |
| `<code>`      | Code snippet                 |
| `<br>`        | Line break                   |
| `<input>`     | Form input                   |
| `<select>`    | Dropdown menu                |
| `<textarea>`  | Text input area              |

---

## 🧩 3. Inline-Block Elements (by default)

These elements behave like inline elements but allow setting width and height.

| Element     | Description     |
|-------------|-----------------|
| `<input>`   | Input field     |
| `<img>`     | Image           |
| `<button>`  | Button          |
| `<select>`  | Dropdown        |

---

## ⚙️ 4. Metadata & Other Elements

| Element       | Description                      |
|---------------|----------------------------------|
| `<script>`    | Embeds JavaScript                |
| `<style>`     | CSS styles                       |
| `<link>`      | External resources (like CSS)    |
| `<meta>`      | Metadata about the document      |
| `<title>`     | Document title (in browser tab)  |

---

> 💡 **Tip:** You can change the default display behavior using CSS (e.g., `display: block;` or `display: inline-block;`).


