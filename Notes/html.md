# FREECODECAMP COURSE NOTES (HTML & CSS NOTES) - BASICS

Headers can be h1-h6

Comments can be made using the <!--task still to do->

The style of code can begin with the following structure: 

<!--DOCTYPE html>
    <html lang="en"> - means the default language is english
    <head>
    <meta charset="UTF-8"> - standard for most sites
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> - standard
    <title>Title of Document</title>
    <link rel="stylesheet" href="styles.css"/>
        </head>
            <body>
                <header>
                    </header>
                    <main>
                        </main>
                            </body>
                                <footer>
                                    </footer>
                                        </html><-->

A good structure to have at the top of your CSS stylesheet is as follows: 

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box; 
}
<<<<<<< Updated upstream
=======

<b><'img'></b> tag is a self closing tag and usually require a source and alternate comment. For example: 

<'img src="link-of-photo" alt="picture-of-dog"'>

<b><'a'></b> tags are anchor tags that source links from another page and are not self-closing tags.

<b><'a href="link to website">Click for link</a'></b> - this would be an example, which would translate to: <a href="link_to_website">Click for link</a>.

Usually anchor tags should also have a target which makes sure the link opens in a new tab. For example: 

<b><"a target="_blank" href="link to website"><img src="link-to-picture" alt="picture-of-dog"/></a"></b> which would equal - <a target="_blank" href="link_to_website"><img src="link-to-picture" alt="picture-of-dog"/>

You can also nest a the </b><'img'></b> information within a <b><'figure'></b> element and use <b><'figcaption'>This is my dog</figcaption></figure'></b> as a caption under the img.

listed items can be ordered <b><'ol'></b> or unordered <b><'ul'><b/> and between these elements will require <b><'li'></b> elements.

<b><'form'></b> elements can be used to submit form information on your website. These are usually paired with <b><'action'></b> elements which indicate where the form is sent to. For example: 

<b><'form action="url">information</form'></b> - the url is obviously where the information is sent to. 

<b><'input'></b> elements also do not require closing tags. They have multiple types which can be seen below (but not limited to): 

<ul>
<li><'input type="button"'></li>

<li><'input type="checkbox"'></li>

<li><'input type="date"'></li>

<li><'input type="email"'></li>

<li><'input type="submit"'></li>
</ul>

input elements require <b><'label'></b> elements to define the values. 
