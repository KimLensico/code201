# HTML Images; CSS Color & Text

## HTML IMAGES
- img - what you need to use an image
    - src - tells the browser where to find the image file. usually a relative url pointing to an image on your own site
- alt - provides text descriptionof the images which describes the image if you cannot see it 
- title provide additional information about the image. most browsers provide this in a tootip when the user hovers over an image 

### Where to place images in your code: 
1. before a paragraph
2. inside inside the start of a paragraph
3. in the middle of a paragraph

**Block elements always appear on a new line** (such as h1, p, etc)

**inline elements sit within a block level elent and do no start on a new line.**

If the ```<img>``` element is inside a block level element, any text or other inline element will flow around the image as shown in the second and third examples. 

```align``` is an old code not used by HTML5 but may still be used in old browsers. 

### Three rules for creating images
1. Save images in the right format jpeg, gif, png)
2. Save images at the right size  that it would appear on the website or else it might be distorted.
3. Use the correct resolution. Saving images at a higher resolution results in images that are larger than necessary to download

## HTML COLORS
- foreground color - the color of text inside an element.
- the three ways you can input the color are:
    1. hex
    2. rgb
    3. typing out the name of the color 
- background color - sets of background color of a box
- there are properties to control the choice of font, size, weight, style, and spacing
- there is a limit choice of fonts that most people will have installed 
    - if you want to use a wider range of typefacex there are several options but you need the right license to use them 
- you can control the space between lines of text, individual letters, and words. text can also be ligned in the left, right, center, or justified. 
    - can also be indented
- use psuedo-classes (:) to change the style of an element whe na user hovers over or clickes on text or when the have visited a link.

### Leading ("ledding") 
Leading is a term typographers use for the vertical space between lines of text. In a typeface, the part of a letter that drops beneath the baseline is called a **descender**, while the highest point of a letter is called the **ascender**. Leading is measured from the bottom of the descender on one line to the top of the ascender on the next.

ex: 
```p {```
```line-height: 1.4em;}```

Increasing the line-height makes the vertical gap between lines of text larger.

### :hover
This is applied when a user hovers over an element with a pointing device such as a mouse. This has commonly been used to change the appearance of links and buttons when a user places their cursor over them. It is worth noting that such events do not work on devices that use touch screens because the screen is not able to tell when someone is hovering their finger over an element.

### :active
This is applied when an element is being activated by a user; for example, when a button is being pressed or a link being clicked. Sometimes this is used to make a button or link feel more like it is being pressed by changing the style or position of the element slightly.

## :focus
This is applied when an element has focus. Any element that you can interact with, such as a link you can click on or any form control can have focus.

more selectors:

SELECTORS | MEANING
|--------------|-----------|
|Existence | ```[]``` Matches a specific attribute (whatever its value) ex: ```p[class]```|
|Equality | ```[=]``` Matches a specific attribute with a specific value ex: ```p[class="dog"]```|
|Space | ```[~=]``` Matches a specific attribute whose value appears in a space-separated list of words|
|Prefix | ```[~=]``` Matches a specific attribute whose value begins with a specific string |
|SubString | ```[*=]``` Matches a specific attribute whose value contains a specific substring |
|Suffix | ```[$=]``` Matches a specific attribute whose value ends with a specific string |


[<===](README.md)