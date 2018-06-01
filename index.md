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

### Lead

```html
{% raw %}
{{% lead %}} [LEDE_TEXT] {{% /lead %}}
{% endraw %}
```

### Pullquote

Add `no_quote="true"` to the pullquote tag to disable the quote icon appearing before the text.

Add `attribution=[ATTRIBUTION_TEXT]` if you'd like to attribute the quote to someone.

```html
{% raw %}
{{% pullquote no_quote="true" attribution="[ATTRIBUTION_TEXT]" %}}What is the role of public media in a multi-platform landscape?{{% /pullquote %}}
{% endraw %}
```

### Full-width Image

```html
{% raw %}
{{< image-full alt="[IMAGE_ALT_TEXT]" url="[IMAGE_URL]" >}}
{% endraw %}
```
