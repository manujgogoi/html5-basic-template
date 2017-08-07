# html5-basic-template
This is a very basic html5 page layout for any Web project.

## The Doctype

First, we have the Document Type Declaration, or doctype. This is simply a way to tell the browser—or any other parser—what type of document it’s looking at. In the case of HTML files, it means the specific version and flavor of HTML. The doctype should always be the first item at the top of any HTML file. Many years ago, the doctype declaration was an ugly and hard-to-remember mess. For XHTML 1.0 Strict:

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
   "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
```

And for HTML4 Transitional:

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
   "http://www.w3.org/TR/html4/loose.dtd">
```
Although that long string of text at the top of our documents hasn’t really hurt us (other than forcing our sites’ viewers to download a few extra bytes), HTML5 has done away with that indecipherable eyesore. Now all you need is this:

```html
<!doctype html>
```

## The `<html>` Element

Next up in any HTML document is the `html` element, which has not changed significantly with HTML5. In our example, we’ve included the `lang` attribute with a value of `en`, which specifies that the document is in English. In XHTML-based syntax, you’d be required to include an xmlns attribute. In HTML5, this is no longer needed, and even the `lang` attribute is unnecessary for the document to validate or function correctly.

So here’s what we have so far, including the closing `</html>` tag:

```html
<!doctype html>
<html lang="en">

</html>
```

## The `<head>` Element

The HTML `<head>` element provides general information (metadata) about the document, including its title and links to its scripts and style sheets.

The first line inside the `head` is the one that defines the character encoding for the document. This is another element that’s been simplified since XHTML and HTML4, and is an optional feature, but recommended. In the past, you may have written it like this:

```html
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
```

HTML5 improves on this by reducing the character encoding `<meta>` tag to the bare minimum:

```html
<meta charset="utf-8">
```

In nearly all cases, `utf-8` is the value you’ll be using in your documents. If you want to delve a little deeper into character encoding, you can read up on the topic on [W3C](https://www.w3.org/) or [WHATWG](https://whatwg.org/).

```html
<title>The HTML5 Layout</title>
```

The HTML `<title>` element defines the title of the document, shown in a browser's title bar or on the page's tab. It can only contain text, and any contained tags are ignored.

```html
<meta name="description" content="The HTML5 Layout">
```

Meta descriptions are HTML attributes that provide concise summaries of webpages. They commonly appear underneath the blue clickable links in a search engine results page (SERP).
Meta descriptions can be any length, but search engines generally truncate snippets longer than 160 characters. It is best to keep meta descriptions long enough that they're sufficiently descriptive, but shorter than that 160-character limit.

```html
<meta name="author" content="MG">
```
Author defines the name of the document's author.

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```
This meta tag is used to make a webpage mobile responsive. It means that the browser will (probably) render the width of the page at the width of its own screen.
**Note:** don't use a responsive meta tag if your website isn't specifically designed to be responsive and work well at that size, as it will make the experience worse.
Learn more about viewports in different mobile browsers in [A Tale of Two Viewports](https://www.quirksmode.org/mobile/viewports2.html) at quirksmode.org.

```html
<link rel="stylesheet" href="css/styles.css?v=1.0">
```
The HTML `<link>` element specifies relationships between the current document and an external resource. Possible uses for this element include defining a relational framework for navigation. This element is most used to link to *style sheets*.
`rel` attribute names a relationship of the linked document to the current document. The attribute must be a space-separated list of the link types values. The most common use of this attribute is to specify a link to an external style sheet: the `rel` attribute is set to stylesheet, and the `href` attribute is set to the URL of an external style sheet to format the page.

```html
<!--[if lt IE 9]>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/html5shiv/3.7.3/html5shiv.js"></script>
<![endif]-->
```
HTML5 Shiv is a JavaScript workaround, created by Sjoerd Visscher, to enable styling of HTML5 elements in versions of Internet Explorer prior to version 9, which do not allow unknown elements to be styled without JavaScript.

## The `<body>` Element
The HTML <body> Element represents the content of an HTML document. There can be only one `<body>` element in a document.

## The `<script>` Element
The HTML <script> element is used to embed or reference an executable script (e.g. Javascript).
