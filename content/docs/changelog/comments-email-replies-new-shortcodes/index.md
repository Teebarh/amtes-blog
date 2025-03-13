---
title: "Comments, Email Replies & New Shortcodes"
date: "2025-03-10"
draft: true
layout:  centered # centered | default single
---

## Cusdis Comments

Add `enableComments: true` to posts to enable comments.

[Cusdis comment block]

## Frontmatter

### Display Header

Show or hide the header **on any page** via the `header` property:

```yaml {linenos=inline hl_lines=[6]}
title: "Dummy Title"
date: 2006-01-04
authors:
  - "john"
  - "doe"
header: false # default = true
```

### Page Subtitles

Add subtitles to **any page** via the `subtitle` property

```yaml {hl_lines=[2]}
title: "My Cool Title"
subtitle: "and an equally cool subtitle"
date: 2006-01-04
```

### Custom Fonts

Set custom page font with the `font` property. 

Available values include `Baskervville`, `Jost`, `RougeScript`, `SplineSansMono` and `Pretendard` (default):

**Baskervville**  
This is some text in Baskervville. Apparently this is said to be best for poetry or something. I'on know.
{.Baskervville}

**Jost**  
Jost looks classy. Use this when you're feeling spicy in your posts.
{.Jost}

**RougeScript**  
Nice font, but base size is a little too small. We can fix that by increasing the font size!
{.RougeScript .text-2xl}

**SplineSansMono**  
A very nice looking monospace font. Very demure, very mindful.
{.SplineSansMono}

## Cover and Fullwidth Images

Add a cover and full-width image at the start of any page.

```md {linenos=inline hl_lines=["4-8", 11]}
---
title: "Dummy Title"
date: 2006-01-04
cover:
  src: "/path/to/cover.jpg"
  alt: "description"
  width: "<int>" # default = 1500
  height: "<int>" # default = 750
---

{{</* fullwidth src="/path/to/image.jpg" alt="description" [optional] width="width" [optional] height="height" */>}}
```

**Params:**

- `src`: Image path
- `alt`: Image description
- `width`: [optional] Image width (defaults to 1920px)
- `height`: [optional] Image height (defaults to 768px)

{{< alert >}}
`src` allows local `(awesome-post/cover-image.jpg)` and external images `(https://example.com/image.jpg)`
{{< /alert >}}

## Reply By Email

Readers can now reply post authors directly via email. The `to` field takes the first author's email and `cc`'s all other authors.

{{< alert >}}
Emails now have the `+amtesblog` alias, making it easier for authors to create reply filters.
{{< /alert >}}

## Markdown Attributes

Enabled [markdown attributes](https://gohugo.io/content-management/markdown-attributes/). (Also supports TailwindCSS classes.)

For example, the font on this paragraph is different from
{.SplineSansMono}

this
{.Jost}

### Automatic last modified date

Posts with the `modified` or `lastmod` frontmatter field would automatically update their values.

```toml {linenos=inline linenostart=16 hl_lines=[3, "11-12"]}
enableEmoji = true

enableGitInfo = true

# googleAnalytics = "G-XXXXXXXXX"

[pagination]
  pagerSize = 100


[frontmatter]
  lastmod = ['lastmod', ':fileModTime']
```