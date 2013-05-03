---
layout: main
---

# HTML Snippet Code Library

## Contents

* TOC
{:toc}

## Typography

<table>
    <tr>
        <th width="25%">Character</th>
        <th>HTML</th>
    </tr>
    <tr>
        <td>Line break</td>
        <td>

{% highlight html %}
<br/>
{% endhighlight %}

        </td>
    </tr>
    <tr>
        <td>Non-breaking space</td>
        <td>

{% highlight html %}
&nbsp;
{% endhighlight %}

        </td>
    </tr>
    <tr>
        <td>Em dash</td>
        <td>

{% highlight html %}
&mdash;
{% endhighlight %}
        </td>
    </tr>
    <tr>
        <td>En dash</td>
        <td>

{% highlight html %}
&ndash;
{% endhighlight %}

        </td>
    </tr>
    <tr>
        <td>Bullet</td>
        <td>

{% highlight html %}
&bull;
{% endhighlight %}

        </td>
    </tr>
</table>

## Basics

### Horizontal rule

{% highlight html %}
<hr />
{% endhighlight %}

### Page break

{% highlight html %}
<pagebreak />
{% endhighlight %}

### Pull quote

{% highlight html %}
<aside class="pullquote">
    [QUOTE]
</aside>
{% endhighlight %}

### Captions / Credits

#### Caption

{% highlight html %}
<figure>
    <img src="[IMAGE URL]" alt="[IMAGE DESCRIPTION]" />
    <figcaption>CAPTION</figcaption>
</figure>
{% endhighlight %}

#### Credit

Credits display slightly smaller than captions and are right-aligned

{% highlight html %}
<figure>
    <img src="[IMAGE URL]" alt="[IMAGE DESCRIPTION]" />
    <figcaption class="credit">CREDITS</figcaption>
</figure>
{% endhighlight %}

#### Caption and credit

To display both a caption and a credit, use the style for captions and add the credits in parentheses after the caption text.

{% highlight html %}
<figure>
    <img src="[IMAGE URL]" alt="[IMAGE DESCRIPTION]" />
    <figcaption>CAPTION (CREDIT)</figcaption>
</figure>
{% endhighlight %}

#### Caption or credit for a video

To use the caption and credit styles on videos and other embeds, use the appropriate style above and replace the `<img/>` tag with your embed code.

### Open a new window with a link (use very sparingly)

{% highlight html %}
<a href="[FULL URL]" target="_blank">link text</a>
{% endhighlight %}

## Suppress Slideshow Thumbnails

{% highlight html %}
<!-- START SUPPRESS SLIDESHOW THUMBNAILS -->
<style type="text/css">
    #altGallery .galleryNav { display: none !important; }
    #altGallery .fullScreen { display: none !important; }
    #altGallery .galleryTitle { display: none !important; }
</style>
<!-- END SUPPRESS SLIDESHOW THUMBNAILS -->
{% endhighlight %}

## Creating bookmarks within a document

Put this where you want the bookmark to be:

{% highlight html %}
<a name="[bookmark_name]"></a>
{% endhighlight %}

Be sure to replace [bookmark_name] with whatever you want to call your bookmark. The name must be unique, consist only of alphanumeric characters (letters and numbers) and underscores.

Then to create a link to that bookmark, use this:

{% highlight html %}
<a href="#[bookmark_name]">[link text, e.g., "go to section 1"]</a>
{% endhighlight %}

Be sure to replace [bookmark_name] with the bookmark’s name, and replace [link text] with whatever you like.

Here’s an example:

{% highlight html %}
<!-- BOOKMARK -->
<a name="section_1"></a>
Section 1: De Dicto vel De Re

Lorem ipsum dolor amet sit . . .

Then somewhere else in the same document, I could link to that bookmark like this:

<a href="#section_1">Go to section 1</a>
{% endhighlight %}

The words "Go to section 1" will be a link, and when the user clicks it, the browser will jump back to the bookmark.

## Promotional Bugs

### Atlantic Wire Bug

![](http://cdn.theatlantic.com/static/front/images/wire/articlePromo.png)

{% highlight html %}
<!-- START "ATLANTIC WIRE" BUG FOR POSTS -->
<a href="http://www.theatlanticwire.com/"
   name="&amp;lid=The-Atlantic-Wire&amp;lpos=Article-Bug">
    <img src="http://cdn.theatlantic.com/static/front/images/wire/articlePromo.png"
         style="border: 0;">
</a>
<!-- END "ATLANTIC WIRE" BUG FOR POSTS -->
{% endhighlight %}

### Atlantic Cities Bug

![](http://cdn.theatlantic.com/static/front/images/cities/Cities_Atl_bug.png)

{% highlight html %}
<!-- START "ATLANTIC CITIES" BUG FOR POSTS -->
<a href="http://www.theatlanticcities.com/"
   name="&amp;lid=The-Atlantic-Cities&amp;lpos=Article-Bug">
    <img src="http://cdn.theatlantic.com/static/front/images/cities/Cities_Atl_bug.png"
         style="border: 0;">
</a>
<!-- END "ATLANTIC CITIES" BUG FOR POSTS -->
{% endhighlight %}

## Related Content

### See Also

{% highlight html %}
<!-- START "SEE ALSO" v. 1 -->
<aside class="callout">
    <hr/>
    <h4>See also</h4>
    <h5>(Optional subtitle)</h5>
    <p><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></p>
    <hr/>
</aside>
<!-- END "SEE ALSO" v. 1 -->
{% endhighlight %}

![](https://raw.github.com/theatlantic/html-snippets/master/img/see_also.png)

<br>

### "More on" Box

{% highlight html %}
<!-- START "MORE ON" SINGLE STORY BOX v. 2 -->
<aside class="callout">
    <hr/>
    <h4>Related Story</h4>
    <div>
        <a href="[URL]">
            <img width="242" src="[THUMBNAIL URL]" />
        </a>
    </div>
    <p>
        <a href="[URL]">[ARTICLE TITLE]</a>
    </p>
    <hr/>
</aside>
<!-- END "MORE ON" SINGLE STORY BOX v. 2 -->
{% endhighlight %}

![](https://raw.github.com/theatlantic/html-snippets/master/img/related_story.png)

<br>

### "More on" list box, with image

{% highlight html %}
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
        <li><a href="[URL]">[TITLE]</a></li>
        <li><a href="[URL]">[TITLE]</a></li>
        <li><a href="[URL]">[TITLE]</a></li>
    </ul>
    <hr/>
</aside>
<!-- END "MORE ON" LIST BOX v. 3 -->
{% endhighlight %}

### "More on" list box, no image

{% highlight html %}
<!-- START "MORE ON" LIST BOX NO IMAGE v. 3 -->
<aside class="callout">
    <hr/>
    <h4>More From Quartz</h4>
    <ul>
        <li><a href="[URL]">[TITLE]</a></li>
        <li><a href="[URL]">[TITLE]</a></li>
        <li><a href="[URL]">[TITLE]</a></li>
    </ul>
    <hr/>
</aside>
<!-- END "MORE ON" LIST BOX v. 3 -->
{% endhighlight %}

![](https://raw.github.com/theatlantic/html-snippets/master/img/more_on_list.png)

<br>

### Study of the Day

{% highlight html %}
<!-- START "MORE STUDY OF THE DAY" BOX v. 1 -->
<aside class="callout">
  <hr/>
  <a href="http://www.theatlantic.com/health/category/studies">
    <img width="242" alt="More Studies of the Day"
         src="http://cdn.theatlantic.com/front/images/bugs/studyoftheday.png"/>
  </a>
  <ul>
    <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
    <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
    <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
  </ul>
  <hr/>
</aside>
<!-- END "MORE STUDY OF THE DAY" BOX v. 1 -->
{% endhighlight %}

![](https://raw.github.com/theatlantic/html-snippets/master/img/study.png)

<br>

### More Emporium

{% highlight html %}
<!-- START "MORE STUDY OF THE DAY" BOX v. 1 -->
<aside class="callout">
  <hr/>
  <a href="http://www.theatlantic.com/health/category/emporium/">
    <img width="242" alt="Dr. Hamblin's Emporium of Medicinal Wonderments"
        src="http://cdn.theatlantic.com/mt/assets/food/DHEMW_bug_2.png"/>
  </a>
  <ul>
    <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
    <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
    <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
  </ul>
  <hr/>
</aside>
<!-- END "MORE STUDY OF THE DAY" BOX v. 1 -->
{% endhighlight %}

![](https://raw.github.com/theatlantic/html-snippets/master/img/emporium.png)

<br>

### Related Video

{% highlight html %}
<!-- START "RELATED VIDEO" SINGLE STORY BOX v. 1 -->
<aside class="callout">
    <hr/>
    <h4>Related Video</h4>
    <a class="related-video-link" href="[ARTICLE URL]">
        <img width="242" src="[THUMBNAIL URL]" />
   </a>
    <p>
        <a href="[ARTICLE URL]">[ARTICLE TITLE]</a>
    </p>
    <hr/>
</aside>
<!-- END "RELATED VIDEO" SINGLE STORY BOX v. 1 -->
{% endhighlight %}

![](https://raw.github.com/theatlantic/html-snippets/master/img/video.png)

<br>

### Multiple "More on" list with thumbnails

{% highlight html %}
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
{% endhighlight %}

### Atlantic Cities partner box

{% highlight html %}
<!-- START "CITIES PARTNER" BOX v. 2 -->
<aside class="callout">
    <hr/>
    <a href="http://www.theatlanticcities.com/">
        <img width="155" alt="The Atlantic Cities"
             src="http://cdn.theatlanticcities.com/img/site/Cities_155x82.png"/>
    </a>
    <ul>
        <li>
            <a href="[ARTICLE URL]">[ARTICLE TITLE]</a>
        </li>
        <li>
            <a href="[ARTICLE URL]">[ARTICLE TITLE]</a>
        </li>
        <li>
            <a href="[ARTICLE URL]">[ARTICLE TITLE]</a>
        </li>
    </ul>
    <hr/>
</aside>
<!-- END "CITIES PARTNER" BOX v. 2 -->
{% endhighlight %}
