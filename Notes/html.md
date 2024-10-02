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
