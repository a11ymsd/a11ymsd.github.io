---
layout: page
title: "Checking Websites: Page Title"
permalink: /checking-websites/page-title/
hidenav: true
bookmarklets:
  showtitle: |
    let title = document.querySelector('title');
    alert(title.innerText);
---

## Why are good page titles important? They…

* inform users of their position in a website.
* help to identify that a user has reached the correct page.
* are the first information screen readers announce to their users when a page loads.

## How to check

1. Use the _“Show Title”_ [bookmarklet](#bookmarklet) to view the page title of a page.
2. Navigate to other pages of the same website and use the same bookmarklet.

## What is a good page title?

1. The title is adequate and describes the content of the page.
2. The title is short.
3. The title is unique in a set of web pages on a website.
4. _Best Practice:_ All pages have a front-loaded title.

### Examples

* Suboptimal titles:
  * Welcome to home page of Acme Web Solutions, Inc.
  * Acme Web Solutions, Inc. \| About Us
  * Acme Web Solutions, Inc. \| Contact Us
  * Acme Web Solutions, Inc. \| History

* Good titles:
  * Acme Web Solutions home page
  * About Acme Web Solutions
  * Contact Acme Web Solutions
  * History of Acme Web Solutions

## Bookmarklet

{% include bmarklet.html label="Show Title" code=page.bookmarklets.showtitle installinfo=true %}



## Other Checks

1. [Page Title](/checking-websites/page-title/)

2. [Images](/checking-websites/images/)

3. [Headings](/checking-websites/headings/)

4. [Contrast](/checking-websites/contrast)

5. [Resize Text](/checking-websites/resize-text/)

6. [Keyboard Access and Visual Focus](/checking-websites/keyboard/)

7. [Forms, labels, and errors](/checking-websites/forms/)

8. [Animated Content](/checking-websites/animations/)

9. [Multimedia (video, audio) alternatives](/checking-websites/multimedia/)

10. [Basic Structure Check](/checking-websites/structure/)