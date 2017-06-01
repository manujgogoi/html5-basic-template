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

The next part of our page is the `<head>` section. The first line inside the `head` is the one that defines the character encoding for the document. This is another element that’s been simplified since XHTML and HTML4, and is an optional feature, but recommended. In the past, you may have written it like this:

```html
<meta http-equiv="Content-Type" content="text/html; charset=utf-8">
```

HTML5 improves on this by reducing the character encoding `<meta>` tag to the bare minimum:

```html
<meta charset="utf-8">
```

In nearly all cases, `utf-8` is the value you’ll be using in your documents. A full explanation of character encoding is beyond the scope of this chapter, and it probably won’t be that interesting to you, either. Nonetheless, if you want to delve a little deeper, you can read up on the topic on [W3C](https://www.w3.org/) or [WHATWG](https://whatwg.org/).

Not completed -----------
