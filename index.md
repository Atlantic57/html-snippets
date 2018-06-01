---
layout: main
---

# WYSWIYG Shortcode Library

## Shortcodes

### Eyebrow

```html
{% raw %}
{{% eyebrow classes="mb-8 block" %}} [EYEBROW_TEXT] {{% /eyebrow %}}
{% endraw %}
```

![](https://raw.githubusercontent.com/Atlantic57/html-snippets/gh-pages/images/eyebrow.png)

### Lede

```html
{% raw %}
{{% lead %}} [LEDE_TEXT] {{% /lead %}}
{% endraw %}
```

![](https://raw.githubusercontent.com/Atlantic57/html-snippets/gh-pages/images/lead.png)

### Pullquote

Add `no_quote="true"` to the pullquote tag to disable the quote icon appearing before the text.

Add `attribution=[ATTRIBUTION_TEXT]` if you'd like to attribute the quote to someone.

```html
{% raw %}
{{% pullquote no_quote="true" attribution="[ATTRIBUTION_TEXT]" %}}What is the role of public media in a multi-platform landscape?{{% /pullquote %}}
{% endraw %}
```

![](https://raw.githubusercontent.com/Atlantic57/html-snippets/gh-pages/images/pullquote.png)

### Blockquote

```
> [BLOCKQUOTE_TEXT]
```

![](https://raw.githubusercontent.com/Atlantic57/html-snippets/gh-pages/images/blockquote.png)

### Full-width Image

```html
{% raw %}
{{< image-full alt="[IMAGE_ALT_TEXT]" url="[IMAGE_URL]" >}}
{% endraw %}
```

![](https://raw.githubusercontent.com/Atlantic57/html-snippets/gh-pages/images/image.png)
