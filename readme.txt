************************
       CSS3 Tabs
************************

----------------
Adding new Tabs
----------------
You can add as many tabs as you would like, just add 
another <div> inside the <div class="tabs">. That new 
<div> should have inside it an anchor link with a hash-tag 
that matches the ID of its parent, and another generic 
<div> that contains the content.

<div id="new-tab">
    <a href="#new-tab">New Tab</a>
    <div>
        Content in here.
   </div>
</div>


----------------
Duplicate Markup
----------------
Notice how there are four tab groups but only three show? 
The last tab is hidden by default, and the content of 
that tab group is the same as the first tab. This is so 
when there is no hash-tag in the URL, the FIRST tabs 
content is what is shown, which is what makes the most sense. 
If you don't like how that duplicates content in the markup
(nobody is blaming you, it is weird), you can just let the
last tab be the default content, and remove this from the CSS:

.tabs > div:last-child > a { display: none; } 



----------------
Browser Support
----------------

WORKS
  Firefox 3+
  Safari 3+
  Chrome (any)
  Opera 10+
  
DOESN'T WORK
  Internet Explorer (8 and down, might work in 9)
  
If IE support is extremely important, you'll need to look into
a JavaScript technique. If an IE fallback is OK, consider
just using an IE stylesheet and hiding the actual tabs and
all but the first panel.

<!--[if lt IE 9]>
	<link rel="stylesheet" type="text/css" href="ie-tab-fallback.css" />
<![endif]-->
