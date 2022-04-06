# CSS-Interview-questions-
All the basics questiomns related to CSS

Problems
#### How to add comments on css?
Ans. To comment in CSS, simply place your plain text inside /* */ marks. This tells  the browser that they are notes and should not be rendered on the front end.

#### Why do we use pseudo-class?
Ans. A pseudo-class is used to define a special state of an element.
For example, it can be used to:
Style an element when a user mouses over it.

Pseudo-class names are not case-sensitive.
Pseudo-classes can be combined with HTML classes.
When you hover over the link in the example, it will change color:
selector:pseudo-class {
  property: value;
}
Like 
/* mouse over link */
a:hover {
  color: #FF00FF;
}

#### 3. How is specificity applied?
Ans. If there are two or more CSS rules that point to the same element, the selector with the highest specificity value will "win", and its style declaration will be applied to that HTML element. Think of specificity as a score/rank that determines which style declarations are ultimately applied to an element.

<style>
.test {color: green;} 
 p{
   color: red;
  } 
  #ptag{
	color:yellow;
}
</style>

<p class="test" id="ptag">Hello World!</p>

#### 4.  What method allows an element to be moved from its current position?
Ans .The translate() method moves an element from its current position (according to the parameters given for the X-axis and the Y-axis).

<style> 
div {
  width: 300px;
  height: 100px;
  background-color: yellow;
  border: 1px solid black;
  transform: translate(50px,100px);
}
</style>

<div>
This div element is moved 50 pixels to the right, and 100 pixels down from its current position.
</div>

#### 5. What properties does flex model have?
Ans. The flex property is a shorthand property for:
flex-grow
flex-shrink
flex-basis
The flex property sets the flexible length on flexible items.

#### 6. What is the difference between flex and grids?
Ans. Grid and flexbox. The basic difference between CSS Grid Layout and CSS Flexbox Layout is that flexbox was designed for layout in one dimension - either a row or a column. Grid was designed for two-dimensional layout - rows, and columns at the same time.
<div class="wrapper">
  <div>Three</div>
  <div>Four</div>
</div>

.wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
Flex Example :
.wrapper {
  width: 500px;
  display: flex;
  flex-wrap: wrap;
}
.wrapper > div {
  flex: 1 1 150px;
}

####  7. Give an example where we have to use grids and where you have to use flexbox? 
Ans. If you are using flexbox and find yourself disabling some of the flexibility, you probably need to use CSS Grid Layout. An example would be if you are setting a percentage width on a flex item to make it line up with other items in a row above. In that case, a grid is likely to be a better choice.
Use a grid when you already have the layout structure in mind, and flex when you just want everything to fit.

#### 8. Give an example where you cannot use flexbox, and you can only use grids?
Ans. When we want to implement a 2d design by using the grid and lest us says we want 5 elements in 1 row and 10 elements in 2nd row and 1 elements in 3rd row.

#### 9. What are combinators? give examples of how you can use them
Ans. A combinator is something that explains the relationship between the selectors. A CSS selector can contain more than one simple selector.
i). Descendant combinator
.box p {
    color: red;
}  
    
<div class="box"><p>Text in .box</p></div>
<p>Text not in .box</p>
    
 ii) Child combinator
ul > li {
    border-top: 5px solid red;
}  
<ul>
    <li>Unordered item</li>
</ul>

iii)Adjacent sibling combinator

The adjacent sibling selector (+) is placed between two CSS selectors. It matches only those elements matched by the second selector that are the next sibling element of the first selector. For example, to select all <img> elements that are immediately preceded by a <p> element.
p + img
	
iv)General sibling combinator
If you want to select siblings of an element even if they are not directly adjacent, then you can use the general sibling combinator (~). To select all <img> elements that come anywhere after <p> elements, we'd do this: p ~ img

#### 10. What does object-fit do?
Ans. The object-fit CSS property sets how the content of a replaced element, such as an <img> or <video> , should be resized to fit its container. You can alter the alignment of the replaced element's content object within the element's box using the object-position property.
	
#### 11. What does rotate do?
Ans: The rotate() CSS function defines a transformation that rotates an element around a fixed point on the 2D plane, without deforming it.
HTML:~
<div>Normal</div>
<div class="rotated">Div to be rorated </div>
CSS:~
div {
  width: 80px;
  height: 80px;
}

.rotated {
  transform: rotate(260deg);
}

#### 12. What rule can be used to define animations 
Ans: An animation lets an element gradually change from one style to another.
You can change as many CSS properties you want, as many times as you want.
To use CSS animation, you must first specify some keyframes for the animation.
Keyframes hold what styles the element will have at certain times
The @keyframes Rule
When you specify CSS styles inside the @keyframes rule, the animation will gradually change from the current style to the new style at certain times.
div {
  animation-name: example;
  animation-duration: 4s;
}

@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}


#### 13. When working with attribute selectors, how can you select elements which contain a particular attribute value
Ans:~ The [attribute] selector is used to select elements with a specified attribute.
a[target] {
  background-color: yellow;
}
input[type="text"] {
  margin-bottom: 10px;
  background-color: yellow;
}

#### 14. What does @media do?
Ans:~ The @media rule is used in media queries to apply different styles for different media types/devices.
@media screen and (min-width: 400px) {
  body {
	background-color: lightgreen;
  }
}
#### 15. What can be used to override properties of an element
Ans:~ To override the CSS properties of a class using another class, we can use the !important directive.

#### 16. How can you select every alternate element in a list of elements using css?
Ans:~  css odd even child

tr:nth-child(even) {background: #FFFFF}
tr:nth-child(odd) {background: #F0F0F}


#### 17. What is the ranking of selectors with respect to specificity?
Ans:~ Every selector has its place in the specificity hierarchy. If two selectors apply to the same element, the one with higher specificity wins. There are four distinct categories which define the specificity level of a given selector: inline styles, IDs, classes, attributes, and elements.

#### 18. how can we apply same styles to multiple selectors?
Ans:~ Grouping CSS selectors helps minimise the size of your stylesheet so it loads faster Admittedly, style sheets are not the main culprits in slow loading; CSS files are text files, so even very long CSS sheets are tiny when compared to unoptimized images. Still, every bit of optimization helps, and if you can save some size off your CSS and load the pages that much faster, that's a good thing.
Grouping selectors also makes site maintenance far easier. If you need to make a change, you can simply edit a single CSS rule instead of multiple ones. This approach saves time and hassle.
Ex2. th, td, p.red, div#firstred { color: red; }


#### 19. What are the differences between relative and absolute in CSS?
Ans:~ position: relative places an element relative to its current position without changing the layout around it, whereas position: absolute places an element relative to its parent's position and changing the layout around it.
