# FREECODECAMP COURSE NOTES (HTML & CSS NOTES) - BASICS

Headers can be h1-h6

Comments can be made using the <!--task still to do->

The style of code can begin with the following structure: 

<!DOCTYPE html>
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
                                        </html>

A good structure to have at the top of your CSS stylesheet is as follows: 

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box; 
}
<<<<<<< Updated upstream
=======

<img> tag is a self closing tag and usually require a source and alternate comment. For example: 

<img src="link-of-photo" alt="picture-of-dog">

<a> tags are anchor tags that source links from another page and are not self-closing tags.

<a href="link to website">Click for link</a>

Usually anchor tags should also have a target which makes sure the link opens in a new tab. For example: 

<a target="_blank" href="link to website"><img src="link-to-picture" alt="picture-of-dog"/></a>

You can also nest a the <img> information within a <figure> element and use <figcaption>This is my dog</figcaption></figure> as a caption under the img.

listed items can be ordered <ol> or unordered <ul> and between these elements will require <li> elements.

<form> elements can be used to submit form information on your website. These are usually paired with <action> elements which indicate where the form is sent to. For example: 

<form action="url">information</form> - the url is obviously where the information is sent to. 

<input> elements also do not require closing tags. They have multiple types which can be seen below (but not limited to): 

<input type="button">

<input type="checkbox>

<input type="date">

<input type="email">

<input type="submit">

<input> elements require <label> elements to define the values. 

>>>>>>> Stashed changes
