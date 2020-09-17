# Forms + JS Events

The term _form_ has referred to a print docyent that contains spaces for you to fill in informaton
- HTML borrows the concept of a form to refer to different elements that allow you to collect information from visitors to your site

## Why Forms
In addition to enabling users to search, forms also allow users to perform other functions online
    - You will see forms when registering as a member of a website, when shopping online, and when signing up for newsletters or mailing lists.

## Form Controls
There are several types of form controls that you can use to collect information from visitors to your site:

### ADDING TEXT
- Text input (single-line)
    - Used for a single line of text such as email addresses and names.
- Password input 
    - Like a single line text box but it masks the characters entered.
- Text area (multi-line)
    - For longer areas of text, such as messages and comments

### MAKING CHOICES
- Radio buttons
    - For use when a user must select one of a number of options.
- Checkboxes
    -When a user can select and unselect one or more options.
- Drop-down Boxes
    - When a user must pick one of a number of options from a list.

### SUBMITTING FORMS
- Submit buttons
    - To submit data from your form to another web page.
- Image buttons
    - Similar to submit buttons but they allow you to use an image.

### Uploading Files
- File upload
    - Allows users to upload files (e.g. images) to a website.

## Form Structure
- ```<form>``` - the element form controls live inside 
    - This element should always carry the action attribute
        - Will usually have a method and id attribute too.
- ```action``` - Every ```<form>``` element requires an ```action``` attribute
    - Its value is the URL for the page on the server that will receive the information in the form when it is submitted.
- ```method``` - Forms can be sent using one of two methods: 
    - ```get```
        - the values from the form are added to the end of the URL specified in the action attribute. 
        - ideal for:
            - short forms (such as search boxes)
            - when you are just retrieving data from the web server
                - not sending information that should be added to or deleted from a database 
    ```post```
        - the values are sent in what are known as HTTP headers
        - rule of thumb you should use the post method if your form:
            - allows users to upload a file
            - is very long
            - contains sensitive data (ex; passwords)
            - adds information to, or deletes information from, a database

_If the method attribute is not used, the form data will be sent using the ```get``` method_

## List, Tables and Forms
- In addition to the CSS properties covered in other chapters which work with the contents of all elements, there are several others that are specifically used to control the appearance of lists, tables, and forms.
- List markers can be given different appearances
using the ```list-style-type``` and ```list-style``` image
properties.
- Table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent.
- Forms are easier to use if the form controls are vertically aligned using CSS.
- Forms benefit from styles that make them feel more interactive.

## Events
- Events are the browser's way of indicating when something has happened (such as when a page has finished loading or a button has been clicked).
- Binding is the process of stating which event you are waiting to happen, and which element you are waiting for that event to happen upon.
- When an event occurs on an element, it can trigger a JavaScript function. When this function then changes the web page in some way, it feels interactive because it has responded to the user.
- You can use event delegation to monitor for events that happen on all of the children of an element.
- The most commonly used events are W3C DOM events, although there are others in the HTMLS specification as well as browser-specific events. 

*see chapter 6 in the js book for specifics*

**[🠴 RETURN](README.md)**