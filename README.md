# Background Images in CSS

This guide explains how to use background images in CSS.

## Background Property

The [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background) property in CSS includes:

- **[Background color](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)** – sets the background color.
- **[Background image](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image)** – sets one or more background images.
- **[Background position](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position)** – defines image positioning.
- **[Background attachment](https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment)** – controls image scrolling.
- **[Background size](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size)** – sets image dimensions.

Each property accepts multiple values, allowing layered images and gradients with customized sizes, positions, and attachments.

**Example:**

```css
background-image: 
    url(images/picture-0.png),
    url(images/picture-1.png),
    url(images/picture-2.png),
    url(images/picture-3.png),
    linear-gradient(red, blue),
    url(images/picture-4.png);
```

In this example, six background layers are defined, with a gradient positioned between `picture-3` and `picture-4`. Images are layered from top (`picture-0`) to bottom (`picture-4`).

## Background Size

[`background-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size) controls the size of each background layer, including gradients. Sizes are set in the order of the images:

```css
background-size: 400px, 300px, 200px, 100px, auto, 50px;
```

Here, `picture-0` is set to 400px, `picture-1` to 300px, and so on. The gradient uses `auto`, its default size.

## Background Repeat

The [`background-repeat`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat) property specifies how images are repeated. Possible values include:

- `repeat` – repeats the image in both directions.
- `no-repeat` – displays the image once without repetition.
- `repeat-x` – repeats the image horizontally.
- `repeat-y` – repeats the image vertically.
- `space` – repeats the image to fill the area with even spacing between copies.
- `round` – repeats the image with resizing to fill the area without gaps.

**Example:**

```css
background-repeat: no-repeat, no-repeat, no-repeat, no-repeat, no-repeat, repeat;
```

In this example, each image repeats based on its specified value.

## Background Position

The [`background-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position) property sets each image's position, using units like `120px` or `50%`, or keywords like `left`, `right`, `top`, `bottom`, and `center`.

**Position Values:**

- `left`, `right`, `top`, `bottom`, `center` – aligns the image relative to the container’s edges.
  - **Offset Values** – You can combine keywords with offsets to position images with more precision. For example, `background-position: left 30px top 50px` places the image 30px to the right of the left edge and 50px below the top edge.

**Example:**

```css
background-position: left top, right 20px top 50px, right bottom, left bottom, center, center;
```

Each position value aligns with the respective image, allowing precise placement within the container.

## Background Attachment

[`background-attachment`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment) defines whether the background image is fixed to the viewport or scrolls with the content.

- `fixed` – fixes the background image in place; it won’t scroll with the content.
- `scroll` – scrolls the background image along with the content.
- `local` – scrolls the background image within the element it’s applied to, behaving as if it’s “pinned” within that element.

**Example:**

```css
background-attachment: scroll, scroll, scroll, scroll, scroll, fixed;
```

Here, the final image remains fixed while others scroll with the content.

## CSS Gradients

CSS gradients are background images created with color transitions. Types include:

- **[Linear gradient](https://developer.mozilla.org/en-US/docs/Web/CSS/linear-gradient)** – transitions colors in a straight line.
  ```css
  background-image: linear-gradient(red, blue);
  ```
- **[Radial gradient](https://developer.mozilla.org/en-US/docs/Web/CSS/radial-gradient)** – transitions colors outward from a central point.
  ```css
  background-image: radial-gradient(circle, red, blue);
  ```

Gradients can blend with images and use properties like `background-size` and `background-position` for added control.

### Using Spread Percentages in Gradients

You can control color distribution in gradients using spread percentages, specifying how much space each color occupies.

**Example of Linear Gradient with Spread Percentages:**

```css
background-image: linear-gradient(to right, red 20%, yellow 40%, green 60%, blue 100%);
```

In this example:
- Red occupies the first 20% of the gradient.
- Yellow appears from 20% to 40%.
- Green fills from 40% to 60%.
- Blue covers the rest up to 100%.

**Example of Radial Gradient with Spread Percentages:**

```css
background-image: radial-gradient(circle, red 20%, yellow 40%, green 60%, blue 100%);
```

In this radial gradient, colors spread outward in the same pattern as the linear gradient but radiate from the center, creating a layered circular effect.

## CSS Color Values

CSS offers several ways to define color values:

- **[Named Colors](https://developer.mozilla.org/en-US/docs/Web/CSS/named-color)** `tomato`
- **[Hexadecimal](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#Hex_colors)** – `#FF5733`
- **[RGB/RGBA](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#RGB_colors)** – `rgb(255, 87, 51)` or `rgba(255, 87, 51, 0.5)` (with opacity)
- **[HSL/HSLA](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value#HSL_colors)** – `hsl(60, 90%, 50%)` or `hsla(10, 100%, 50%, 0.5)`

These formats provide flexibility, with RGBA and HSLA allowing transparency.

You can use these color formats anywhere a color is expected in CSS. 

## CSS is Awesome
- https://css-tricks.com/css-is-awesome/
- https://blog.jim-nielsen.com/2021/css-is-in-fact-awesome/