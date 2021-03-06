# HTMLWorkshop

## Useful Links for this Tutorial
* https://developer.mozilla.org/en-US/docs/Web/HTML/Element
* https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes
* https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started
* https://pages.github.com/
* http://startbootstrap.com/template-categories/all/

## The Beginning

We're going to begin our journey into HTML with the beginner.html file. Create a directory somewhere on your system and create a file called beginner.html within that directory. Copy and paste the following snippet of HTML into beginner.html:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<title>Homepage</title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" type="text/css" href="beginner.css"/>
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
	<img src="https://i1.sndcdn.com/artworks-000138786392-3da84t-t500x500.jpg" alt="suh dude"/>
</body>
</html>
```

You can think of HTML as a set of rules that dictates how a webpage will be formatted and presented. These "rules" come in the form of "tags". When your browser is loading an HTML page, it goes through the above chunk of HTML, and structures the webpage that we will see based off these tags. The **html** tag tells the browser that we're dealing with an HTML document, and the **body** tag is where we'll be putting all the website's displayable content. We'll come back to the **head** tag later. Try going to your browser and click **File->Open File**, then navigate to where your beginner.html file is located and click **Open**. 

As you can see, all the "whaddup"s we placed in our body tag are showing up on the webpage. But, the way these "whaddup"s are arranged on the page and how they appear to the viewer is dictated by each of the **tags** we put around each "whaddup". The first tag is the **h1**, or heading, tag. Pretty self-explanatory, it just tells the browser to make the text surrounded by the tag to be the heading of the page. The second tag is the **h2** tag. This tag is essentially a toned down version of **h1**. The third tag is the **p** tag, or paragraph tag. Generally, big chunks of readable text are supposed to go inside **p** tags, hence the long sequence of "whaddup"s. The **ul** tag stands for unordered list. They're meant for lists of text, hence we see each "whaddup" preceded by a bullet point. Next, we have the **img** tag, which tells the browser to insert the image from the url inside the **src=""** part of the tag. 

So, those are some of the most basic tags we can use in HTML. Now that we're getting a sense of how HTML is used to structure content on a webpage, let's dive into some of the more interesting elements of making a webpage, namely CSS. CSS stands for Cascading Style Sheets, and it's used to style a webpage. It allows us to do things like set the font size and type of text, use background colors and images, set margins for the page, and position elements on a webpage to where we want them to go. Let's take a look at some example CSS:

```css
p {
	font-size: 40px;
	color: blue;
	margin-top: 100px;
	margin-bottom: 100px;
}
```

Create a file called beginner.css in the same directory as beginner.html and paste the above snippet into the beginner.css file. The above CSS applies all the stylistic elements within the curly braces to every piece of text surrounded by a **p** tag in our HTML document. Using the previous HTML example, all the "whaddup"s within the **p** tag would now have a font size of 40 and have a blue text color. But, what if we don't want to change the font size and color of **all p** elements on our webpage, only specific ones? Let's modify the above HTML a little:

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

In the HTML, we added this mysterious **class="whaddupText"** line. This allows us to specify style for specific elements in our HTML. You can assign a **class** to any tag in HTML, and set its corresponding style in CSS by prefacing the classname with a "." and adding whatever features you want. In this case, I made it so that all text in **p** tags have a font-size of 20 and use the Helvetica font. But, since only the first **p** tag has the **class="whaddupText"**, only the text within that first **p** tag will have a font-color of blue. Try opening the webpage and see what happened!

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

## Building our First Site

We're going to be building a personal website with four pages including a home page, a bio/resume page, a favorite movie quotes page, and a miscellaneous page with whatever your heart desires on it. The homepage will link to the the other three pages, and the other three pages will link back to the home page. All the pages are going to have a similar feel to them in terms of design and style, so we'll be making several CSS classes to help us do this. We'll build the homepage and the movie quotes together, and then you should be able to use what you learned to build the other two pages.

Start by creating a home.html file, again in the same directory as the two beginner files, and paste the below HTML into home.html.

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

and the browser would have directed us to google when we click the link. Alright, now let's also put a little text in each of the three HTML files we just created so we'll actually see something when we click on each of the links from the homepage. Just copy and paste the following HTML into each of those three files:

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

Now, create file called style.css in the same directory as home.html so we can start prettyfying our webpage. First, let's make the links have a nicer and bigger font, be centered on the page, and put some nice borders on the links. We can edit the style.css like so to accomplish this:

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

So, there's a lot of new things going on here. First, set the text-decoration to none, which gets ride of the default underlines under all links in HTML. We then set the left and right margins of each of the links to **auto**. This tells the browser that, whatever the width of the screen, I want even margins on both the left and the right side of the element, which effectively centers it. We also set the font size, weight, and family to be more appealing than the HTML defaults. For the border attribute, we specified three things. The first is 1px which is the thickness of the border, followed by specifying a solid line border, followed by the color of the border. The text-align: center attribute is fairly self-explanatory. I set the color of the border and the text to the hex color: **#f15f5d**, which is a light shade of red, but you can change this to anything you like. Just google hex color finder to find the code for the color you like most!

As the page stands now, it seems like the link text inside the border is too close to the border. Let's let the text breathe a little by using the **padding** attribute in CSS. Padding allows us to add space in between the text and the border. We can add padding to the top, bottom, left, and right of the text like so:

```css
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

This will give us very subtly rounded edges around our border. Let's add one more nice feature to our links and invert the color when a user hovers of the links. In CSS, we can specify style changes to elements when the user of the webpage performs a certain action on a certain element. For example, if we did:

```css
.link:hover {
	font-size: 90px;
}
```

it would tell the browser to increase the font-size of the link every time the user hovers over the link with the mouse. Increasing the font-size is pretty obnoxious though, so let's instead invert the colors of the element like:

```css 
.link:hover {
	background-color: #f15f5d;
	color: white;
}
```

So, now when a user hovers their mouse on any of the link boxes, the background-color will turn the light shade of red, and the text color will turn white. This adds a nice user experience effect. Let's now spruce the homepage up a bit more by adding an image of your choosing. Above the links section in the HTML, let's insert an **img** tag which lets us insert images into the webpage:

```html
<img src="<url of image you want here>" class="homeImage"/>
<a href="bio.html" class="link"> My Biography </a>
<a href="quotes.html" class="link"> My Favorite Movie Quotes </a>
<a href="misc.html" class="link"> Learn s'more about me! </a>
```

Inside the **src** attribute of the **img** tag, insert a link to an image (from google, or flickr, or any other website) that you want to appear on your home page. The image may appear to a little awkwardly positioned and sized on the page, so we'll use CSS to make sure it's the right size and nicely aligned in the center of the page with all the links. We're going to create new CSS class called **homeImage** in style.css and add some margin and width attributes:

```css
.homeImage {
	display: block;
	margin-left: auto;
	margin-right: auto;
	margin-top: 20px;
	margin-bottom: 20px;
	width: 20%;
}
```

Here, we again set the margin left and right attributes to be **auto** so the browser can just center the image for us. We also set its margin bottom and top attributes so the image doesn't stick to the top of the page and there's some space between the image and the first link. I personally like the width of my image to take up 20% of the screen, but you can play around with all the above values of the attributes to see what suits you best!

Now that our homepage is looking moderately fresh, let's move on to the favorite movie quotes page. On this page, we're going to create a nice header followed by a series of text boxes that contain each of your favorite quotes. Start by inserting the following html inside the **body** tag of quotes.html:

```html
<body>
	<div class="quotesPage">
		<h3 class="quoteHeader"> My Favorite Movie Quotes EVER!!!!! </h3>
		<div class="movieQuote">
			"Let's put a smile on that face!" - The Joker from the The Dark Knight
		</div>
		<div class="movieQuote">
			"I like to picture Jesus in a tuxedo T-Shirt because it says I want to be formal, but I'm here to party." - Cal Jr. from Talladega Nights
		</div>
		<div class="movieQuote">
			"There were horses, and a man on fire, and I killed a guy with a trident!" - Brick Tamland from Anchorman
		</div>
		<div class="movieQuote">
			"I would like to extend to you an invitation to the pants party." - Brick Tamland from Anchorman
		</div>
		<div class="movieQuote">
			"Anyone can cook!" - Chef Gusteau from Ratatouille
		</div>
	</div>
</body>
```

I'm using a new tag here called the **div** tag. **Div** tags don't have any special meaning in HTML, they're just used to assign style to a certain portion of text. For example, I wanted to give style to each of the above quotes, so I just put them inside a **div** tag so I could assign a class to them and therefore style the elements. We add the outer **<div class="quotesPage">** to surround both the heading and the quotes so we can put a background image over the entire page. Let's add style for the three new classes created above, **quoteHeader**, **movieQuote**, and **quotesPage**:

```css
.quotesPage {
	background-image: url("https://i.ytimg.com/vi/2LoaD6tTB08/maxresdefault.jpg");
}

.quoteHeader {
	font-family: Pacifico;
	font-weight: 200;
	margin-bottom: 20px;
	text-align: center;
	color: white;
}

.movieQuote {
	border: 1px solid #e8e8e8;
	border-radius: 3px;
	padding: 20px 10px 20px 10px;
	margin-bottom: 20px;
	background-color: #B9B9E2;
	font-family: Helvetica;
	font-weight: 200;
	color: black;
	font-size: 15px;
	width: 40%;
	margin-left: auto;
	margin-right: auto;
	text-align: center;
}
```

Most of the above attributes should look pretty familiar from the homepage style. We again use **auto** margins to center everything and we have a nice shade of light blue in our text boxes. Definitely feel free to change up the values and colors to see what you like best. The new attribute we used is **background-image**, which again is pretty self-explanatory. We just give CSS a URL and it applies the image at that URL to be the background of all the elements that are contained within its corresponding class tag.

So, that's a pretty basic intro into HTML/CSS. I'd definitely suggest using the skills we learned today to complete the bio and miscellaneous portions of the website, or add more pages if you want. But, as you can probably see, using HTML/CSS to build more complex websites than the one we built today would get incredibly annoying and tedious. Lucky for web developers, there's a tool called Bootstrap that simplifies the process a lot while still allowing you to customize the website a good deal.

## Bootstrap

Try going to http://startbootstrap.com/template-categories/all/. Here you'll find several website templates that you can download for free and customize to your heart's content. Try downloading a theme that you like into a directory of your choosing and open up the index.html file in your browser. You'll see an extremely nice and well fleshed out site with generic content. You can go into the index.html file and edit the content to make the site personal to you. Take 10-15 minutes to customize one of the themes to make it your personal website. You can also edit or add your own CSS if you don't like how a particular element on the page is currently styled.

One of the nicest features of Bootstrap is the column feature. Often times, it's really annoying to precisely position HTML elements on a webpage using just CSS. So, Bootstrap came up with a useful, but kind of confusing, system for arranging elements of your HTML into columns on the page. Let's create two new files called columns.html and columns.css and paste the following HTML into columns.html:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<title>Homepage</title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" type="text/css" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css"/>
	<link rel="stylesheet" type="text/css" href="columns.css"/>
</head>
<body>	
	
</body>
</html>
```

Boostrap is basically a library of pre-built CSS classes, just like the ones we built above, that we can assign to any of our HTML elements. There are a lot of useful classes that Bootstrap has to offer, but we'll be covering the ones that have to do with creating columns. The Boostrap system uses 12 columns to describe a webpage. We can make elements in HTML that extend any number of columns wide between 1 and 12 like so:

```html
<body>	
	<div class="col-lg-6 firstCol">
		HI
	</div>
	<div class="col-lg-6 secondCol">
		YO
	</div>
</body>
```

```css
.firstCol {
	background-color: blue;
	height: 200px;
}
.secondCol {
	background-color: red;
	height: 200px;
}
```

What we did here is create two columns, using the Bootstrap **col-lg-6** class, each of length six, so that together they take up the width of the entire page. Since 12 columns is equal to the width of the page, and we created two sections of size 6 columns each, we fill up the entire width of the page. I also added our own classes here and put background-colors on each of the columns to accentuate the difference between the sections of the page. The Bootstrap **col** classes dictate the width of an element in HTML, we are free to modify the height of such elements. Here, I made each column have a height of 200px. Already, we can see how a system like this would be useful for compartmentalizing information on a website. For example, if we were creating a website for a newspaper, which is information heavy, we could very easily split up the different sections of the newspaper into columns. We could have a column for sports, a column for world news, etc. Let's create some more columns:

```html
<body>	
	<div class="col-lg-6 firstCol">
		HI
	</div>
	<div class="col-lg-6 secondCol">
		YO
	</div>
	<div class="col-lg-1 thirdCol">
		sup
	</div>
	<div class="col-lg-1 fourthCol">
		whaddup
	</div>
	<div class="col-lg-4 fifthCol">
		hola
	</div>
	<div class="col-lg-6 sixthCol">
		nein
	</div>
</body>
```

```css
.firstCol {
	background-color: blue;
}
.secondCol {
	background-color: red;
}
.thirdCol {
	background-color: green;
	height: 100px;
}
.fourthCol {
	background-color: yellow;
	height: 100px;
}
.fifthCol {
	background-color: purple;
	height: 100px;
}
.sixthCol {
	background-color: black;
	height: 100px;
}
```

## Hosting

As of now, we can only view the webpage we just created on our own machine. What we want is for the whole world to see it! So, we need some way of hosting the webpage on the Internet, publicly accessible to everyone. Luckily, github makes this really easy for us in just a few simple steps. Visit https://pages.github.com/ and follow the steps and your website should be online almost immediately!



