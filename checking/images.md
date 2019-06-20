---
layout: page
title: "Checking Websites: Images"
permalink: /checking-websites/images/
hidenav: true
bookmarklets:
  checkimages: |
    var label = document.createElement('span');
    label.style.outline = '3px dashed red';
    label.style.position = 'absolute';
    label.style.padding = '3px';
    label.style.backgroundColor = 'yellow';

    var images = document.querySelectorAll('img:not([alt])');
    label.innerHTML = '🚨 NO ALT';
    Array.prototype.forEach.call(images, function(el, i){
      el.style.outline = '3px dashed red';
      var lb = label.cloneNode(true);
          lb.style.top = el.offsetTop + 'px';
          lb.style.left = el.offsetLeft + 'px';
      el.parentNode.insertBefore(lb, el);
    });

    images = document.querySelectorAll('img[alt]');
    label.innerHTML = '🚨 EMPTY ALT';
    label2 = label.cloneNode(true);
    label2.style.outline = '3px solid green';
    Array.prototype.forEach.call(images, function(el, i){
      if (el.getAttribute('alt') != '') {
          el.style.outline = '3px solid green';
          label2.innerHTML= '🖼 ' + el.getAttribute('alt');
          var lb = label2.cloneNode(true);
          lb.style.top = el.offsetTop + 'px';
          lb.style.left = el.offsetLeft + 'px';
          console.log(lb);
          el.parentNode.insertBefore(lb, el);
        } else {
          el.style.outline = '3px solid red';
          var lb = label.cloneNode(true);
          lb.style.top = el.offsetTop + 'px';
          lb.style.left = el.offsetLeft + 'px';
          el.parentNode.insertBefore(lb, el);
        }
    });
---

## Why are accessible images important? They…

* provide information about an image or a button to the user.
* can hide presentational images.
* often contain essential information for users.

## How to check

1. Use the _“Check Images”_ [bookmarklet](#bookmarklet) to highlight images on the page.
2. The images will have a little icon and text depending on the level of accessibility:
3. 

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


{% include bmarklet.html label="Check Images" code=page.bookmarklets.checkimages installinfo=true %}

### Test here

<div style="display: flex">
  <img style="margin: 0 10px;" src="https://images.unsplash.com/photo-1503803548695-c2a7b4a5b875?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=300&q=80">
  <img style="margin: 0 10px;" src="https://images.unsplash.com/photo-1503803548695-c2a7b4a5b875?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=300&q=80" alt="">
  <img style="margin: 0 10px;" src="https://images.unsplash.com/photo-1503803548695-c2a7b4a5b875?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=300&q=80" alt="Sunset">
</div>

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