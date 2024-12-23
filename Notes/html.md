# HTML & UDEMY COURSE NOTES (HTML & CSS NOTES) - BASICS

Headers can be h1-h6 throughout the document. Usually the header is within the BODY of the document. 

<strong><'em'></strong> is a tag to make things italic and <strong><'strong'></strong> is a tag to make things bold - this is more semantic and better practice when compared to <'i'> and <'e'>.

Comments can be made using the <!--task still to do->

a <'section'> element can be used to give the html meaning rather than a <'div'> for web design, as a <'div'> element holds no semantic meaning.

<'meta charset="UTF-8/'> - meta stands for meta data (data about the data). Charset is the character set and then UTF-8 encapsulates all the characters we use in the english language.

A good structure to have at the top of your CSS stylesheet is as follows: <strong>This is used as a global reset</strong> to make it easier to style our pages. 

<strong>* {
    margin: 0;
    padding: 0;
    box-sizing: border-box; 
}</strong>

<strong><'li'></strong> items can form a list within a paragraph which can either be an unordered list <strong><'ul'></strong> or ordered list <strong><'ol'></strong>

<strong><'img'></strong> tag is a self closing tag and usually require a source and alternate comment. For example: 

<'img src="link-of-photo" alt="picture-of-dog"'> - src is an example of an attribute which can describe elements. Alt will allow search engines to know what the image is actually about & allows blind people to use our website!

Also always make sure you put your images in a seperate folder on the explorer tag.

<strong><'a'></strong> tags are anchor tags that source links from another page and are not self-closing tags.

<strong><'a href="link to website">Click for link</a'></strong> - this would be an example, which would translate to: <a href="link_to_website">Click for link</a>.

Usually anchor tags should also have a target which makes sure the link opens in a new tab. For example: 

<strong><"a target="_blank" href="link to website"><img src="link-to-picture" alt="picture-of-dog"/></a"></strong> which would equal - <a target="_blank" href="link_to_website"><img src="link-to-picture" alt="picture-of-dog"/>

You can also use the # as a placeholder after the link - <'a' href="#"></'a>. 

A <strong><'nav'></strong> element is a special element to help store links - navigation. These are usually stored within header elements - <strong><'header'></strong>. These can sometime also contain your h1/h2 elements for example.

An <strong><'article'></strong> element can be a multitude of things, it doesn't necessarily mean it will be an article. 

You can also nest a the </strong><'img'></strong> information within a <strong><'figure'></strong> element and use <strong><'figcaption'>This is my dog</figcaption></figure'></strong> as a caption under the img.

listed items can be ordered <strong><'ol'></strong> or unordered <strong><'ul'></strong> and between these elements will require <strong><'li'></strong> elements.

<strong><'form'></strong> elements can be used to submit form information on your website. These are usually paired with <strong><'action'></strong> elements which indicate where the form is sent to. For example: 

<strong><'form action="url">information</form'></strong> - the url is obviously where the information is sent to. 

<strong><'input'></strong> elements also do not require closing tags. They have multiple types which can be seen below (but not limited to):

<ul>
<li><'input type="button"'></li> - in CSS buttons can have hover styles.

<li><'input type="checkbox"'></li>

<li><'input type="date"'></li>

<li><'input type="email"'></li>

<li><'input type="submit"'></li>
</ul>

input elements require <strong><'label'></strong> elements to define the values. Input elements have a lot of default styling - such as borders, backgrounds and outlines. 

A <strong><'footer'></strong> element should still be based within the body.

<strong><'div'></strong> are used when we don't want to attach a certain meaning to a certain container. <'nav'> for example will be needing to ensure that the links are under a navigation for example - to give the element meaning.

An <'aside'> element is used for secondary information - related posts about the main part or as a sidebar. 

# CSS notes

CSS includes selectors (i.e. h1) and then the style which includes properties (i.e. color, font-size) and values (i.e. blue, 14px). Properties and values together are called declarations/styles. The declaration block includes ALL the properties and values for the selector. ALL of this together (including the selector) is called a <strong>CSS rule</strong>. 

<'link href="styles.css" rel="stylesheet"/> - is a good way to let the html know that this is a stylesheet - this is put in the head of the HTML. 

<strong>line-height property</strong> - 1.5 would mean that the line height is 1.5 x the font-size. By default it is 1.0.

The normal font-size is 16px. 

<strong>eA descendant selector</strong> in CSS (i.e 'footer p {') will select all the p elements inside of all the 'footer' elements as it is a child element of the footer. 

To add comments or block out comments on CSS - /* */ . "ctrl /" will automatically comment out a CSS declaration.

For classes, it is good to use - between spaces. Classes should be used before ID's (always use classes). This makes sure you avoid any errors by using ID's in the future - especially if you have a very big project full of code.

To remove bullet points from lists, you need to use the <strong>list-style</strong> property. 

<strong>Colours</strong> can be represented by <em>the RGB model</em> (R, G, B). These can be values up to 255. I.e. Red would be (255, 0, 0). You can also use the <em>RGBA</em> model - the extra colour option is for transparency/alpha (which is used as a decimal). Colours can also be used with the <em>hexadecimal notation</em>. This is more commonly used - i.e. '#00ffff" (00 is red, ff is green, ff is blue). You can also use shorthand with this, i.e. '#0ff'. 

A pseudo class is used by writing a ':' in between selectors. An example would be the 'li:first-child' which means that the first child element inside of the parent element will be selected, and then whatever property and value is selected will only impact the first-child of that container. This can be the same for last-child, nth-child(2), nth-child(3), nth-child(odd), nth-child(even) etc. 

When styling hyperlinks or 'a', you should make sure to style the 'a' in all of the different states. These are listed below and <strong>MUST</strong> be in this order below <em>(LVHA)</em> 
</ul>
<li>'a:link' - this will style the anchor elements that have an 'href' attribute</li>
<li>'a:visited' - this will style the anchor when the link is visited. This should be the same color as the above 'a:link'</li>
<li>'a:hover' - this will style the anchor elements when you hover over the hyperlink</li>
<li>'a:active' - this will style the anchor element when you click the hyperlink</li>
</ul>

To style the above in CSS - you can save some time by doing the following (this is usually best practice): For example: 

.class-name:link, .class-name:visited {
color: black; 
}
.class-name:hover, .class-name:active {
color: white; 
}


# Conflicts between SELECTORS (IMPORTANT PART OF CSS)

Highest priority in CSS

<ol>
    <li>!important - not really used either, but can use if stuck</li>
    <li>inline styles (not necessarily used)</li>
    <li>ID selector (#)</li>
    <li>class selector (.) or pseudoclass selector (:) </li>
    <li>element selector (i.e. div, p)</li>
    <li>universal selector (*)</li>
</ol>

To find out which css style has priority, hover over the CSS and look at the Selector Specificity (1, 0, 0). The higher the numbers, the more that css style has priority over the other.

<ul>
    <li>Hovering over a property with (1,0,0) would mean that this is the declaration that has the highest priority, followed by (0,1,0) and then (0,0,2) for example.</li>
</ul>

<strong>Inheritence</strong> - most properties related to text will get inherited

# BOX MODEL - Will need to brush up on this 

<ul>
<li>The border is still inside of the element</li>
<li>The padding is the space between the border and the content - this is still <strong>inside</strong> of the element too</li>
<li>The margin is the space <strong>outside</strong> of the element - between elements. This is used to create space betwen elements</li>
    <li>The <strong>fill area</strong> is the area (excluding the margin - as this is the space between elements) that will be filled with the background color and background images</li>
    <li>All of the above are optional</li>
</ul>

The final height of an element would be the bottom border, bottom padding, height, top padding, top border.
The final width of an element would be the left border, left padding, width, right padding, right border.
This above is just the default behaviour, you can change this throughout. 
This means that the margin is not involved in the final width and height. 

Short hand for padding: first number = (paddingtop + paddingbottom) second number = (paddingleft + paddingright)

When styling list items, you want to make sure you don't have any space at the end of the last item of the list. You only want to have space between list items. To do this you would have li:last-child margin: 0;

It is usually more common to have space at the bottom, to achieve vertical space. 

<strong>Collapsing margins</strong> is a phenomenon when you have (for example) a margin-top of one element set at 40px and a margin-bottom of another element set at 15px. You would expect them to be added to a total of 55px between the margins of the two, but in fact it is usually only 40px total (usually the bigger number). This is called collapsing margins. 

When styling images for size under CSS - you can also use percentages. The percentage of the image's width/height (i.e. 100%) would be 100% of the parent container's width/height. 

A good way to centre your page would be to add a <'div'> element just after your <'body'> element and close it when the <'/body'> element ends. You could then for example make a class from that element, and style it with a set width. The margin-left and margin-right properties could then have a value of auto (meaning that the browser will make sure that the margin to the left and right is always the same).

<strong>What I got stuck on - you can't use margins on elements such as links!</strong>

# Types of Boxes

<strong>Inline elements</strong> occupy only the exact space that they need. They can be side by side with one another. Padding and margins are only applied <em>horizontally</em>. This is extremely important to keep in mind! Default inline elements would be <em>strong, em, a, button etc.</em>. They do not make line breaks. 

<strong>Block level elements</strong> occupy all the space that they can, and can create linebreaks after them (meaning they cannot be side by side with one another). These <em>elements occupy 100% of the parent's width</em>. These elements can be stacked one after another by default. Default block elements are usually: <em>body, main, header, section, nav, li, div, aside, h1-h6, p, ol, ul etc.</em>.

<strong>Inline block elements</strong> look like inline blocks from the outside, but behave like block level elements on the inside. They do not cause any line breaks but you can use heights, width, paddings and margins (combines the best of both worlds between the two). Display: inline-block. IMG's behave like inline-block elements. 

Normal flow is the normal/default positioning (position: relative). 
Absolute flow (position: absolute) means that the element will be out of the flow. This would mean it doesn't have impact around the surrounding elements. You can use the top, bottom, left or right properties in order to position the element from it's <em>relatively positioned container</em>. This can be a great way to "fix" an item on the page, so it doesn't move elements around it when shifting the page. 
When setting top, bottom, left or right - the pixels are in relation to the viewport (which is the visible part of the page in the browser). Usually this is not what we want, we usually want to make sure that it is positioned in relation to a <em>parent element</em>. Meaning we should set the parent element to relative. 
We only use absolute positioning for buttons really, or small elements. 

<strong>Pseudo-elements</strong> are written in the CSS with two colons (::). An example would be <em>'h1::first-letter'</em> which would mean that you can style every first leader of the h1 class. 

<em>Siblings</em> are all elements that are under the parent element. Using the <strong>adjacent-sibling</strong> pesudo-element will style the very next element in the HTML. The adjacent sibling selector would be for example: h3 <strong>+</strong> p::first-line - would mean only the paragraphs immediately after the h3 would be selected (and the first line obviously). 

The most used pseudo-elements are the ::after and ::before pseudo-elements. Within both you need to specify the content. This way you can create elements outside of the "html" and create items in the "CSS". 

If having trouble centering text, try to use "'text-align: center'" on the parent element - as they could be inline or inline-block elements. 

# Good Websites for Reference & HELP
<ul>
    <li>Stack overflow</li>
    <li>CSS tricks</li>
    <li>Developer.mozilla.org - which is the <strong>MDN documentation</strong></li>
    <li>HTML validator (W3) version - copy and pasting the code to see where the errors are.</li>
    <li>Diff Checker - to compare code between your creation and another sites</li>
</ul>

# Building Layouts 

<p>Layouts are ways to build visual structure, instead of just having them in the "normal flow"</p>
<p>There are three ways to make layouts</p>
<ol>
    <li><strong>Float layouts -</strong> older version of layouts that are becoming outdated</li>
    <li><strong>Flexbox -</strong> modern way to build one dimensional layouts - perfect for component layouts</li>
    <li><strong>CSS Grid -</strong> perfect for big page layouts and complex components (2 dimensional grid)</li>
</ol>

# Float Layouts 

<p>Float layouts will take the element completely out of the "flow" (i.e. float:'left' or float:'right').</p>
<p>Float elements are still able to create margins around them.</p>
<p>Floats may seem similar to absolute positioning, as the elements are moved "out of the flow" - but text and inline elements will wrap around the floated element. The container will also not adjust it's height to the element and this can result in "collapsing heights". </p>

<strong>Clearing Floats -</strong>: you will need to create a new element (usually a div with the class - clear) and then style it for clear: left, right or both. This is if you have collapsing heights. This is not usually best practice however so you can do the following: create another class for the element you are adjusting and name this clearfix. On CSS you can then create a pseudo property (usually ::after) and then define content (because it has to have some content - even if it is just '') and then display: block, then you can create another property clear: both; and it should do the same thing (rather than making an extra div for each). 

<p>Box-sizing: border box - is a great tool to use in majority of the elements. It takes away from the default box model to make sure that the height and the width are fixed inside the border of an element when designing layouts. If there is extra padding and margins, it will subtract it from the total width to make sure the element does not disappear or go where you don't want it to go. <strong>It is usually applied to the universal selector at the start of the CSS</strong></p>

# Flex Box 

<ul>
    <li>This is an easier way that 'floats' to bring elements side by side (display: flex).</li>
    <li>Vertically by default, all the flex items are as tall as the tallest element. It is the best way to build 1 dimensional layouts. </li>
    <li>It makes it a lot easier to align items one another inside of a parent container (both horizontally and vertically).</li>
    <li>The main axis is the line that goes from left to right, and the cross axis is up and down.</li>
    <li>The flex container is the main container (parent container) that holds all of the flex items (child elements). </li>
    <li>Flex box is allowed to shrink elements so that they fit the container. </li>
    <li>The default direction is "row" which means the main axis is horizontal and the cross axis is vertical. When this switches to "column" i.e. flex-direction: column - this axis then changes and the main axis becomes the vertical axis, and cross axis becomes the horizontal axis.</li>
</ul>
<p><strong>THE FLEX CONTAINER PROPERTIES- </strong> include mainly the following:</p>
<ol>
    <li><strong>The GAP property: which has a default of 0</strong> - length: this creates space between lines without using margins</li>
    <li><strong>The JUSTIFY-CONTENT property: which has a default of flex-start</strong> - flex-start, flex-end, center, space-between, space-around, space-evenly: this aligns items along the <strong>main axis</strong></li>
    <li><strong>The ALIGN-ITEMS property: which has a default of stretch</strong> - flex-start, flex-end, center, baseline - this aligns items along the <strong>cross axis</strong>. If this doesn't work, usually you need to specify a height - i.e. height: 100vh. Baseline usually keeps all the text even, no matter how big the size of the flex-item is. </li>
    <li><strong>The FLEX-DIRECTION property: which has a default of row</strong> - row-reverse, column, column-reverse: this defines which is the main axis</li>
        <li><strong>The FLEX-WRAP property: which has a default of nowrap</strong> - wrap, wrap-reverse: this allows items to wrap into a new line if they are too big. In order to set the flex-wrap though you will need to make sure the element has a select width/flex-basis.</li>
    <li><strong>The ALIGN-CONTENT property: which has a default of stretch</strong> - flex-start, flex-end, center, space-between, space-around: only applies when there are multiple lines. </li>
</ol>
<p><strong>THE FLEX ITEM PROPERTIES - </strong> include mainly the following:</p>
<ol>
    <li><strong>The ALIGN-SELF property which has a default of auto</strong> - stretch, flex-start, flex-end, center, baseline: this overrides the align-items for <strong>individual flex items</strong>.</li>
    <li><strong>Flex Grow which has a default of 0</strong> - allows an item to grow (0 means no, +1 means yes). If all flex items have 1 it means they will all grow to the same size.</li>
    <li><strong>Flex Shrink which has a default of 1</strong> - allows an item/element to shrink to fit inside of the container (0 means no, +1 means yes). There are no negative values for this. </li>
    <li><strong>Flex Basis which has a default of auto</strong> - defines an items width instead of the "width" property. Flex basis acts as a recommendation to the browser (it is not really a rule) but acts as the starting measurement/width.</li>
    <li>The short hand of all the above goes flex: grow, shrink, basis - always use the shorthand</li>
    <li>If flex:1 then it means that flex-grow is 1 AND flex-shrink is 1.</li>
    <li><strong>The ORDER property which has a default of 0</strong> - which controls the order of the flex items (-1 makes it first, 1 makes it last)</li>
</ol>

# CSS Grid - 

CSS grid makes two dimensional layouts. It divides the container elements into rows and columns to make easier to read HTML and CSS. Display: grid. 
To use CSS grid, you use grid-template-columns and grid-template-rows. 
Always use gap when doing grids, <strong>not margins</strong>.
<ol>
    <li>column-gap: makes the gap between columns</li>
    <li>row-gap: makes the gap between rows</li>
    <li>Gaps are also called gutters.</li>
</ol>

If you want a one dimensional layout - use flexbox, but if you want a two dimensional layout, use CSS grid. You cannot change the axis for CSS grids. 

<strong>Grid Container</strong> has 3 MAIN properties you can use: 

<ol>
    <li>grid-template-rows and grid-template-columns which show the track size usually in pixels or fr (fractional). Fr kind of acts as flex:1 on flexbox. To make 4 columns the same width using the fr property, you would write - grid-template-columns: repeat(4, 1fr); </li>
    <li>row-gaps and column-gaps - to create empty space between tracks</li>
    <li>justify-items and align-items - to align items horizontally and vertically</li>
</ol>

<strong>Grid Items</strong> has 2 MAIN properties you can use: 

<ol>
    <li>grid-column and grid-row - which have a start and end line (usually span)to place a grid item in a specific cell</li>
    <li>justify-self and align-self - to overwrite align-items and justify-items for SINGULAR items</li>
</ol>

<strong>Justify-content and align-content</strong> - if you wanted to do flex-end and flex-start (similar to flexbox) then you need to use "start" and "end" instead of "flex-end" and "flex-start". The <strong>Justify-content and align-content</strong> will align the tracks INSIDE THE CONTAINER whereas <strong>justify-items and align-items</strong> will aign items INSIDE THE CELL (both for the container). 

