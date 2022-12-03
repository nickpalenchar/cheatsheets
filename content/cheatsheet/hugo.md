---
title: "Hugo"
date: 2022-12-03T08:04:42-05:00
draft: true
---


## Templating

### Markdown

Items in `content/*` are markdown and can have templates

```
{{ somevalue }} = interpolate a value
{{< shortcode >}} = add a shortcode (see Shortcodes)
{{% shortcode %}} = add a shortcode (see Shortcodes)
```

## Shortcodes

Used in **markdown** documents (under `content`)

```
{{< shortcode-name >}} = layouts/shortcode-name.html
{{% shortcode-name >}} = layouts/shortcode-name.md 
```

```html
<h1> this is a shortcode!</h1>
```

### Params

```
{{< shortcode-name "foo" "bar"  >}} (positional args)
{{< shortcode-name foo="bar" >}} (named arg)
```

accessed in shortcode with `.Get`

```
{{ .Get 0 }} and {{ .Get 1 }} (positional)

{{ .Get "foo" }} (named{
```


