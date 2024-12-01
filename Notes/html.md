# HTML & UDEMY COURSE NOTES (HTML & CSS NOTES) - BASICS

Headers can be h1-h6

<strong><'em'></strong> is a tag to make things italic and <strong><'strong'></strong> is a tag to make things bold - this is more semantic and better practice when compared to <'i'> and <'e'>.

Comments can be made using the <!--task still to do->

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

input elements require <strong><'label'></strong> elements to define the values. 

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
