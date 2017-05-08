# A modified jsoup to preserve the linebreaks when extracting text from an element

## English Introduction
When parsing HTML that uses `<br>` and `<p>` to indicate new lines, the original version of jsoup ruins the paragraphical structure of a website because all the whitespaces including linebreaks are ommited.

However, this version is highly convenient in parsing webpages for Android applications. The implementation of `Element.text()` and `StringUtil.appendNormalisedWhitespace()` is changed.

## 中文简介
当解析使用`<id>`和`<p>`来换行的HTML时，原版**jsoup**的**Element**对象在调用`text()`方法来返回一个字符串时，所有换行符都会丢失，因而破坏了网页中文本原有的段落结构。

因此，在这个分支中我重写了如上所示的两个类的方法，非常适合用于在安卓应用中解析网页的文本。



## Original Readme
jsoup: Java HTML parser that makes sense of real-world HTML soup.

jsoup is a Java library for working with real-world HTML. It provides a very convenient API for extracting and manipulating data, using the best of DOM, CSS, and jquery-like methods.

jsoup implements the WHATWG HTML5 specification (http://whatwg.org/html), and parses HTML to the same DOM as modern browsers do.

* parse HTML from a URL, file, or string
* find and extract data, using DOM traversal or CSS selectors
* manipulate the HTML elements, attributes, and text
* clean user-submitted content against a safe white-list, to prevent XSS
* output tidy HTML

jsoup is designed to deal with all varieties of HTML found in the wild; from pristine and validating, to invalid tag-soup; jsoup will create a sensible parse tree.

jsoup runs on Java 1.5 and up.

See https://jsoup.org/ for downloads and documentation.


