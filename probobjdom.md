# Problem Domain, Objects, + the DOM

## Objects
Objects gorup together a set of variables and functions to create a model of a something yyou would recognize from the real world. In n object, variables and functions take on new names. 
- in an object: 
    - variables become known as *properties* 
        - tells us about the object 
    - functions become known as *methods* 
        - represent tasks that are associated with the object 
            - the value of a method is always a function. 
    - named functions are known as *keys*
        - an object cannot have two keys at the same name
            - this is because keys are used to access their corresponding values
    - the value of a property can be a string, number, Boolean, array, or even another object. 

### Creating an object: Literal notation
literal notation is the easiest and most popular wat ocreate objects - there are several was to create objects
- the object is the curtly braces and their contents 
- separate each key from its value using a colon
- separate each property and method with a comma 
    - not after the last value 
- when setting properties, treat the values like you would do for variables:
    - strings in live in quotes and arrays live in square brackets

### Accessing an object and dot notation 
Literal notation as the easiest and most popular wat to create objects. 
- you can access the properties or methods of an object using dot notation. 
- you can also use properties using square brackets
- to access a property: you use *dot notation*
    - use the name of the object
    - follow the object by a period
    - name the propert or method you want to access 
- the period is known as the *member operator*
    - the property or method on its right is a member of the object on its left 
- you can also access the properties of an object - BUT NOT ITS METHODS - using *square bracket syntax*
    - the object name is followed by square brackets, and the property name is inside them
    - most commonly used when:
        - the name or property is a number (technically allowed but should generally be avoided)
        - a variable is being used in place of the property name (you will see this techniwue used in chapter 12)
        
## Document Object Model

#### SUMMARY: (IN CASE YOU'RE TRYING TO SKIM FOR MORE INFO) 
- The browser represents the page using a DOM tree.
- DOM trees have four types of nodes: document nodes, element nodes, attribute nodes, and text nodes.
- you can select element nodes by their id or class attributes, by tag name, or using CSS selector syntax.
- whenever a DOM query can return more than one node, it will always return a Nadelist
- from an element node, you can access and update its content using properties such as textContent and innerHTML or using DOM manipulation techniques.
- an element node can contain multiple text nodes 
    - child elements that are siblings of each other
- browsers offer tools for viewing the DOM tree . 

- the Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the
contents of a web page while it is in the browser window.
    - the *DOM* is neither part of HTML, nor part of JavaScript; it is a separate set of rules.
        - it is implemented by all major browser makers, and covers two primary areas:

### Making a Model of the HTML Page 
When the browser loads a web page, it creates a model of the page in memory.
 - the DOM specifies the way in which the browser should structure this model using a *DOM tree*.
 - The DOM is called an *object model*
    - the model (the DOM tree) is made of objects.
- each object represents a different part of the page loaded in the browser window

### Accessing and Changing the HTML Page
the DOM also defines methods and properties to access and update each object in this model 
    - which in turn updates what the user sees in the browser.
- you will hear people call the DOM an *Application Programming Interface (API)*
    - user interfaces let humans interact with programs
    - APls let programs (and scripts) talk to each other
    -the DOM states what your script can "ask the browser about the current page
        - how to tell the browser to update what is being shown to the user. 

### The Dom Tree is a Model of a Web Page
as a browser loads a web page, it creates a model of that page
- the model is called a *DOM tree*
    - it is stored in the browsers' memory.
    - it consists of four main types of nodes:
        - DOCUMENT NODE :
            - every element, attribute, and piece of text in the HTML is represented by its own DOM node
            - at the top of the tree a document node is added
                - it represents the entire page 
                    - also corresponds to the document object
                when you access any element, attribute, or text node, you navigate to it via the document node
                - it is the starting point for all visits to the DOM tree. 
        - ELEMENT NODE :
            - HTML elements describe the structure of an HTML page. 
                - (The <h l > - <h6> elements describe whatparts are headings,
                - the <p> tags indicate where paragraphs of text start and finish, etc
            - to access the DOM tree, you start by looking for elements
            - once you find the element you want, you can access its text and attribute nodes if you  want to
            - this is why you start by learning methods that allow you to access element nodes, before learning to access and alter text or attributes. 
        - ATTRIBUTE NODES
            - the opening tags of HTML elements can carry attributes 
                - these are represented by attribute nodes in the DOM tree
            - attribute nodes are not children of the element that carries them
                - they are *part of that element* 
                - once you access an element, there are specific JavaScript methods and properties to read or change that element's attributes.
                    - for example, it is common to change the values of cl ass attributes to trigger new  CSS rules that affect their presentation. 
        - TEXT NODES
            - once you have accessed an element node, you can then reach the text within that element
            - this is stored in its own *text node* 
            - text nodes cannot have children 
            - if an element contains text and another child element:
                - the child element is not a child of the text node but rather a child of the containing element.

                
[<==back](README.md)