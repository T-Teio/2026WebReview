# 2026WebReview
ah $hit here we go again
HTML Review

What does HTML stand for
Hypertext Markup Language

What is the differencec between <head> and <body>?
<head> --> Metadata - read by the browser
<body> -->This is the content DISPLAYED in the browser

Name THREE semantic HTML elements.
<header></header>
<footer></footer>
<main></main>
<nav></nav>
<article></article>
<aside></aside>
<section></section>

What attribute does an <a> tag need to create a link?

    href --> <a href="https://www.google.com">

What is a self-closing HTML tag? Give an Example
Are tags that do not have closing tags, also known as Void Elements
<br>
<img>
<link>
<meta>

What does <!DOCTYPE html> do?
This tells the browser that the file is an HTML file.

Every HTML file has the same SKELETON (Boilerplate, template) structure:

<!DOCTYPE html>
<html lang="en">
<head>
    <title></title>
    <link>
    <style></style>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width", initial-scale="1.0">
        - Makes the page Responsive
</head>
<body>
    <header>
        <nav>Contains any Navigation bar elements</nav>
    </header>
    <h1>largest heading/most important heading</h1>
    <!-- ALL VISIBLE elements go inside the body -->
</body>
</html>

Part 2 : Core HTML Elements
Heading 1 - 6
<h1> --> There should be only 1 <h1> per page
<h2> --> section titles, subtitles
<h3> --> sub-sections
<h4>
<h5> --> Fine print (Copyright, statements, etc)
<h6> --> Finer print (Copyright, statements, etc)

Text elements
<p> --> paragraph tag
<strong> --> bold / important text - semantic weight
<em> --> italic / emphasized text - semantic weight
<br> --> line break (void element)
<u> --> underline
<hr> --> Horizontal row --> visual line divider (void element)
<span> --> inline element, does not create a line break

HTML Lists

Unordered List - bulleted list
- Used for : Items with no ranking order
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>


Ordered List --> numbered or alphabetized
- used for steps, rankings, sequences, etc
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>

Links

How do I create a link to sllboces.org?
<a href="https://sllboces.org" target="_blank">SLL BOCES</a>

How do I create a link to about.html - relative path (page in the same directory)?
<a href="about.html">About</a>

Link to a file in the content folder?
<a href="content/page.html">Page</a>

A link to another section of the page?
<a href="#about">Junp to About section</a>

A link to send an email?
<a href="mailto:student@sllboces.org">Email Me</a>

Images
What are the two required attributes for <img> tags
alt - accessibility text
src - file path to the Image
<img src="images/hero.jpg" alt="Adirondack Mountains in fall">
<img src="images/logo.png" alt="SLL BOCES Logo">

What is hot-linking an image?
- linking to an image somwhere on the internet
- Placeholder images for design purposes
- Replace hotlinks before publishing the site
- If the hotlinked image gets moved, it will break your design

<img src="https://google.com/2/abc/file/images/myGoogleImage.png" alt="my hotlinked image">

SEO - Search engine optimization - how search engine rank well structured pages

Semantic tags replaced the use of <div> tags:
    <div class-"header"> vs <header>
Layout Semantic Elements: header, nav, main, section, aside, footer

Content Semantic Elements:
<figure></figure> - image with caption
<figcaption> - caption for figure image
<time> - a fate or time value
<address> - contact address info
<mark> - highlighted text
<details> / <summary> -expand and collapse more details
<div> - non semantic container

/* --- CSS --- */

:root {

--color-navy: #003366;

--color-gold: #F5A800;

--color-white: #FFFFFF;

--font-main: 'Segoe UI', Arial, sans-serif;

--spacing-md: 1.5rem;

}

/* Using variables */

nav {

background-color: var(--color-navy);

font-family: var(--font-main);

padding: var(--spacing-md);
}

/* --- ELEMENT --- */
h1 {

color: #003366;

font-size: 2rem;

}

/* --- CLASS --- */
.project-card {

border: 2px solid #F5A800;

padding: 1rem;

}

/* --- ID --- */
#hero {

height: 400px;

background-image:

url('img/hero.jpg');

}


/* --- BOX MODEL --- */

.card {

/* Content */

width: 300px;

height: auto;

/* Padding (inside) */

padding: 1rem;

/* Border */

border: 2px solid

#F5A800;

/* Margin (outside) */

margin: 1.5rem;

/* Modern fix */

box-sizing: border-box;

}

/* --- COLORS --- */

color: #003366; /* hex */

color: rgb(0, 51, 102); /* rgb */

color: rgba(0,51,102,.8); /* + opacity */

color: navy; /* named */

background-color: var(--color-gold);

/* --- BACKGROUND --- */

#hero {

background-color: #003366;

background-image:

url('images/hero.jpg');

background-size: cover;

background-position: center;

background-repeat: no-repeat;

/* Overlay technique:

position + pseudo-element */

position: relative;

}

/* --- FLEXBOX --- */

nav {

display: flex; /* Activate Flexbox */

/* Main axis alignment */

justify-content: space-between;

/* Options: flex-start | flex-end

center | space-between

space-around | space-evenly */

/* Cross axis alignment */

align-items: center;

/* Options: flex-start | flex-end

center | stretch | baseline */

flex-wrap: wrap; /* Allow wrapping */

gap: 1rem; /* Space between items */

}

/* --- HERO SECTION --- */

#hero {

background-image: url('images/stlawrence.jpg');

background-size: cover;

background-position: center center;

background-repeat: no-repeat;

min-height: 450px;

display: flex;

align-items: center;

justify-content: center;

position: relative;

}

/* Dark overlay so white text is readable */

#hero::before {

content: '';

position: absolute;

inset: 0; /* top/right/bottom/left: 0 */

background: rgba(0, 51, 102, 0.6);

z-index: 1;

}

/* Text above the overlay */

.hero-content {

position: relative;

z-index: 2;

color: #FFFFFF;

text-align: center;
}

/* --- FOOTER --- */

footer {

background-color: var(--color-navy);

color: var(--color-white);

padding: 3rem 2rem 1.5rem;

}

.footer-nav {

display: flex;

flex-wrap: wrap;

gap: 2rem;

justify-content: space-between;

margin-bottom: 2rem;

}

.footer-column {

flex: 1 1 180px; /* grow | shrink | min-width */

}

.footer-column h4 {

color: var(--color-gold);

font-size: 0.875rem;

text-transform: uppercase;

letter-spacing: 0.1em;

margin-bottom: 0.75rem;

}

.footer-column a {

display: block;

color: rgba(255,255,255,0.75);

text-decoration: none;

padding: 0.25rem 0;

transition: color 0.2s;

}

.footer-column a:hover {

color: var(--color-gold);

}