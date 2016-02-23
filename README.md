# HTMLWorkshop

## Useful Links for this Tutorial
* https://developer.mozilla.org/en-US/docs/Web/HTML/Element
* https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes
* https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started

## The Beginning

We're going to begin our journey into HTML with the beginner.html file. Let's take a look at the following snippet from the file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<title>Homepage</title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" type="text/css" href="style.css"/>
</head>
<body>
	<h1> WHADDUP </h1>
	<h2> whaddup </h2>
	<p> whaddup whaddup whaddup whaddup. whaddup? whaddup! </p>
	<ul>
		<li> whaddup </li>
		<li> whaddup </li>
		<li> whaddup </li>
	</ul>
</body>
</html>
```

You can think of HTML as a set of rules that dictates how a webpage will be formatted and presented. These "rules" come in the form of "tags". When your browser is loading an HTML page, it goes through the above chunk of HTML, and structures the webpage that we will see based off these tags. The **html** tag tells the browser that we're dealing with an HTML document, and the **body** tag is where we'll be putting all the website's displayable content. We'll come back to the **head** tag later. Try going to your browser and click **File->Open File**, then navigate to where your beginner.html file is located and click **Open**. 

As you can see, all the "whaddup"s we placed in our body tag are showing up on the webpage. But, the way these "whaddup"s are arranged on the page and how they appear to the viewer is dictated by each of the **tags** we put around each "whaddup". The first tag is the **h1**, or heading, tag. Pretty self-explanatory, it just tells the browser to make the text surrounded by the tag to be the heading of the page. The second tag is the **h2** tag. This tag is essentially a toned down version of **h1**. The third tag is the **p**, or paragraph. Generally, big chunks of readable text are supposed to go inside **p** tags, hence the long sequence of "whaddup"s. The **ul** tag stands for unordered list. They're meant for lists of text, hence we see each "whaddup" preceded by a bullet point.

So, those are some of the most basic tags we can use in HTML. Now that we're getting a sense of how HTML is used to structure content on a webpage, let's dive into some of the more interesting elements of making a webpage, namely CSS. CSS stands for Cascading Style Sheets, and it's used to style a webpage. It allows us to do things like set the font size and type of text, use background colors and images, set margins for the page, and many others. Let's take a look at some example CSS:

```css
p {
	font-size: 40px;
	color: blue;
	margin-top: 100px;
	margin-bottom: 100px;
}
```

The above CSS snippet applies all the stylistic elements within the curly braces to every piece of text surrounded by a **p** tag in our HTML document. Using the previous HTML example, all the "whaddup"s within the **p** tag would now have a font size of 40 and have a blue text color. But, what if we don't want to change the font size and color of **all p** elements on our webpage, only specific ones? Let's modify the above HTML a little:

```html
<p class="whaddupText"> whaddup whaddup whaddup whaddup. whaddup? whaddup! </p>
<p> second whaddup paragraph </p>
```

Let's also change the CSS to:

```css
p {
	font-size: 20px;
	font-family: Helvetica;
}

.whaddupText {
	color: blue;
}
```

In the HTML, we added this mysterious **class="whaddupText"** line. This allows us to specify style for specific elements in our HTML. You can assign a **class** to any tag in HTML, and set its corresponding style in CSS by prefacing the classname with a "." and adding whatever featues you want. In this case, I made it so that all text in **p** tags have a font-size of 20 and use the Helvetica font. But, since only the first **p** tag has the **class="whaddupText"**, only the text within that first **p** tag will have a font-color of blue. Try opening the webpage and see what happened!

Just for example's sake, let's assign a class to our first **li** tag and make it have a background color of red in our CSS. Let's also make all the text in our bullet list have a font-size of 30px. The following HTML and CSS snippets will accomplish this:

```html
<li class="firstBullet"> whaddup </li>
```

```css
ul {
	font-size: 30px;
}

.firstBullet {
	background-color: red;
}
```

Note again how if you assign a class to an element, you must but a "." before its name, which is unlike assigning style to a certain tag, such as **ul**.

So, this was a very bare bones introduction into HTML and CSS. Both of the two languages offer a ton of more features that are also really useful, but we won't be able to cover all of them today unfortunately. But, now that we have a basic understanding of how things work, let's start making our personal websites.

## Personal Site

We're going to be building a personal website with four pages including a home page, a bio/resume page, a favorite movie quotes page, and a miscellaneous page with whatever your heart desires on it. The homepage will link to the the other three pages, and the other three pages will link back to the home page. All the pages are going to have a similar feel to them in terms of design and style, so we'll be making several CSS classes to help us do this.

Let's start with the home.html page. So far we just have a blank html page:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<title>Homepage</title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link href="http://fonts.googleapis.com/css?family=Pacifico%7COpen+Sans:300,400,700" rel="stylesheet" type="text/css"/>
	<link rel="stylesheet" type="text/css" href="style.css"/>
</head>
<body>
</body>
</html>
```

We want to have three links to our pages, and HTML provides us with an **a** tag that will allow us to do this. Let's first create three new files in the same directory as home.html called: bio.html, quotes.html, misc.html. Now let's edit the above HTML inside the **body** tag:

```html
<body>
	<a href="bio.html"> My Biography </a>
	<a href="quotes.html"> My Favorite Movie Quotes </a>
	<a href="misc.html"> Learn s'more about me! </a>
</body>
```

So, there's a new tag I just introduced here called the anchor or **a** tag. These tags are meant to insert links into an HTML page. We tell the browser where to direct the viewer of the site when they click a link by setting the **href** attribute of the **a** tag. In this case, we direct users to each of our three pages that are part of the website. We also could have done something like:

```html
<a href="http://www.google.com"> CLICK TO GO TO GOOGLE </a>
```

and the browser would have directed us to google when we click the link. Alright, now let's also put some bare bones text in each of the three HTML files we just created so we'll actually see something when we click on each of the links from the homepage. Just copy and paste the following HTML into each of those three files:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<title>Homepage</title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link href="http://fonts.googleapis.com/css?family=Pacifico%7COpen+Sans:300,400,700" rel="stylesheet" type="text/css"/>
	<link rel="stylesheet" type="text/css" href="style.css"/>
</head>
<body>
	FILL ME IN LATER
</body>
</html>
```
Now try opening home.html in your browser and you should be able to click on any of the three links and the browser will take you to an HTML page that just displays the "FILL ME IN LATER" text. Our homepage looks incredibly dull right now, so let's add some style to our links to spruce the page up a bit. First, let's make all the **a** tags we added above belong to a CSS link class like so:

```html
<a href="bio.html" class="link"> My Biography </a>
<a href="quotes.html" class="link"> My Favorite Movie Quotes </a>
<a href="misc.html" class="link"> Learn s'more about me! </a>
```

Now we can go to our style.css file and start adding stylistic elements to all the above links. First, let's make the links have a nicer and bigger font, be centered on the page, and put some nice borders on the links. We can edit the style.css like so to accomplish this:

```css
.link {
	display: block;
	text-decoration: none;
	margin-left: auto;
	margin-right: auto;
	margin-top: 15px;
	margin-bottom: 15px;
	font-size: 16px;
	font-family: Helvetica;
	font-weight: 700;
	border: 1px solid #f15f5d;
	text-align: center;
	color: #f15f5d;
	width: 20%;
}
```

So, there's a lot of new things going on here. First, set the text-decoration to none, which gets ride of the default underlines under all links in HTML. We then set the left and right margins of each the links to **auto**. This tells the browser that, whatever the width of the screen, I want even margins on both the left and the right side of the element, effectively centering it. We also set the font size, weight, and family to be more appealing. For the boder attribute, we specified three things. The first is 1px which is the thickness of the border, followed by a solid line border, followed by the color of the border. The text-align: center attribute is fairly self-explanatory. I set the color of the border and the text to the hex color **#f15f5d**, which is a light shade of red, but you can change this to anything you like. Just google hex color finder to find the code for the color you like most!

As the page stands now, it seems like the link text inside the border is too close to the border. Let's let the text breathe a little by using the **padding** attribute in CSS. Padding allows us to add space in between the text and the border. We can add padding to the top, bottom, left, and right of the text like so:

.link {
	padding-right: 30px;
	padding-left: 30px;
	padding-top: 15px;
	padding-bottom: 15px;
}
```
Now, if you refresh the page, the links shouldn't look as scrunched up as they used to. Now, I personally don't like square boxes that much, I like a little bit of roundness in them. We can make our borders rounded by setting the border-radius attribute like so:

```css
.link {
	border-radius: 3px;
}
```

This will give us very subtly rounded edges around our border. 

HOME
-> First show how to use img tag with src="some link from online"
-> Then show how to use a tags with src="some file in same dir as home.html"
-> Then show how to make links cool by turning them into buttons with a nice border, font, and color
-> Then introduce to div tags and show how to center things on a page with margins and display: block

OTHERS
-> Show how to make nice textboxes with padding, background color, and Helvetica font
-> Use ul tags and li tags for lists on the bio page



















