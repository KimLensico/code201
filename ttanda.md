# CSS: Transform, Transition, + Animations

## Transform Syntax
- The value specifies the transform type followed by a specific amount inside parentheses
-  transform property includes multiple vendor prefixes to gain the best support across all browsers
- un-prefixed declaration comes last to overwrite the prefixed versions, should a browser fully support the transform property

- use the transform element to rotate up to 360 degrees 

```
.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
```

- use the scale to change the appeared size of the element. the default scale is 1 (original size)

```
.box-1 {
  transform: scale(.75);
}
.box-2 {
  transform: scale(1.25);
}
``` 

- perspective can be thought of as a vanishing point. similar to 3D drawings.
    - element can be set in two different ways
        - useing the perspective value within the transform property on individual elements
        - the other insludes using the perspective property on the parent element residing over child elements being transformed
        - perspective value can be set as none or a length measurement
            - The none value turns off any perspective, while the length value will set the depth of the perspective. 
            - The higher the value, the further away the perspective appears, thus creating a fairly low intensity perspective and a small three-dimensional change. 
            - The lower the value the closer the perspective appears, thus creating a high intensity perspective and a large three-dimensional change.

```
.box-1 {
  transform: perspective(100px) rotateX(45deg);
}
.box-2 {
  transform: perspective(1000px) rotateX(45deg);
}
```

## Transitions

-  for a transition to take place, an element must have a change in state, and different styles must be identified for each state. 
    - The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.

There are four transition related properties:
- total
- including transition-property
- transition-duration
- transition-timing-function
- transition-delay

*Not all of these are required to build a transition, with the first three are the most popular.*

## Animations

### Animation Keyframes
To set multiple points at which an element should undergo a transition, use the @keyframes rule. The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.

### Vendor Prefixing the Keyframe Rule
The @keyframes rule must be vendor prefixed, just like all of the other transition and animation properties. 

### Animation Name
Once the keyframes for an animation have been declared they need to be assigned to an element. 
    - To do so, the animation-name property is used with the animation name
        - identified from the @keyframes rule, as the property value. 
    - The animation-name declaration is applied to the element in which the animation is to be applied to.

### Animation Duration, Timing Function, & Delay
Once you have declared the animation-name property on an element, animations behave similarly to transitions. 
- They include a duration, timing function, and delay if desired. 
- To start, animations need a duration declared using the animation-duration property.
    - As with transitions, the duration may be set in seconds or milliseconds.

### Customizing Animations
Animations also provide the ability to further customize an element’s behavior 
- including the ability to declare the number of times an animation runs
    - as well as the direction in which an animation completes.

for more content: [see here](https://learn.shayhowe.com/advanced-html-css/css-transforms/)


**[🠴 RETURN](README.md)**