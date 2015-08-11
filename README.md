HTML Snippet Code Library
=========================

* [Basics](#basics)
    * [Line across page](#line-across-page)
    * [Hard carriage return](#hard-carriage-return)
    * [Non-breaking space](#non-breaking-space)
    * [Registered trademark](#registered-trademark)
    * [Page break](#page-break)
    * [Em dash](#em-dash)
    * [Bullet Point](#bullet-point)
    * [Image Captions](#image-captions)
    * [Image Credits](#image-credits)
    * [Pull quote](#pull-quote)
    * [Open a new window with a link (use very sparingly)](#open-a-new-window-with-a-link-use-very-sparingly)
    * [Gray box](#gray-box)
    * [Suppress Slideshow Thumbnails](#suppress-slideshow-thumbnails)
* [Creating bookmarks within a document](#creating-bookmarks-within-a-document)
    * [Sister Site Bugs](#sister-site-bugs)
    * [Atlantic Cities partner-style](#atlantic-cities-partner-style)
* [Related Content](#related-content)
    * [See Also](#see-also)
    * [Study of the Day](#study-of-the-day)
    * [More Emporium](#more-emporium)
    * [Related Video](#related-video)
    * [Multiple "More on" list with thumbnails](#multiple-more-on-list-with-thumbnails)


## Basics

### Line across page

```html
<hr />
```

### Hard carriage return

```html
<br />
```

### Non-breaking space

```html
&nbsp;
```

### Registered trademark

```html
&reg;
```

### Page break

```html
<pagebreak />
```

### Em dash

```html
&mdash;
```

### Bullet Point
```
&#8226;
```

### Image Captions

```html
<!-- FULL Width Image Caption -->
<p>
 <img src="[Photo-URL-Here]" alt="[optional image description]" class="mt-image-none" />
 <span class="caption" style="font-family: arial, sans-serif; font-size: 11px; ">[CAPTION (CREDITS)]</span>
</p>
 
<!-- RIGHT Caption (and optional credits): -->
<span style="float: right; margin: 0 0 20px 20px;">
  <img src="[Photo-URL-Here]" alt="[optional image description]" class="mt-image-none" />
  <span class="caption" style="font-family: arial, sans-serif; text-align:left; display:block ">[CAPTION (CREDITS)]</span>
</span>
 
<!-- LEFT  Caption (and optional credits): -->
<span style="float: left; margin: 0 20px 20px 0;">
  <img src="[Photo-URL-Here]" alt="[optional image description]" class="mt-image-none" />
  <span class="caption" style="font-family: arial, sans-serif; text-align:left; display:block ">[CAPTION (CREDITS)]</span>
</span>
```

 
### Image Credits

```html
<!-- Full Width Image Credit -->
<p>
  <img src="[Photo-URL-Here]" alt="[optional image description]" class="mt-image-none" />
  <span class="credit" style="font-family: arial, sans-serif; color: #242b30; font-size: 9px; text-align:right">[CREDITS]</span>
</p>

<!-- RIGHT Credits: -->
<span style="float: right; margin: 0 0 20px 20px;">
  <img src="[Photo-URL-Here]" alt="[optional image description]" class="mt-image-none" />
  <span class="credit" style="font-family: arial, sans-serif; text-align:right; display:block ">[CREDITS]</span>
</span>
 
<!-- LEFT Credits: -->
<span style="float: left; margin: 0 20px 20px 0;">
  <img src="[Photo-URL-Here]" alt="[optional image description]" class="mt-image-none" />
  <span class="credit" style="font-family: arial, sans-serif; text-align:right; display:block ">[CREDITS]</span>
</span>
```

### Pull quote

```html
    <!-- PULL QUOTE v. 2 -->
    <aside class="pullquote">
        [QUOTE GOES HERE]
    </aside>
    <!-- END PULL QUOTE v. 2 -->
```

### Open a new window with a link (use very sparingly)
   
```html 
<a href="something" target="_blank">link text</a>
```

### Gray box

```html
<div class="graybox">[CONTENT GOES HERE.]</div>
```

### Suppress Slideshow Thumbnails

```html
<style type=”text/css”>
    #altGallery .galleryNav { display:none !important } 
    #altGallery .fullScreen { display: none !important }
    #altGallery .galleryTitle { display:none !important } 
</style>
```

## Creating bookmarks within a document

Put this where you want the bookmark to be:

```html
<!-- BOOKMARK -->
<a name="[bookmark_name]"></a>
```

Be sure to replace [bookmark_name] with whatever you want to call your bookmark. The name must be unique, consist only of alphanumeric characters (letters and numbers) and underscores.

Then to create a link to that bookmark, use this:

```html
<!-- LINK TO BOOKMARK -->
<a href="#[bookmark_name]">[link text, e.g., "go to section 1"]</a>
```

Be sure to replace [bookmark_name] with the bookmark’s name, and replace [link text] with whatever you like.

Here’s an example:

```html
<!-- BOOKMARK -->
<a name="section_1"></a>
Section 1: De Dicto vel De Re

Lorem ipsum dolor amet sit . . .

Then somewhere else in the same document, I could link to that bookmark like this:

<a href="#section_1">Go to section 1</a>
```

The words “Go to section 1” will be a link, and when the user clicks it, the browser will jump back to the bookmark.

### Sister Site Bugs

#### Atlantic Wire Bug
![](http://cdn.theatlantic.com/static/front/images/wire/articlePromo.png)

```html
<!-- START "ATLANTIC WIRE" BUG FOR POSTS -->
<a href="http://www.theatlanticwire.com/"
   name="&amp;lid=The-Atlantic-Wire&amp;lpos=Article-Bug">
    <img src="http://cdn.theatlantic.com/static/front/images/wire/articlePromo.png"
         style="border: 0;">
</a>
<!-- END "ATLANTIC WIRE" BUG FOR POSTS -->
```

#### Atlantic Cities Bug
![](http://cdn.theatlantic.com/static/front/images/cities/Cities_Atl_bug.png)

```html
<!-- START "ATLANTIC CITIES" BUG FOR POSTS -->
<a href="http://www.theatlanticcities.com/"
   name="&lid=The-Atlantic-Cities&lpos=Article-Bug">
    <img src="http://cdn.theatlantic.com/static/front/images/cities/Cities_Atl_bug.png"
         style="border: 0;">
</a>
<!-- END "ATLANTIC CITIES" BUG FOR POSTS -->
```

### Atlantic Cities partner-style

```html
<!-- START "CITIES PARTNER" BOX v. 1 -->
<div style="margin: 10px;
        padding: 10px;
        width: 215px;
        float: right;
        text-align: left;">
    <hr/>
    <div style="font-family: Arial, sans-serif;
        font-size: 7.5pt;
        font-weight: bold;
        margin-left: 20px;">
        <a href="http://www.nationaljournal.com/">
            <img alt="Cities Logo"
                 src="http://cdn.theatlanticcities.com/img/site/Cities_155x82.png"
                 style="margin-top: 5px;
            height: 82px;
            width: 155px;"/>
        </a>
        <br />
        [DEK GOES HERE]
    </div>
    <ul style="text-align: left;
        line-height: 12pt;
        margin-left: -20px;">
        <li style="margin-bottom: 7px;">
            <a href="[ARTICLE'S URL GOES HERE]">
                [ARTICLE'S HEADLINE GOES HERE]
            </a>
        </li>
        <li style="margin-bottom: 7px;">
            <a href="[ARTICLE'S URL GOES HERE]">
                [ARTICLE'S HEADLINE GOES HERE]
            </a>
        </li>
        <li style="margin-bottom: 7px;">
            <a href="[ARTICLE'S URL GOES HERE]">
                [ARTICLE'S HEADLINE GOES HERE]
            </a>
        </li>     
    </ul>
    <hr/>
</div>
<!-- END "CITIES PARTNER" BOX v. 1 -->
```

## Related Content

### See Also

![](https://raw.github.com/theatlantic/html-snippets/master/img/see_also.png)

```html
<!-- START "SEE ALSO" v. 1 -->
<aside class="callout">
    <hr/>
    <h4>See also</h4>
    <h5>(Optional subtitle)</h5>
    <p><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></p>
    <hr/>
</aside>
<!-- END "SEE ALSO" v. 1 -->
```

### "More on" Box

![](https://raw.github.com/theatlantic/html-snippets/master/img/related_story.png)

```html
<!-- START "MORE ON" SINGLE STORY BOX v. 2 -->
<aside class="callout">
    <h4>Related Story</h4>
    <div>
        <a href="[URL]">
            <img width="242" src="[THUMBNAIL URL]" />
        </a>
    </div>
    <p>
        <a href="[URL]">
            [ARTICLE TITLE]
        </a>
    </p>
</aside>
<!-- END "MORE ON" SINGLE STORY BOX v. 2 -->
```

### "More on" list box, with image

```html
<!-- START "MORE ON" LIST BOX v. 3 -->
<aside class="callout">
    <hr/>
    <h4>More From Quartz</h4>
    <div>
        <a href="[URL]">
            <img width="242" src="[THUMBNAIL URL]" />
        </a>
    </div>

    <ul>
        <li><a href="[URL]">[HEADLINE 1]</a></li>
        <li><a href="[URL]">[HEADLINE 2]</a></li>
        <li><a href="[URL]">[HEADLINE 3]</a></li>
    </ul>

    <hr/>
</aside>
<!-- END "MORE ON" LIST BOX v. 3 -->
```

### "More on" list box, no image

![](https://raw.github.com/theatlantic/html-snippets/master/img/more_on_list.png)

```html
<!-- START "MORE ON" LIST BOX NO IMAGE v. 3 -->
<aside class="callout">
    <hr/>
    <h4>More From Quartz</h4>
    <ul>
        <li><a href="[URL]">[TITLE 1]</a></li>
        <li><a href="[URL]">[TITLE 2]</a></li>
        <li><a href="[URL]">[TITLE 3]</a></li>
    </ul>
    <hr/>
</aside>
<!-- END "MORE ON" LIST BOX v. 3 -->
```

### Study of the Day

![](https://raw.github.com/theatlantic/html-snippets/master/img/study.png)

```html
<!-- START "MORE STUDY OF THE DAY" BOX v. 1 -->
<aside class="callout">
   <hr/>
    <a href="http://www.theatlantic.com/health/category/studies">
        <img width="242" alt="NJ logo.JPG" 
                src="http://cdn.theatlantic.com/static/front/images/bugs/studyoftheday.png"/>
    </a>
    <ul>
        <li>
            <a href="[ARTICLE URL]">
                [ARTICLE TITLE]
            </a>
        </li>
        <li>
            <a href="[ARTICLE URL]">
                [ARTICLE TITLE]
            </a>
        </li>
        <li>
            <a href="[ARTICLE URL]">
                [ARTICLE TITLE]
            </a>
        </li>
   </ul>
   <hr/>
</aside>
<!-- END "MORE STUDY OF THE DAY" BOX v. 1 -->
```

### More Emporium

![](https://raw.github.com/theatlantic/html-snippets/master/img/emporium.png)

```html
<!-- START "MORE STUDY OF THE DAY" BOX v. 1 -->
<aside class="callout">
   <hr/>
    <a href="http://www.theatlantic.com/health/category/emporium/">
        <img width="242" alt="NJ logo.JPG" 
                src="http://cdn.theatlantic.com/static/mt/assets/food/DHEMW_bug_2.png">
    </a>
    <ul>
        <li>
            <a href="[ARTICLE'S URL GOES HERE]">
                [ARTICLE'S HEADLINE GOES HERE]
            </a>
        </li>
        <li>
            <a href="[ARTICLE'S URL GOES HERE]">
                [ARTICLE'S HEADLINE GOES HERE]
            </a>
        </li>
        <li>
            <a href="[ARTICLE'S URL GOES HERE]">
                [ARTICLE'S HEADLINE GOES HERE]
            </a>
        </li>
   </ul>
   <hr/>
</aside>
<!-- END "MORE STUDY OF THE DAY" BOX v. 1 -->
```

### Related Video

![](https://raw.github.com/theatlantic/html-snippets/master/img/emporium.png)

```html
<!-- START "RELATED VIDEO" SINGLE STORY BOX v. 1 -->
<aside class="callout">
    <hr/>
    <h4>Related Video</h4>
    <a class="related-video-link" href="[ARTICLE URL]">
        <img width="242" src="[THUMBNAIL URL]" />
   </a>
    <p>
        <a href="[ARTICLE URL]">
            [ARTICLE TITLE]
        </a>
    </p>
    <hr/>
</aside>
<!-- END "RELATED VIDEO" SINGLE STORY BOX v. 1 -->
```

### Multiple "More on" list with thumbnails

```html
<!-- START MULTI-THUMB "MORE ON" WITH IMAGES v. 3 -->
<aside class="callout">
  <hr/>
  <h4>More on [SUBJECT]</h4>
  <ul class="with-thumbs">
    <li>
      <a href="[ARTICLE URL]">
        <img width="90" src="[THUMBNAIL URL]"/>
        [ARTICLE TITLE]
      </a>
    </li>

    <li>
      <a href="[ARTICLE URL]">
        <img width="90" src="[THUMBNAIL URL]"/>
        [ARTICLE TITLE]
      </a>
    </li>

    <li>
      <a href="[ARTICLE URL]">
        <img width="90" src="[THUMBNAIL URL]"/>
        [ARTICLE TITLE]
      </a>
    </li>

  </ul>
  <hr/>
</aside>
<!-- END MULTI-THUMB "MORE ON" WITH IMAGES v. 3 -->
```
