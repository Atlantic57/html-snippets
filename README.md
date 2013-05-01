HTML Code Snippets
=============

A convenient reference for Atlantic writers.


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

## Related Content

### See Also

    <!-- START "SEE ALSO" v. 1 -->
    <aside class="callout">
        <hr/>
        <h4>See also</h4>
        <h5>(Optional subtitle)</h5>
        <p>Text goes here</p>
        <hr/>
    </aside>
    <!-- END "SEE ALSO" v. 1 -->


### "More on" Box

    <!-- START "MORE ON" SINGLE STORY BOX v. 2 -->
    <aside class="callout">
        <h4>Related Story</h4>
        <div>
            <a href="[URL]">
                <img style="width: 242px; height: 157px;" src="[THUMBNAIL URL]" />
            </a>
        </div>
        <p>
            <a href="[URL]">
                [HEADLINE]
            </a>
        </p>
    </aside>
    <!-- END "MORE ON" SINGLE STORY BOX v. 2 -->

### "More on" list box, with image

    <!-- START "MORE ON" LIST BOX v. 3 -->
    <aside class="callout">
        <hr>
        <h4>More From Quartz</h4>
        <div>
            <a href="[URL]">
                <img style="width: 242px; height: 157px;" src="[THUMBNAIL URL]" />
            </a>
        </div>

        <ul>
            <li><a href="[URL]">[HEADLINE 1]</a></li>
            <li><a href="[URL]">[HEADLINE 2]</a></li>
            <li><a href="[URL]">[HEADLINE 3]</a></li>
        </ul>

        <hr>
    </aside>
    <!-- END "MORE ON" LIST BOX v. 3 -->

### "More on" list box, no image

    <!-- START "MORE ON" LIST BOX NO IMAGE v. 3 -->
    <aside class="callout">
        <hr>
        <h4>More From Quartz</h4>
        <ul>
            <li><a href="[URL]">[HEADLINE 1]</a></li>
            <li><a href="[URL]">[HEADLINE 2]</a></li>
            <li><a href="[URL]">[HEADLINE 3]</a></li>
        </ul>
        <hr>
    </aside>
    <!-- END "MORE ON" LIST BOX v. 3 -->

### Study of the Day, Dr. Hamblin, and "More On" lists with lead images

    <!-- START "MORE STUDY OF THE DAY" BOX v. 1 -->
    <aside class="callout">
       <hr>
        <a href="http://www.theatlantic.com/health/category/studies">
            <img width="242" alt="NJ logo.JPG" 
                    src="http://cdn.theatlantic.com/static/front/images/bugs/studyoftheday.png">
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
       <hr>
    </aside>
    <!-- END "MORE STUDY OF THE DAY" BOX v. 1 -->

### Related Video

    <!-- START "RELATED VIDEO" SINGLE STORY BOX v. 1 -->
    <aside class="callout">
        <hr/>
        <h4>Related Video</h4>
        <a class="related-video-link" href="[ARTICLE URL]">
            <img width="242" src="[THUMBNAIL URL]" />
       </a>
        <p>
            <a href="[ARTICLE URL]">
                [HEADLINE]
            </a>
        </p>
        <hr/>
    </aside>
    <!-- END "RELATED VIDEO" SINGLE STORY BOX v. 1 -->


### Multiple "More on" list with thumbnails

    <!-- START MULTI-THUMB "MORE ON" WITH IMAGES v. 3 -->
    <aside class="callout">
      <hr>
      <h4>More on [SUBJECT]</h4>
      <ul class="with-thumbs">
        <li>
          <a href="[ARTICLE URL]">
            <img width="90" src="[THUMBNAIL URL]">
            [ARTICLE TITLE]
          </a>
        </li>

        <li>
          <a href="[ARTICLE URL]">
            <img width="90" src="[THUMBNAIL URL]">
            [ARTICLE TITLE]
          </a>
        </li>

        <li>
          <a href="[ARTICLE URL]">
            <img width="90" src="[THUMBNAIL URL]">
            [ARTICLE TITLE]
          </a>
        </li>

      </ul>
      <hr>
    </aside>
    <!-- END MULTI-THUMB "MORE ON" WITH IMAGES v. 3 -->

