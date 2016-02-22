-> What do we wanna do here?
-> Create one index.html file
	-> Creating a personal website with the following sections:
		-> Homepage
		-> Hobbies
		-> Favorite Movie/TV Quotes
		-> Bio/Resume
		-> Answers to the following questions:
			-> What is your biggest irrational fear?
-> Create one style.css file
	-> Design like my rishindoshi.github.io
	-> Simple light blue boxes for text with font Helvetica
	-> Pacifico Headers
-> Bootstrap?
-> Host to github?

-> Start off with template that they can use in beginner.html
	-> 

# HTMLWorkshop

## Setup

We're going to begin our journey into HTML with the beginner.html file. Let's take a look at the following snippet from the file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<title>Homepage</title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" type="text/css" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css"/>
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

So, those are some of the most basic tags we can use in HTML. Now that we're getting a sense of how HTML is used to structure content on a webpage, let's dive into some of the more interesting elements of making a webpage, namely CSS. CSS stands for Cascading Style Sheets, and it's used to style a webpage. It allows to do things like set the font size and type of text, use background colors and images, set margins for the page, and many others. Let's take a look at some example CSS:

```css
p {
	font-size: 40px;
	color: blue;
	margin-top: 100px;
	margin-bottom: 100px;
}
```


