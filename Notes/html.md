# HTML & UDEMY COURSE NOTES (HTML & CSS NOTES) - BASICS

Headers can be h1-h6

<strong><'em'></strong> is a tag to make things italic and <strong><'strong'></strong> is a tag to make things bold - this is more semantic and better practice when compared to <'i'> and <'e'>.

Comments can be made using the <!--task still to do->

<'meta charset="UTF-8/'> - meta stands for meta data (data about the data). Charset is the character set and then UTF-8 encapsulates all the characters we use in the english language.

A good structure to have at the top of your CSS stylesheet is as follows: 

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
<li><'input type="button"'></li>

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

# Conflicts between SELECTORS (IMPORTANT PART OF CSS)


