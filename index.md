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

You can also float images so they don't take up the full-width by setting the size and direction
in a class.

{% highlight html %}
<figure class="right one-third">
    <img src="[IMAGE URL]" alt="[IMAGE DESCRIPTION]" />
    <figcaption>CAPTION</figcaption>
</figure>
{% endhighlight %}

This will put the image on the right and make it up to one-third of the content well's width.

The direction can be `right` or `left`. The size class (which sets the width) can be `one-third` (190px on TheAtlantic.com), 
`two-thirds` (380px), `golden-ratio-big` (352px) and `golden-ratio-small` (218px).

You'll want to resize the image width to match these sizes manually.


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


### Amazon Links

If you're linking to a book on Amazon, we'd like to let Amazon know it is coming from us. You can set up the link to the book by putting the ISBN number in this URL and using this as the link: 

    http://www.amazon.com/exec/obidos/ISBN=[10 digit ISBN number]/theatla05-20/

Example:

    http://www.amazon.com/exec/obidos/ISBN=0701206713/theatla05-20/

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
<!-- START "MORE ON" LIST BOX v. 3 -->
<aside class="callout">
    <hr />
    <h4>More on Coffee</h4>

<div>
<figure href="[URL]"><img alt="" src="" width="242" /></figure>
</div>

<ul>
    <li><a href="[URL]">Consume More Beans</a></li>
    <li><a href="[URL]">Coffee for Children and Tots</a></li>
    <li><a href="[URL]">Trading Beans for Freedom</a></li>
</ul>

<hr /></aside>
<!-- END "MORE ON" LIST BOX v. 3 -->
<!-- END "MORE ON" LIST BOX v. 3 -->
{% endhighlight %}
![](https://raw.github.com/theatlantic/html-snippets/master/img//more_on.png)


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

![](https://raw.github.com/theatlantic/html-snippets/master/img/updated_video.png)

<br>

### Multiple "More on" list with thumbnails

{% highlight html %}
<!-- START MULTI-THUMB "MORE ON" WITH IMAGES v. 3 -->
<aside class="callout">
<hr />
<h4>More on Coffee</h4>

<div>
<figure href="[URL]"><img alt="" src="" width="242" /></figure>
</div>

<ul>
    <li><a href="[URL]">[TITLE]</a></li>
    <li><a href="[URL]">[TITLE]</a></li>
    <li><a href="[URL]">[TITLE]</a></li>
</ul>

<hr /></aside>
<!-- END MULTI-THUMB "MORE ON" WITH IMAGES v. 3 -->
{% endhighlight %}

### Notes 
{% highlight html %}
<!-- Read "Follow-up Notes" -->
<aside class="callout callout-notes">
<hr />
<h4>Read Follow-Up <a href="http://www.theatlantic.com/notes/">Notes</a></h4>
<ul>
    <li><a href="[NOTE URL]">[NOTE TITLE]</a></li>
    <li><a href="[NOTE URL]">[NOTE TITLE]</a></li>
</ul>

<hr /></aside>
</aside>
<!-- END "Follow-up Notes" -->
{% endhighlight %}
![](https://raw.github.com/theatlantic/html-snippets/master/img/notes_screenshot.png)


## More From Partners

These are thin bars that go on the right size of NJ/Quartz stories.

### More from Quartz
{% highlight html %}
<!-- START "MORE FROM" QZ -->
<aside class="partner-box">
    <hr/>
    <h4 class="qz">More From <a href="http://qz.com">Quartz</a></h4>
        <ul>
            <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
            <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
            <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
        </ul>
    <hr/>
    </aside>
<!-- END "MORE FROM" QZ -->
{% endhighlight %}
![](images/more-from-qz.png)

### More from GovExec
{% highlight html %}
<!-- START "MORE FROM" GOVEXEC -->
<aside class="partner-box">
    <hr/>
    <h4 class="govexec">More From <a href="http://govexec.com">GovExec</a></h4>
        <ul>
            <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
            <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
            <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
        </ul>
    <hr/>
</aside>
<!-- END "MORE FROM" GOVEXEC -->
{% endhighlight %}


### More From National Journal
{% highlight html %}
<!-- START "MORE FROM" NATIONAL JOURNAL -->
<aside class="partner-box">
    <hr/>
    <h4 class="nj">More From <a href="http://nationaljournal.com">National Journal</a></h4>
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
<!-- END "MORE FROM" NATIONAL JOURNAL -->
{% endhighlight %}

### More from Defense One

{% highlight html %}
<!-- START "MORE FROM" DEFENSE ONE -->
<aside class="partner-box">
    <hr/>
    <h4 class="defense-one">More From <a href="http://defenseone.com">Defense One</a></h4>
    <ul>
        <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
        <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
        <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
    </ul>
    <hr/>
    </aside>
<!-- END "MORE FROM" QZ -->
{% endhighlight %}

### More from Anyone Else (Custom)

Copy the code below, edit the link and couple click the
empty image to upload the logo into cropduster.

{% highlight html %}
<!-- START "MORE FROM" Custom -->
<aside class="partner-box custom">
<hr />
<h4>More From</h4>

<figure><a href="http://[example_site.com]">
    <img alt="[Site's Name]" src="" width="150" />
</a></figure>

<ul>
    <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
    <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
    <li><a href="[ARTICLE URL]">[ARTICLE TITLE]</a></li>
</ul>

<hr /></aside>
<!-- END "MORE FROM" Custom -->
{% endhighlight %}


## Video

### From the CMS

You can find this code with the embed button on video channel pages.

{% highlight html %}
<iframe width="640" height="360" frameborder="0" webkitallowfullscreen="webkitallowfullscreen" 
    allowfullscreen="allowfullscreen" mozallowfullscreen="mozallowfullscreen" 
    src="http://www.theatlantic.com/video/iframe/[VIDEOARTICLE_ID]/"></iframe>
{% endhighlight %}

### From Brightcove

Videos that don't live in Waldo/Ollie can be included if you have their Brightcove ID.

{% highlight html %}
<iframe width="640" height="360" frameborder="0" webkitallowfullscreen="webkitallowfullscreen" 
    allowfullscreen="allowfullscreen" mozallowfullscreen="mozallowfullscreen" 
    src="http://www.theatlantic.com/video/embed/?brightcove_id=[BRIGHTCOVE_ID]"></iframe>
{% endhighlight %}

**Optional:** You can add `&player=[playername]` to the end of the `src` to control which kind of player is served. This is mainly to separate 
advertising and analytics - you usually don't need it. The players are:

* `events` (for Atlantic Live)
* `features` (legacy)
* `cities` (for videos in the Cities account)
* `national-journal` (for NJ's videos that aren't imported into our system)

{% highlight html %}
<iframe width="640" height="360" frameborder="0" webkitallowfullscreen="webkitallowfullscreen" 
    allowfullscreen="allowfullscreen" mozallowfullscreen="mozallowfullscreen" 
    src="http://www.theatlantic.com/video/embed/?brightcove_id=[BRIGHTCOVE_ID]&player=[PLAYER]"></iframe>
{% endhighlight %}

### Full Width Video

Like images, wrap them in a `full-width` figure.

{% highlight html %}
<figure class="full-width">
    <iframe width="640" height="360" frameborder="0" webkitallowfullscreen="webkitallowfullscreen" 
        allowfullscreen="allowfullscreen" mozallowfullscreen="mozallowfullscreen" 
        src="..."></iframe>
</figure>
{% endhighlight %}
