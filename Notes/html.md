# HTML & UDEMY COURSE NOTES (HTML & CSS NOTES) - BASICS

Headings can be h1-h6 and can be used throughout the document. They are usually used in new section elements. 

<strong><'em'></strong> is a tag to make things italic and <strong><'strong'></strong> is a tag to make things bold - this is more semantic and better practice when compared to <'i'> and <'e'>.

Comments can be made using the <!--task still to do->

a <'section'> element can be used to give the html meaning rather than a <'div'> for web design, as a <'div'> element holds no semantic meaning.
a <'span'> element can be used for inline text (and is preferred over a div - but this doesn't hold any semantic meaning. This can be great for things like subheadings. If you were to style a span element, you would want to make this a block element.  
a <'blockquote'> element is used when you want to quote text. 

<'meta charset="UTF-8/'> - meta stands for meta data (data about the data). Charset is the character set and then UTF-8 encapsulates all the characters we use in the english language.

A good structure to have at the top of your CSS stylesheet is as follows: <strong>This is used as a global reset</strong> to make it easier to style our pages. 

<strong>* {
    margin: 0;
    padding: 0;
    box-sizing: border-box; 
}</strong>

It is also common practice to split your css into multiple files! (i.e. using all of your general CSS and creating a folder called general.css to link to) - this way your code is easier to access and easier to go back to/read. 

<strong><'li'></strong> items can form a list within a paragraph which can either be an unordered list <strong><'ul'></strong> or ordered list <strong><'ol'></strong>

<strong><'img'></strong> tag is a self closing tag and usually require a source and alternate comment. For example: 

<'img src="link-of-photo" alt="picture-of-dog"'> - src is an example of an attribute which can describe elements. Alt will allow search engines to know what the image is actually about & allows blind people to use our website!

Also always make sure you put your images in a seperate folder on the explorer tag. Images will also always take as much space as they can. You can also add a filter to images in CSS using the filter CSS property. If you see a space between img's that you don't want there, you have to change it to display: block; 

<strong><'a'></strong> tags are anchor tags that source links from another page and are not self-closing tags.

<strong><'a href="link to website">Click for link</a'></strong> - this would be an example, which would translate to: <a href="link_to_website">Click for link</a>.

Usually anchor tags should also have a target which makes sure the link opens in a new tab. For example: 

<strong><"a target="_blank" href="link to website"><img src="link-to-picture" alt="picture-of-dog"/></a"></strong> which would equal - <a target="_blank" href="link_to_website"><img src="link-to-picture" alt="picture-of-dog"/>

You can also use the # as a placeholder after the link - <'a' href="#"></'a>. 

A <strong><'nav'></strong> element is a special element to help store links - navigation. These are usually stored within header elements - <strong><'header'></strong>. These can sometime also contain your h1/h2 elements for example. It is a good idea to add an "ul" when storing your anchor tags in a nav - this makes it more semantic. If you are using LOGOs in a header, it is important to wrap the logo in a <'anchor'> tag so that when people click on the logo, it goes back to the top of the page. 

<strong>WHEN STYLING A NAV SECTION, SET THE DISPLAY OF THE NAV TO FLEX AND THEN YOU CAN ORGANISE YOUR CONTENT AS YOU LIKE (I.E. JUSTIFY-CONTENT: SPACE BETWEEN). 

An <strong><'article'></strong> element can be a multitude of things, it doesn't necessarily mean it will be an article. 

You can also nest a the </strong><'img'></strong> information within a <strong><'figure'></strong> element and use <strong><'figcaption'>This is my dog</figcaption></figure'></strong> as a caption under the img.

listed items can be ordered <strong><'ol'></strong> or unordered <strong><'ul'></strong> and between these elements will require <strong><'li'></strong> elements.

<strong><'form'></strong> elements can be used to submit form information on your website. These are usually paired with <strong><'action'></strong> elements which indicate where the form is sent to. For example: 

<strong><'form action="url">information</form'></strong> - the url is obviously where the information is sent to. 

<strong><'input'></strong> elements also do not require closing tags. They have multiple types which can be seen below (but not limited to):

<ul>
<li><'input type="button"'></li> - in CSS buttons can have hover styles. - A button will always have a border so make sure the style is set to none if you want to style it.

<li><'input type="checkbox"'></li>

<li><'input type="date"'></li>

<li><'input type="email"'></li>

<li><'input type="submit"'></li>
</ul>

input elements require <strong><'label'></strong> elements to define the values. Input elements have a lot of default styling - such as borders, backgrounds and outlines. 

A <strong><'footer'></strong> element should still be based within the body (but outside of the main element). 

<strong><'div'></strong> are used when we don't want to attach a certain meaning to a certain container. <'nav'> for example will be needing to ensure that the links are under a navigation for example - to give the element meaning.

An <'aside'> element is used for secondary information - related posts about the main part or as a sidebar. The main element is where you would want to use for your main information.  

## CSS notes

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

A common theme for links is having the link and visited state (as inline-block) with a border-bottom (i.e. 1px solid currentColor) and then getting rid of the underline/border-bottom when the link is hovered/active (i.e. 1px solid transparent) - can't just get rid of the border-bottom as it will become janky. 

## Conflicts between SELECTORS (IMPORTANT PART OF CSS)

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

When using absolute positioning to take a complete element out of the flow of the page, you must make sure to make the parent container's position to relative. Top and left will only use the dimensions of the PARENT element as the reference. (refer to lecture 113 for a good recap of positioning). 

#nbsp; - is a non-breaking space to use in your code instead of "empty space". 

## BOX MODEL - Will need to brush up on this 

<ul>
<li>The border is still inside of the element</li>
<li>The padding is the space between the border and the content - this is still <strong>inside</strong> of the element too</li>
<li>The margin is the space <strong>outside</strong> of the element - between elements. This is used to create space betwen elements</li>
    <li>The <strong>fill area</strong> is the area (excluding the margin - as this is the space between elements) that will be filled with the background color and background images</li>
    <li>All of the above are optional</li>
</ul>

The final height of an element would be the bottom border, bottom padding, height, top padding, top border (NO COMMAS). 
The final width of an element would be the left border, left padding, width, right padding, right border (NO COMMAS). 
When styling a button, it is a good idea to have the second value of the padding shorthand usually double of the first (i.e 16px, 32px). 
This above is just the default behaviour, you can change this throughout. 
This means that the margin is not involved in the final width and height. 

Short hand for padding: first number = (paddingtop + paddingbottom) second number = (paddingleft + paddingright) - <strong>goes round in a clockwise direction</strong>

When styling list items, you want to make sure you don't have any space at the end of the last item of the list. You only want to have space between list items. To do this you would have li:last-child margin: 0;

It is usually more common to have space at the bottom, to achieve vertical space. 

<strong>Collapsing margins</strong> is a phenomenon when you have (for example) a margin-top of one element set at 40px and a margin-bottom of another element set at 15px. You would expect them to be added to a total of 55px between the margins of the two, but in fact it is usually only 40px total (usually the bigger number). This is called collapsing margins. 

When styling images for size under CSS - you can also use percentages. The percentage of the image's width/height (i.e. 100%) would be 100% of the parent container's width/height. 

A good way to centre your page would be to add a <'div'> element just after your <'body'> element and close it when the <'/body'> element ends. You could then for example make a class from that element, and style it with a set width. The margin-left and margin-right properties could then have a value of auto (meaning that the browser will make sure that the margin to the left and right is always the same).

<p><strong>Using AUTO for width/height will mean that the element will only be filled by whatever is in the content</strong></p>

<strong>What I got stuck on - you can't use margins on elements such as links!</strong>

### Types of Boxes

<strong>Inline elements</strong> occupy only the exact space that they need. They can be side by side with one another. Padding and margins are only applied <em>horizontally</em>. This is extremely important to keep in mind! Default inline elements would be <em>strong, em, a, button etc.</em>. They do not make line breaks. 

<strong>Block level elements</strong> occupy all the space that they can, and can create linebreaks after them (meaning they cannot be side by side with one another). These <em>elements occupy 100% of the parent's width</em>. These elements can be stacked one after another by default. Default block elements are usually: <em>body, main, header, section, nav, li, div, aside, h1-h6, p, ol, ul etc.</em>.

<strong>Inline block elements</strong> look like inline blocks from the outside, but behave like block level elements on the inside. They do not cause any line breaks but you can use heights, width, paddings and margins (combines the best of both worlds between the two). Display: inline-block. IMG's behave like inline-block elements. 

<strong>In order to give a button padding, you may need to set the display to inline-block to create a border-radius.</strong>

Normal flow is the normal/default positioning (position: relative). 
Absolute flow (position: absolute) means that the element will be out of the flow. This would mean it doesn't have impact around the surrounding elements. You can use the top, bottom, left or right properties in order to position the element from it's <em>relatively positioned container</em>. This can be a great way to "fix" an item on the page, so it doesn't move elements around it when shifting the page. 
When setting top, bottom, left or right - the pixels are in relation to the viewport (which is the visible part of the page in the browser). Usually this is not what we want, we usually want to make sure that it is positioned in relation to a <em>parent element</em>. Meaning we should set the parent element to relative. 
We only use absolute positioning for buttons really, or small elements. 

Viewport height (vh) i.e. 100vh (means it will take up the space of 100% of the viewport height). Can also be 50vh (which means it would be exactly half of the screen). 

<strong>Pseudo-elements</strong> are written in the CSS with two colons (::). An example would be <em>'h1::first-letter'</em> which would mean that you can style every first leader of the h1 class. 

<em>Siblings</em> are all elements that are under the parent element. Using the <strong>adjacent-sibling</strong> pesudo-element will style the very next element in the HTML. The adjacent sibling selector would be for example: h3 <strong>+</strong> p::first-line - would mean only the paragraphs immediately after the h3 would be selected (and the first line obviously). 

The most used pseudo-elements are the ::after and ::before pseudo-elements. Within both you need to specify the content. This way you can create elements outside of the "html" and create items in the "CSS". These cannot be added to imgs. Specifying the width and content (even if content: "") is important. If you want to make a box, define the width as a percentage and padding-bottom as the height (as you can't use the height). The padding-bottom will act as the height as it will be the percentage of the parent's.

If having trouble centering text, try to use "'text-align: center'" on the parent element - as they could be inline or inline-block elements. 

### Good Websites for Reference & HELP
<ul>
    <li>Stack overflow</li>
    <li>CSS tricks</li>
    <li>Developer.mozilla.org - which is the <strong>MDN documentation</strong></li>
    <li>HTML validator (W3) version - copy and pasting the code to see where the errors are.</li>
    <li>Diff Checker - to compare code between your creation and another sites</li>
</ul>

### Building Layouts 

<p>Layouts are ways to build visual structure, instead of just having them in the "normal flow"</p>
<p>There are three ways to make layouts</p>
<ol>
    <li><strong>Float layouts -</strong> older version of layouts that are becoming outdated</li>
    <li><strong>Flexbox -</strong> modern way to build one dimensional layouts - perfect for component layouts. CHECK LECTURE 87 FOR GOOD TRICK FOR FLEX BOX.</li>
    <li><strong>CSS Grid -</strong> perfect for big page layouts and complex components (2 dimensional grid)</li>
</ol>

### Float Layouts 

<p>Float layouts will take the element completely out of the "flow" (i.e. float:'left' or float:'right').</p>
<p>Float elements are still able to create margins around them.</p>
<p>Floats may seem similar to absolute positioning, as the elements are moved "out of the flow" - but text and inline elements will wrap around the floated element. The container will also not adjust it's height to the element and this can result in "collapsing heights". </p>

<strong>Clearing Floats -</strong>: you will need to create a new element (usually a div with the class - clear) and then style it for clear: left, right or both. This is if you have collapsing heights. This is not usually best practice however so you can do the following: create another class for the element you are adjusting and name this clearfix. On CSS you can then create a pseudo property (usually ::after) and then define content (because it has to have some content - even if it is just '') and then display: block, then you can create another property clear: both; and it should do the same thing (rather than making an extra div for each). 

<p>Box-sizing: border box - is a great tool to use in majority of the elements. It takes away from the default box model to make sure that the height and the width are fixed inside the border of an element when designing layouts. If there is extra padding and margins, it will subtract it from the total width to make sure the element does not disappear or go where you don't want it to go. <strong>It is usually applied to the universal selector at the start of the CSS</strong></p>

When styling a container and wanting to center it (i.e. margin: 0 auto) you must provide a specific width. (i.e. width: 1200px). 

## Flex Box 

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

## CSS Grid - 

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

<strong>Instead of having to repeat many grid CSS properties and filling up your stylesheet, it can be good practice to use basic classes in CSS (such as .grid, .grid--2-cols, .grid--3-cols - to create basic grid structures). Then just adding this on top of the class in html - see below</strong> 

.grid {
 display: grid; 
 gap: 1.4rem
 }

 .grid--2-cols {
  grid-template-columns: repeat(2, 1fr) 
  }

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

## WEB DESIGN

Web designers are designers who create the overall look and feel for the web page, whereas web developers implement the design using HTML, CSS and Javascript. 

<strong>10 Ingredients to Good Web Design</strong>

<ul>
    <li><strong>1. Typography (most important):</strong> This is the art and technique of making text beautiful and easy to read. 
        <p>Serif typefaces creates a traditional/luxurious feel and is good for long text. Sans-serif type faces do not have the 'curvy' lines when compared to serif typefaces and gives a more modern look (easier to work with for beginners).</p>
        <p>Some good examples of Sans-serif are: <strong>Inter, Open Sans, Roboto, Monsterrat, Work Sans and Lato.</strong></p>
        <p>Some good examples of serif are: <strong>Merriweather, Aleo, Playfair Display, Cormorant, Cardo, Rubik and Lora.</strong></p>
            <p>Try to limit your typefaces to 1-2 per webpage. </p>
        <p><strong>Font size guidelines:</strong> use a "typescale tool" and normal text should be around 16px-32px in size. For long-text (like a blogpost) text should be 20px-32px. For big headlines, you can go >50px and bold >600, depending on personality. Do not use a font-weight <400 for any text.</p>
            <p><strong>Create a good user experience:</strong> Use less than 75 characters per line, use a line height between 1.5-2 (the more text there is, the bigger the line height), if it looks unnatural - decrease letter spacing, experiment with ALL CAPS for short titles (make them small and bold and increase letter spacing), and don't justify your text (also don't center the text, as this can make it harder to read).</p>
            <p>A good font-size system as is follows: FONT SIZE SYSTEM (px) 10 / 12 / 14 / 16 / 18 / 20 / 24 / 30 / 36 / 44 / 52 / 62 / 74 / 86 / 98</p>
            <p>A good spacing systems as is follows: SPACING SYSTEM (px) 2 / 4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 80 / 96 / 128</p>
    </li>
    <li><strong>2. Colours:</strong> You can use "open colour" and "tailwind CSS" to use custom selected colours.
    <p>You need at least two types of colours in your colour palette - a main colour, and a grey colour (doesn't have to be grey, just a darker shade of a colour). You can also have an accent colour with more experience. </p>
        <p>For diversity, you will need tints (lighter versions of your colour) and shades (darker versions of your colour) which is usually important of your 'grey colour'. To do this you can use tint and shade generator (such as "pallenton.com" and "coolors". </p>
        <p>Use the <strong>Main Colour</strong> to draw attention (such as buttons, headers, and logos).</p>
        <p>You can also link the main colour into images and illustrations to make them stand out. </p>
        <p>On dark coloured backgrounds, try to use a tint (lighter version) of the background for text. </p>
        <p>Text should not be completely black. Lighten it up if it looks heavy and uninviting (and never make the text too light otherwise it'll affect accessibility). To enhance accessibility, you can use the "coolors" tool to make sure the contrast ratio is at least 4.5:1 for normal text, and 3:1 for larger text (>18px). </p>
    </li>
    <li><strong>3. Images & Illustrations:</strong> Different types of images include <strong>product photos, storytelling photos (most important - i.e. a site about journalling showing someone journalling), illustrations (abstract way of doing story telling) and patterns</strong>
    <p>The best websites to get "free" high quality stock photos (if nil other photos are available) are: "Unsplash" - which is the best, "Pexels", "Drawkit" and "UnDraw". 
    </p>
        <p>Show real people to trigger people's emotions.</p>
        <p>Crop your images in order to fit your message.</p>
        <p>Combine photos, illustrations and patterns.</p>
        <p>To handle text on images, it is usually a good idea to darken the image with lighter text, or partially darken an image using a gradient. You can also place the text in an 'image neutral area'. You can also put text in a box. </p>
        <p>You need to account for high resolution screens - make the image dimensions 2 x as big as their displayed size (if it's 300 x 300, the original image should be 600x600). </p>
        <p>You need to compress the image for lower file size and better performance. To do this use "Squoosh" to reduce file sizes.</p>
        <p>When using images side by side, you need to make sure the images are of the same dimensions.</p>
        <p>Uifaces - you can download people's faces for completely free (for icons etc).</p>
    </li>
    <li><strong>4. Icons:</strong> it's best to use a good icon pack such as "Phosphor icons", "ionicons" and "icons8". Don't mix icons from different icon packs.
    <p>Use SVG icons or icon fonts, don't use jpg or png icon files as these may tend to blur on high resolution screens.</p>
        <p>Adjust your icons to fit your website's typography.</p>
        <p>Use icons to create "feature blocks" which can help to describe the features of a website/service. To keep icons neutral, use the same colour as your text. To draw more attention, use brand or different colours.</p>
        <p>Dont make icons bigger than they are designed for - if anything, encase them in a shape.</p>
        <p>To fill outlined icons with a colour - use the "stroke" CSS property. For filled icons, use the "fill" property in CSS.THIS IS SUPER IMPORTANT FOR STYLING ICONS.</p>
        <p>Icons usually have a standard dimension of 24px x 24px</p>
    </li>
    <li><strong>5. Shadows:</strong> The more shadow there is, the further away the element is away from the interface. Shadows help to create depth. Use less shadows for more serious websites. Use light shadows to make things look more natural (mainly on items you want to draw attention to. Use medium sized shadows for bigger elements that you want to stand out. Use larger shadows for navigations and items that float above the rest of the website. To use shadows, use the box-shadow CSS property (or text-shadow CSS property for text - the only difference is that text-shadow does not have the fourth value) - example 20px (horizontal shadow - usually 0px) 20px (vertical shadow) 20px (blur) 10px (scales the shadow as a radius - if you don't specify the fourth it will just automatically be 0 - usually do leave it to 0), color (rgba). The value of shadow should be <0.1 (can look good as 0.07). Usually for shadows you want the light to be coming from the top. 
    The darker the colour of the background, the darker the shadow has to be</li>
    <li><strong>6. Border Radius:</strong> the more border radius, the more playful the website design. You also need to make sure the border radius fits the roundness of the typeface of text. Always use a bigger value than the height of the button (usually the bigger the better if you want to make a round button).If the image is square (not a button), then 50% should make the square a circle.</li>
    <li><strong>7. White Space:</strong> The right amount of white space is important to give objects on the page space to breathe. It's good to add a lot of "white space" between sections and groups of elements. It's always better to have too much white space and go down, than starting with it cramped and going up. It's also good to use a rule of multiples of 16px (but still having smaller values like 2, 4, 8, 16px - from there go up in 16px. </li>
    <li><strong>8. Visual Hierarchy:</strong> This is about establishing more important elements on the page to attract more attention (while defining a path to guide a user through the page). To do this: 
    <p>Position important elements closer to the top of the page (attention will then follow from top to bottom).</p>
        <p>Images draw a lot of attention so you will need to use these mindfully. You will also need to use white space appropriately to highlight important elements.</p>
        <p>For text elements - use font size, font weight, color (both background and text color) and white space to help convey importance. It is important to emphasize title, sub-titles, links, buttons, icons and data points (and then important to de-emphasize less important text like labels or secondary information).</p>
        <p>To establish visual hierarchy bewteen components - use background color, shadow and borders. It is important to emphasize things like testimonials, call-to-action sections, highlight sections, preview cards (if you have two cards or more with images at the top, they need to have the exact same aspect ratio or same dimensions, forms, pricing tables, and important rows/columns.</p>
    </li>
    <li><strong>9. User Experience/Responsiveness (UI/UX):</strong> UI is the graphical interface and UX is the user experience. 
    <p>Goals for UX design is to ensure that the goals are met for both company/business and the user. 
    </p>
    <p>Examples of bad UX design are using pop ups, hiding a cancel subscription button, etc</p>
        <p>Always make your "call to action" more prominent to stand out</p>
        <p>Only use blue text and underlines for links</p>
        <p>Animations should be between 200 to 500ms</p>
        <p>Always only have a singluar line for forms to make it easier to read</p>
        <p>Always have a section to offer user feedback - i.e. when you click submit a form and it says "form has been submitted". </p>
        <p>UX rules include: use descriptive keywords for headlines and don't make them too fancy or wordy.</p>
        <p></p>
    </li>
    <li><strong>10. Components/Layouts</strong></li> - steal like an artist (finding websites that you like, and copy aspects of a certain design to make it fit your own design). Websites that are useful are land-book.com, onepagelove.com, and awwwards.com (in collections and websites) and screenlane.com (for individual components). 
</ul>

<strong>Website Personalities</strong>

<p>You need to have a look at the lecture slides for this - The Website Personalities Framework</p>

<ol>
    <li><strong>Serious/Elegant:</strong> thin serif typefaces, golden or pastel colours and big, high quality images.</li>
    <li><strong>Minimalist/Sipmle:</strong> focuses on essential text content, using small or medium sized sans-serif black text, lines and very few images and icons.</li>
    <li><strong>Plain/Neutral:</strong> neutral and small typefaces with a very structured layout. This is common for big corporations (like Adobe and Microsoft.</li>
    <li><strong>Bold/Confident:</strong> features big/bold typography with confident use of big and bright coloured blocks.</li>
    <li><strong>Calm/Peaceful:</strong> features products and services that care (calming pastel colours, soft serif headings and matching images/illustrations).</li>
    <li><strong>Startup/Upbeat:</strong> modern looking sans-serif type faces, light grey and text backgrounds with rounded elements (commonly used in start up companies).</li>
    <li><strong>Playful/Fun:</strong>Colourful and round designs, fueled by creative elements like hand-drawn icons, illustrations and fun languages.</li>
</ol>

## Components and Layouts (Rule no. 10) 

<p>Elements are organised into components, which are then formed into layouts (with patterns) and then made into the web page.</p>
<p>Have a look at Lecture 86 for inspiration of elements (i.e. text, inputs, images, tags). </p>
<p>Common components can be: breadcrumbs, pagination, alert and status bars, statistics (usually about the service), image galleries, feature boxes, preview and profile cards, accordions (usually for FAQ), TABS (for data that you want to initially hide until clicked), Carousel, Customer Testimonials, Customer Logos, Featured-In Logos (usually appears after the HERO section), Steps (showing a customer how to get/use the product - best way to show how your product works), Forms, Tables (for specifications etc), Pricing Tables, and Modal Windows (usually a window that pops up for sign ins and sales - marketing pop up windows). </p>

To hide an accordion box - the easiest thing to do is set the display of the content to none. To set it back - display: block.

To design testimonials, a common way is to use a "blockquote" element. 

The transform CSS property can be used to "scale" images - i.e. transform: scale(1) - will keep the image the same size, transform:scale(2) would mean that the image would double in size. You can also use transform CSS property to translate an element across the page - i.e. transform: translate(x,y) - x: horizontal, y: vertical. An example would be to move an object halfway down the page/of the element you would use transform: translate(0, -50%) - as this would move the element down 50% of the ACTUAL element's height (as opposed to using the height of the parents). 

Tables aren't really used in CSS anymore (due to flex box and grid) - but still have a place when having to display data. This is done through the <"table"> element. Inside the table element you have <"tr"> which is the "table row" and then inside of the "tr" you used the <"td"> element which contains the data. In order to give the table a heading, you need to wrap the particular <tr> section into a <"thead"> element (inside of this thead - you need to change the td to th values. You would then wrap the rest of it in <"tbody"> element. You can also use <th> elements inside of the tbody elements as well, to emphasize the text. Th elements will also center. 

To create "zebra stripes" in tables, you would just use the pseudo selector :nth-child(odds) and :nth-child(evens) to change the background colours.

Border-collapse CSS property can help to get rid of borders that are too close together. You would write border-collapse: collapse. This can also get rid of gaps between columns in tables. 

<strong>Hero sections:</strong> Hero sections are sections that you usually see on a website's home page. The most common is where the text is on one side and then an image is on the other. The next most common is where there is background image and then text on the top (this is becoming less popular). You can have a hybrid layout too (which is a mix of the two). <strong>The hero section should always be slightly wider than the rest of the content</strong>. Hero sections should always have a class .hero (not a .container). 

<strong>Call to action sections</strong> usually come at the end of the page where we want the user to take some 'action' - usually above the footer. Usually this will need to stand out using some visual hierarchy. Call to action sections can also be used to get the user to contact the company (just using contact details or forms). 

Pricing usually comes just before the call to action section. 

<strong>Feature rows</strong> usually have an image on one side, text on the other side (heading + description + button) that describes a specific feature. 

## Layout Patterns 

<ol>
    <li>Rows of cards/boxes</li>
    <li>Grids of cards/boxes</li>
    <li>Asides - you can also nest patterns inside of components</li>
    <li>Z pattern - using a "Z" pattern for the eyes that moves down the page from top to bottom left to right - usually 3 rows are used, but more can also be used</li>
    <li>F pattern - Always has images on the one side (so they are fixed) with content on the opposite side.</li>
    <li>Single columns - usually just used for mobile and side bars</li>
    <li>Sidebars - can be used for blogs or options in a web application, table of contents, or summary.</li>
    <li>Multi-column/magazine layout</li>
    <li>Asymmetrical layouts</li>
</ol>

In order to create an image in the background - you should apply the CSS property - background-image: url(). To change the size, you will use background-size: cover (can use contain, but cover is better in some cases). 

If you have to go "one level up in the file tree" on VS code you will need to do background-image: url("../ - to find the folder. The same case would be for two levels up background-image: url("../../ - etc. 

background-position: center etc - can be used to position an image. 

<strong>How to darken background images:</strong> in order to do this, you need to create a background linear gradient. This would be by using the following: background-image: linear-gradient(rgba(34,34,34,0.6), rgba(34,34,34,0.6), url(img); - you have to use rgba in order to create opacity. This obviously doesn't have to be the above - you can use any other colours. Using greys can give "a softer touch". 

To create a background with a gradient, you will need to use the following: 
background-image: linear-gradient(). In the parenthesis you would have degrees first (90deg would mean gradient would be left-right and 180deg would be up and down) OR you can have "to right" (without the comma's), "to left", "to right bottom" etc. 

<strong><'menu'></'menu'></strong> is an HTML element for web applications. It differs from a NAV element, as nav elements contain links to point to other places in the application. Menu is for menu buttons in a web application. This isn't really used unless you are building a web application.

When wanting to put space between elements on a page - you can use the margin (whether that be margin-left, margin-right) to auto and this would mean that the element would occupy all of the space needed (and then push out through the content). 

Setting overflow (CSS property) to scroll will help to create a scroll bar (usually when elements don't fit in the container). Setting overflow: hidden can help if the top part of your card/image is not inheriting the border radius.

## 7 steps to a great website

<ol>
    <li><strong>Define and plan the project</strong>
    <p>Who is the project for? What is the website for? (providing information, selling something, or entertaining) and you need to define the business and user goals (lecture on UX), define a specific target audience for the website (usually comes from the client)</p></li>
    <li><strong>Plan</strong>
    <p>Plan and gather the website content (images, text, videos - usually provided by the client), plan the sitemap for bigger websites (what pages the sites need, and how they are related to eachother), plan what sections each page needs in order to convey the content's message, and finally define the website personality</p></li>
    <li><strong>Sketch</strong>
    <p>Think about what components you may need and how you can use them in layout patterns (get inspiration from the web design section UDEMY), start sketching on pen and paper or FIGMA (digital design software), you don't need to sketch everything and don't need to make anything perfect. An example would be if a client wants a landing page (which is one page for a website).</p>
    </li>
    <li><strong>Design & Build</strong>
    <p>Do the actual design in code, choose and apply actual visual styles for your design (which need to be based on the website personalitie and what you have got from inspiration), use the client's branding for design decisions where possible (colours, typography, icons)</p>
    </li>
    <li><strong>Test & Optimise</strong>
    <p>Make sure website works in all major browsers (chrome, firefox, safari, edge), test on actual mobile devices, optimise all images (make sure dimensions are right and that they are compressed so users do not have to download big images), fix accessibility problems (e.g. colour contrast), run the Lighthouse performance tool in Chrome DevTools to try and fix reported issues, think about SEO (search engine optimisation)</p>
    </li>
    <li><strong>Launch</strong>
    <p>Upload website to hosting platform (netlify), choose and buy a great domain name for your website (memorable and easy to write), </p>
    </li>
    <li><strong>Maintain & Update</strong>
    <p>If you're with a client, create a monthly maintenance contract with your client and install some analytics software (google analytics, Fathom to give you stats about your website users - to adapt website structure and content), A blog is also a great way to keep users coming back to the website (and good for SEO)</p>
    </li>
</ol>

## RESPONSIVE WEB DESIGN 

A technique used to make a webpage adjust it's layout to a specific screen size (makes websites usable on all devices). 

<ol>
    <li><strong>Fluid layouts -</strong> allows the website to adapt to the viewport width/height. Use percentages instead of pixels. Always use the max-width property instead of the width property. The usual default is 1200px or 120rem (or sometimes also 1140px). 
    </li>
    <li><strong>Responsive units -</strong> using the 'rem' unit instead of pixels. This makes it easy for us to scale the entire page up or down automatically. 1rem is set to 10px - this makes it easy for us to calculate the length.</li>
    <li><strong>Flexible/fluid images -</strong> images behave differently to text content as they do not scale automatically when we change the viewport. We usually do this by using percentages for image dimensions with the max-width property.</li>
    <li><strong>Media queries -</strong> this brings all of the other ingredients together. This allows us to change CSS styles on certain viewport widths (or break points). This allows us to create different websites for different types of devices.</li>
</ol>

<strong>Desktop first vs mobile-first development</strong> - it is easier to learn desktop first development (then using media queries to shrink as you go). Designing mobile-first forces us to reduce websites and apps to the absolute essentials (this is the more modern way to design websites). 

<strong>max-width</strong> property will make the element flexible because it will adapt to the viewport width. 

<strong>REM (root element font size)</strong> the root of the document is the html document. If you don't define any font size, 1rem is equal to the browser's default font size (which the default is 16px). 

How to get rid of JANKY borders: the reason why the borders become JANKY is due to the border being added to the outside of the element. To fix this you need to add the border to the INSIDE of the button. To fix this - instead of using the border property, you use the box-shadow property (below): 

Instead of doing - border: 3px solid #fff; 
You do this - box-shadow: inset 0 0 0 3px #fff; 
The inset will help with creating the border on the inside of the button. 

For button hover transitions - all 1s; (this would help to change the colour of your link and visited buttons (that have the main styling/original state) over a period of 1s. The transition property helps to change one property from one value to another. A usual value is 0.3. The third value of a transition is the ease attribute. 

Adding a "helper class" i.e. .margin-right-sm will mean that you can add margins to a class without having to completely write new code or wrap the component you want to add a small margin to in divs/flex boxes. You can then add this to the elements you would like to move by certain rem to the right. With these you would usually add the !important key word (i.e. margin-right: 1.6rem !important; 

<strong>Z index</strong> helps to position an item in front or behind anothe element (a minus element means that it will go behind, and positive means it will go in front) - as long as it is a higher number it will go in front. 

When using ionicons - you need to copy the script from their website (which is now really hard to find - so copy this (<script src="https://unpkg.com/ionicons@5.4.0/dist/ionicons.js"></script>) and paste it in your html just before the body element ends. 

role attribute: describes the role of an element in programs that can make use of it, such as screen readers or magnifiers. So role="img" would tell the screen reader that it is an image. This would usually be accompanied with an aria-label which helps to describe the content. aria-label="woman enjoying food". 

For forms, it is important to structure them like this: 
<'form' 'class'='form' action='#'> - this would usually have a url to send the information to
<'label' (which tells the user what to put into the input usually) 'for'='full-name' (the for property can help to link the label to the input's id)>Full Name</'label'>
<'input' id='full-name' type='text' placeholder='John Smith'/> 
etc... 
</'form'>

To style a placeholder - you can use the input::placeholder (pseudoelement) to change the colour. 

You usually do not give forms classes due to the many attributes they have. You usually would just style the descendant selector i.e. .cta-form label {}, .cta-form input etc. To put the label and the input on seperate lines, you would need to make the label element display: block; 

A <'select'> box can create a select box but requires you to have <'option'> in between them i.e. 

<'label' for="select-where">WHere did you hear from us?<'/label'>
<'select' id="select-where"><option value="Friends"'>Friends & Family</'option'>
</'select'>

The required property works on input and select elements. 

On input elements, to make them wider you would usually make the width: 100% to make them as wide as the parent (while also adding some padding). Input and button elements do not inherit the font from the body - but you can force them to by: font-family: inherit; which will inherit the font from the parent. You can also do this with colours. You want to remove the border of the input too. It is also a good idea to make a box-shadow of input fields: i.e. (0 1px 2px rgba(0, 0, 0, 0.1); and with/without border radius and background color. 

<strong>A focus state</strong> is when you hover over an input and the background goes blue. Or same if you press tab on the page and it goes to the buttons (makes it easy for users that only use a keyboard to get through the page). To style this on the page, you will need to create a general CSS class of: *:focus { outline: none AND it is nice to add a box-shadow to ensure accessibiilty is there - DO NOT LEAVE IT WITH NO OUTLINE. A box-shadow instead of border-radius will ensure it just creates an even shadow around the element.

When designing footers, it is important to have the address in an <'address'> element. You can also create specific anchor tags which describe and utilise phone numbers and emails. Examples below: 

Phone: <'a href="tel:0211991223"'>0211991223</a'>
Email: <'a href="mailto:jamesbickertonaut@gmail.com">jamesbickertonaut@gmail.com</a'>

The address element has default formatting of italic, so you need to change

#Media Queries 

<strong>Media queries are tools to override specific parts of our CSS at certain viewport widths</strong>. It's a good idea to create a new CSS file for your media queries. 
How media queries work with max-width: This max-width will decide whether or not the media query will still apply. So a max-width of 600px (which is the 'breakpoint') for example will mean the styles will apply until AFTER 600px (where the styles will then no longer work).

Breakpoints:
<ul>
    <li>Most phones are between 300-500px. Usually good to do a final media query at around 600px</li>
    <li>Most tablets are between 600-900px</li>
    <li>Most landscape tablets are between 900-1100px</li>
    <li>Most desktops are 1200px and above - important to do 1200px</li>
</ul>

It is important to set breakpoints where the design breaks down. We usually put these break points where the design starts to "look weird and out of place". 

If there are conflicting styles with the media query, it is the style that appears last that overrides. 

<strong>Media queries do not respond to the basic setting of font-size: 62.5% in the html settings. 1rem does not equate to 10px (1rem will always be the default browser font size setting). Media queries should have a range between 200px. 

rem and em do NOT depend on html font-size in media queries. Instead we assume 1rem = 1em = 16px. We should not use rem in media queries, we should use em (which are the exact same). Which means if you have a 1200px value where it looks weird, you would divide it by 16 to get the rounded number for your breakpoint. 

When display is set to "none" animations will not work. To hide an element (like a nav when doing media-queries for mobile devices) without using display:none - you can do this: 

1. Hide the element visually
    opacity: 0;
2. Make it unaccessible to mouse/keyboard
    pointer-events: none;
3 Hide it from screen readers
    visibility: hidden;

On the open class (i.e. nav-open) you would then need to make the opacity: 1, pointer-events:auto, and visbility: visible (to reverse it). 
