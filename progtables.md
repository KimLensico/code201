# Object-Oriented Programming, HTML Tables

## Domain Modeling
### Summary
Domain modeling is the process of creating a conceptual model for a specific problem. And a domain model that's articulated well can verify and validate your understanding of that problem.

**Tips to follow when building your own domain models.**

1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
2. Model its attributes with a constructor function that defines and initializes properties.
3. Model its behaviors with small methods that focus on doing one job well.
4. Create instances using the new keyword followed by a call to a constructor function.
5. Store the newly created object in a variable so you can access its properties and methods from outside.
6. Use the this variable within methods so you can access the object's properties and methods from inside.

### Tables
- a **table** represents information in a grid format
    - ex: financial reports, tv schedules, sports results
- grids allow us to understand complex data by referencing information on two axis
- each blco in the grid is referred to as a *table cell*.
    - in HTML a table is written out row by row
- ```<table>``` element is used to create a table
    - the contents are written out row by row
- ```<tr>``` - indicates the start of each row
    - followed by one or more ```<td>``` elements 
        - one for each cell in that row
        - use closing tag at the end of each row

EXAMPLE:
```
<table>
    <tr>
        <td>15</td>
        <td>15</td>
        <td>30</td>
    </tr>
    <tr>
        <td>45</td>
        <td>60</td>
        <td>45</td>
    </tr>
    <tr>
        <td>60</td>
        <td>90</td>
        <td>90</td>
    </tr>
</table>
```

- ```<th>``` - used like the td element - *table heading*
    - purpose is to represent the heading for either a column or a row
    - even if a cell has no content, you should still use a ```<td>``` or ```<th>``` to represent the presence of an empty cell
        - table will not show correctly otherwise
    - helps people who use screen readers
    - improves ability for search engines to index in your pages
    - enables you to control the appearance of tables better 
    - you can use the scope attribute on the ```<th>``` element to indicate whether it is a heading for a column or a row
        - it can take the values ```row``` to indicate a heading for a row or ```col``` to indicate a heading for a column 
- ```<colspan>``` attribute can be used on a ```<th>``` or ```<td>``` element and indicates how many columns that cell should run across.
- ```<rowspan>``` attribute can be used on a ```<th>``` or ```<td>``` element to indicate how many rows a cell should span down the table.
- the headings of the table should sit inside the ```<thead>``` element
- the body should sit inside the ```<tbody>``` element
- the footer belongs inside the ```<tfoot>``` element

### Creating an Object: Constructor Notation
- the **new** keyword and the object constructor create a blank object
    - you can then add properties and methods to the object
- ```this``` is commonly used inside functions and objects
    - it refers to one object
        - usually the object in which the function operates

