## CSS SELECTORS

### selctors

It is an pattern to style the element and it tell the browser which html elements should be selected to have the CSS property.

### Types of selectors

1. Element Selector
2. Id Selector
3. Class Selector
4. Universal Selector
5. Group Selector
6. Attribute Selector
7. Combinators Selector
8. Pseudo-class
9. Pseudo-element

> #### Element Selector

Element selctor will select the _all html element_ of node.

```css
p {
  color: red;
}
```

> #### Id Selector

Id selctor will select one html element with a specific _id attribute_., write a hash (#) character, followed by the id of the element.

```css
#demo {
  color: red;
}
```

> #### Class Selector

Class selctor will select all the html element with a specific _class attribute_, write a dot (.) character, followed by the id of the element.

```css
.demo {
  color: red;
}
```

> #### Universal Selector

Universal selctor will select all the element document, write a asterisk (\*).

```css
* {
  color: red;
}
```

> #### Group Selector

Group selector will select all the element and style them together.To group selectors declare _,_ and give _space_ between elements.

```css
div,
span {
  color: red;
}
```

> #### Attribute Selector

Attribute selector will select the element based on the _certain attribute_ and _particular value_ of attribute.

```css
a[title] {
  color: red;
}
a[href="https://example.com"]
{
  color: red;
}
```

> #### Combinators Selector

Combinators selector is used to specify the relationship between exactly two CSS selectors.

#### There are four different types of Combinators

- General sibling Combinator(~)
- Adjacent sibling Combinator(+)
- Child Combinator(>)
- Descendant Combinator(space)

**General sibling Combinator(~)**

General sibling Combinator is select siblings of an element even if they are not directly adjacent, then you can use the general sibling combinator (~).

```css
h1 ~ p {
  font-weight: bold;
  background-color: #333;
  color: #fff;
  padding: 0.5em;
}
```

**Adjacent sibling Combinator(+)**

Adjacent sibling Combinator will matches only those elements matched by the second selector that are the next sibling element of the first selector.(+) is placed between two selector.

```css
h1 + p {
  font-weight: bold;
  background-color: #333;
  color: #fff;
  padding: 0.5em;
}
```

**Child Combinator(>)**

Child Combinator will matches only second selector that are the direct children of elements matched by the first.(>) is placed between two selector

```css
ul > li {
  border-top: 5px solid red;
}
```

**Descendant Combinator(space)**

Descendant Combinator will select all the child elements of the specified element.The element can be the direct child of the specified element or can be very deep in the specified element. (space) is placed between two selector

```css
.box p {
  color: red;
}
```

> #### Pseudo-class

Pseudo-class used to add styles to selectors, but only when those selectors meet certain conditions. A pseudo class is expressed by adding a colon (:) .pseudo-class is a keyword added to a selector that specifies a special state of the selected element(s).

```css
a/* Any button over which the user's pointer is hovering */
button:hover {
  color: blue;
}
/* It will style to button when it hover*/
.container:fullscreen {
  ...;
}
/* When the element is switched back and forth between fullscreen this css rule will be applied */
input:autofill {
  ...;
}
/* Matches when an input has been autofilled by the browser. */
*:enabled {
  ...;
}
/* Represents a user interface element that is in an enabled state. */
*:disabled {
  ...;
}
/* Represents a user interface element that is in a disabled state.*/

input:checked {
  ...;
}
/* Matches when elements such as checkboxes and radio buttons are toggled on. */
a:link {
  ...;
}
/* Matches links that have not yet been visited. */

a:visited {
  ...;
}
/* Matches links that have been visited. */
td:nth-child(arg) 
/* selects all the td elements which will be odd or even */
 
li:first-child {
  ...;
}
/* selects the first sibling  */
li:last-child {
  ...;
}
/* selects the last sibling */
button:active {
  ...;
}
/* Matches element that is being activated by user */
input:focus {
  ...;
}
/* Matches element that has received focus */
```

> #### Pseudo-elements

 pseudo-element is a keyword added to a selector that lets you style a specific part of the selected elements.

```css
p::first-line {
  color: blue;
  text-transform: uppercase;
} /*applies styles to the first line of a p element*/
p::first-letter {
  color: blue;
  text-transform: uppercase;
}
/*applies styles to the first letter of the first letter of a block-level element*/
p::after {
  /* It is used to add something after the element's content. */
  content: "hi";
}
p::before {
  /* It is used to add something before the element's content.*/
  content: "hi";
}
input::placeholder {
  ...;
}
/* it focus on the placeholder attribute of the input tag */
p::selection {
  ...;
}
/* Applies styles to a part of the content which was selected by the user */
```
