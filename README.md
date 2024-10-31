# background-images
 
These examples illustrate how to work with background images in CSS. 

## Background property 
The background property covers the following areas: 
- background color - sets the 
- background image 
- background position
- background attachment 
- background size

All of these properties accept multiple values. This allows you to layer images and gradients, and set the size, postition, and attachement for each. 

Use `background` like this: 

```CSS
background-image:
  background-image: 
    url(images/picture-0.png),
    url(images/picture-1.png),
    url(images/picture-2.png),
    url(images/picture-3.png),
    linear-gradient(red, blue),
    url(images/picture-4.png)
```

Here we've layered 6 background "images", notice there is a gradient sandwiched between picture-3 and picture-4. 

Picture-0 will be on top (in front) and picture-4 will be on the bottom (in back).

https://developer.mozilla.org/en-US/docs/Web/CSS/background-image

Use `background-size` to set the size of an image. This also applies to gradients! Fo example: 

```CSS
background-size: 400px, 300px, 200px, 100px, auto, 50px;
```

Each of the values is seprated by a comma, and are applied to each of the images in the same order! picture-0 is 400px, picture-1 is 300px, etc. Notice the gradient is set to `auto` this makes the gradient use its default or original size. 

https://developer.mozilla.org/en-US/docs/Web/CSS/background-size

`background-repeat` works the same. Values can be:
- repeat
- no-repeat
- repeat-x
- repeat-y
- space
- round
- or a combination of these. 

For example: 

```CSS
background-repeat: no-repeat, no-repeat, no-repeat, no-repeat, no-repeat, repeat;
```

Again the values are applied in order! So first 5 images are `no-repeat` and the last image (picture-4) is `repeat`.

https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat

`background-position` determines the position of the image. you can use unit values like 120px and 50%, or keyword values like: left, right, top, bottom, and center. **You can also mix these!** 

Here is an example, again the values are applied to the images in same order. Notice that each value is separqated by a comma. 

```CSS
background-position: left top, right 20px top 50px, right bottom, left bottom, center, center;
```

Notice the first value: `left top`. This aligns the left edge of the image with the left of the container, and the top edge with the top of the container. You can use `left`, `top`, `right`, or `bottom`. 

You can combine keywords with unit values to create an offset. Notice the second value: `right 20px top 50px`. Here the image would be placed 20px to the right of the right edge, and 50px down from the top. 

https://developer.mozilla.org/en-US/docs/Web/CSS/background-position

`background-attachment` is used to determine if the image is fixed to the viewport or scrolls with the containing block. 

Values can be:
- fixed
- scroll
- local 

The values apply to the images in same order, and are comma separated, for example: 

```CSS
background-attachment: scroll, scroll, scroll, scroll, scroll, fixed;
```

In this case the first 5 images are `scroll` and image 6 (picture-4) is fixed. 

https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment


