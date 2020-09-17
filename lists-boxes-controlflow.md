# HTML Lists, CSS Boxes, + JavaScript Control Flow

## Types of Lists
- ordered lists - numbered list
- unordered lists - bullet points
- definition lists - set of terms along with the definitions for each of those terms.
    - ```<dl></dl>``` = "heading" kind of like a box to put the terms and definitions in
    - ```<dt></dt>``` = term being defined
    - ```<dd></dd>``` = contains the definition 

    lists can be nested inside one another

## CSS boxes
- min-width/height - specifies the smallest size a box can stretch when a browser is narrow
- max-width/height - specifies the max size a box can stretch when a browser is wide
- overflow - tells the browser what to do if the content in the box is bigger than the box. it can have two values:
    - hidden - hides extra content that does not fit in the box
    - scroll - adds a scrollbar so people can see the missin item 
**include a !DOCTYPE declaration so IE6 will format things correctly**

## JavaScript Control Flow
**ARRAYS**
    - create an array like creating any variabe (var arrayName) 
    - values are assigned within the square brackets
    - each separated by a comma
    - values do not need to be the same data type
        - you can store a string, a boolean, a number - ALL in the SAME array
**ARRAY TECHNIQUES**
- array literal - method for creating an array
- array constructor - usere the new keyway

colors = ['white'
          'black'
          'custom'];

**SWITCH STATEMENTS**
    - starts with a variable called the ```switch value```
    - each case indicates a possible value for the variable AND the code that should run if the variable matches that value 
    - ```break``` - tells JS to move on to the next code after the one it's in

**TYPE COERCION + WEAK TYPING**
- type coercion - when JS converts data types behind the scenes to complete an operation 
    - can lead to unexpected values in your code and also cause errors
- weak typing - what JS uses because the data type for a value can change 
- strong typing - other language require specifications on what data type each variable should be
due to type coercion, every value in JavaScript can be treated as if it were true or false
- falsy - treated as IF the were false
    - can also be treated as the number 0
- truthy - as IF the values were true
    - as long as it's not falsy it can be treated as true
the presence of an object or an array is usually considered truthy too
- common when checking for the presence of an element on a page

*refer to loop notes in code 102 read-me*

**[🠴 RETURN](README.md)**