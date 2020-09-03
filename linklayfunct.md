# HTML Links, CSS Layouts, JavaScript Functions 
## HTML

- ```<a>``` is the element used for links
    - has an href attribute is where you want to go to when they click the link
- ```<a> link text </a>``` - where the link is
- example: ```<a href=link.here> text </a>```

**absolute url** - the value of the href attribute will be the full web address for the site
    - url = *uniform resource locator*. the address typed in a browser for a specific page. if no page is specific, it will go to the homepage

**relative url** - shorthand version of a website when you don't need to specify the domain name. 
- if all pages of the site are in the same folder, the href attribute is just the name of the file.
- if you have different pages of a site in different folders then you use a sightly more complex syntax to indicate where the page is in relation to the current page 
- ```index.html``` contains links that use relative urls.
- you can create links between pages without having to setup your domain name or hosting. 

### Directory Structure 
Every page and image on a site has a url. the url is made up of the domain name followed by the **path** to that page or image.

You use urls when linked to other web pages and when including images in your own site. 

**Structure**
- **root** folder - contains all other files and folders or a website. contains:
    - ... the ```index.html``` which is the homepage
    - ... individual folders
- each section of the site is places in a separate folder.

**Relationships**
- the relationship between files and folderson a website is described using the same terminology as a family tree

**Homepages**
- ```index.html``` the main homepages of a site written in HTML /and the homepages of each section in a child folder/
- usually set up to return the ```index.html``` if no file is specified.

- content management systems, blogging softwares, e-commerce systems might not have individual files for each website. 
    - these systems often use one template filefor each different type of page 
    - editing the template file would change all of the pages that use the template
    - *DO NOT* change any code that is not HTML or you may break the page 

### Relative URLs
Relative urls can be used when thinking to pages within your own website. they provide a shorthand way of telling the browser where to find your files. 
- because the domain name does not have to be repeated, they are quicker to write
- if all the files in you site are in one folder, you use the file name for the page
- if your site is organized into separate folders/directories you need to tell the browser how to get from the page it is CURRENTLY ON to the page you are LINKING TO.
- if you link the same page from two different pages, you might, therefore, need to write two different relative urls. 

### Relaive Link Types
- same folder - to link a file in the same folder just use the file name
- child folder - use the name of a child folder followed by a forward slash, then file name 
    - ex: ```<a href="main/child-folder.html">```
- grandchild folder - like the child folder but add another forward slash and is placed after the child folder
- parent folder - use ../ to indicate the folder about the current one, then follow it with the file name
    - ex: ```<a href="../index.html">Home</a>```
- grandparent folder - repeat the ../ to indicate you want to go up two folders rather than one before the file name.

### E-mail Links
```mailto:``` - to create a link that starts up the user's e-mail program and addresses an email to a sepcified email address, you use the ```<a>``` element. this time the value of the ```href``` attribute starts with ```mailto:``` and is followed by the email address you want the email to be sent to. 
- ex: ```<a href="mailto:email@example.com">person</a>```

### Opening Links  in a New Window
**target** - attribute. used if you want a link to open in a new window. the value of this attribute should be ```_blank```.
- GENERALLY you should avoid opening links to a new window. if you do, it is considered good practice to inform users that the link will open a new window before they click on it.

### Linking to a Specific Part of a Homepage 
ex: 
```<h1 id="top">Title</1>```
```<a href="#section_one">Section One</a>```
```<p>filler text</p>```
```<a href="#top">Return to Title</a>```

- the value of the attribute should start with a letter or an underscore (not a number or any other character)
- on a single page, no two two id attributes should have the same value 

## CSS Layouts
- block level elements: start on a new line
- inline elements: flow in between the surrounding text

### Position of Elements:
**Normal flow** 

every block element is on a new line

**Relative positioning**

moves an element from the position it would be in normal flow, shifting it to the top/right/bottom/left whhere it would have been placed. does not affect the position of the surrounding elements.

**Absolute Positioning**

positions the element in relation to its containing element. 
- taken out of the normal flow
    - does not effect the position of any surrounding elements 
    - move as users scroll up/down the page 

**Floating Elements**

allows you to take an element in normal flow and place it as far as left/right of the containing element as possible

### Layout Types
**fixed** - does not adjust to the screen size. is fixed to where it is
**liquid layouts** adjusts to the screen size.

Designers keep pages within  960-1000 pixels wide and indicate what the tite is about within the top 600 pixels (to demonstrate its relevance without scrolling)

Grids help create professional and flexible designs

CSS Frameworks provide rules for common tasks

Multiple CSS files can be included in one page

## JavaScript Functions 
 lets you group a series of statements together to perform a specific task
 - if different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of statements)

**CALLING THE FUNCTION**
- when you ask the function to perform its task

**PARAMETERS**
- when pieces of information are passed to a function

**RETURN VARIABLE**
- when you write a function and you expect it to provide an answer

### Declaring a Function

**function declaration**
- to create a function, you give it a name and then write the statements needed to achieve its task inside the curly braces

### Calling Functions That Need Information
**Arguements** - the values that you specify the function should use in the parenthesis that follow its name. can be provided as values or variables

[<===](README.md)