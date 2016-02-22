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

# HTMLWorkshop

## Setup

Create a new directory for all the code we're going to write today and then create a file within that directory called index.html. Copy and paste the following HTML chunk into the index.html file to get started:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<title>Homepage</title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" type="text/css" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css"/>
	<link rel="stylesheet" type="text/css" href="css/style.css"/>
</head>
<body>
	WHADDUP
</body>
</html>
```

You can think of HTML as a set of rules that dictates how a webpage will be formatted and presented. These "rules" come in the form of "tags". When your browser is loading an HTML page, it goes through the above chunk of code, and structures the webpage that users see based off these tags. The <html> tag tells the browser