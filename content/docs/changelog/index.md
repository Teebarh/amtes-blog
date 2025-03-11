---
title: "Changelog"
date: "2025-03-10T12:56:28+01:00"
modified:
font: SplineSansMono
---

# Welcome to The Changelog

This changelog tracks updates and improvements to the AMTES blog. Each entry documents new features, improvements, and breaking changes.

## Latest Update (2025-03-10)

### New Features

- Added open-source comment system: [Cusdis](https://cusdis.com)
- Added `subtitle` frontmatter property
- Added 4 new fonts: Baskervville, Jost, RougeScript, and SplineSansMono

### Improvements

- Modified layouts: `centered`, `single`
- Changed site's default font to Pretendard
- Enhanced `replyByEmail` functionality for multiple authors
- Modified header for better cover image rendering

### New Shortcodes

- `fullwidth`: Display full-width images
- `pullquote`: Create highlighted quotes
- `blockquote`: Standard quote blocks
- `bigquote`: Large-format quotes
- `script`: Include external scripts
- `arena`: Arena.im integration

### Cover and Fullwidth Images

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

{{< alert >}}
`src` allows local `(awesome-post/cover-image.jpg)` and external images `(https://example.com/image.jpg)`
{{< /alert >}}

### Frontmatter properties

#### Header

Show or hide the header **on all page types** via the `header` property:

```yaml
title: "Dummy Title"
date: 2006-01-04
authors:
  - "john"
  - "doe"
header: false # default = true
```

#### Subtitles

Add subtitles to **any page** via the `subtitle` property

```yaml {hl_lines=[2]}
title: "My Cool Title"
subtitle: "and an equally cool subtitle"
date: 2006-01-04
```

#### Reply By Email

Readers can now reply post authors directly via email. The `to` field takes the first author's email and `cc`'s all other authors.

{{< alert >}}
Emails now have the `+amtesblog` alias, making it easier for authors to create reply filters.
{{< /alert >}}

#### Cusdis Comments

Add `enableComments: true` to posts to enable comments.

### Markdown Attributes

Enabled [markdown attributes](https://gohugo.io/content-management/markdown-attributes/). (Also supports TailwindCSS classes.)

```toml {linenos=inline hl_lines=["8-11"]}
# -- Markup --
# These settings are required for the theme to function.

[goldmark]
  [goldmark.renderer]
    unsafe = true

  [goldmark.parser]
    [goldmark.parser.attribute]
      block = true
      title = true

[highlight]
  style = 'native'

[tableOfContents]
  startLevel = 2
  endLevel = 4
```

#### Fixed Heading Attributes

Fixed the issue where headings were not allowing attributes by overriding `render-heading.html`. For more details, refer to the [source](https://discourse.gohugo.io/t/adding-class-to-heading-not-working-while-attribute-adds-just-fine/53048/6).

```html {linenos=inline hl_lines=[3]}
{{ $strAnchor := urlize .Anchor }}
{{ $replacedAnchor := replaceRE "%25" "" $strAnchor }}
<h{{ .Level }} class="relative group {{ .Attributes.class }}">{{ .Text | safeHTML }} ## Added {{ . Attributes.class }}
    <div id="{{ .Anchor | safeURL | urlize }}" class="anchor"></div>
    {{ if.Page.Params.showHeadingAnchors | default (.Page.Site.Params.article.showHeadingAnchors | default true) }}
    <span
        class="absolute top-0 w-6 transition-opacity opacity-0 ltr:-left-6 rtl:-right-6 not-prose group-hover:opacity-100">
        <a class="group-hover:text-primary-300 dark:group-hover:text-neutral-700"
            style="text-decoration-line: none !important;" href="#{{ $replacedAnchor | safeURL }}" aria-label="{{ i18n "
            article.anchor_label" }}">#</a>
    </span>
    {{ end }}
</h{{ .Level }}>
```

### Automatic last modified date

Posts with the `modified` or `lastmod` frontmatter field would automatically update their values.

```toml {linenos=inline linenostart=16 hl_lines=[3, "11-12"]}
enableEmoji = true

enableGitInfo = true

# googleAnalytics = "G-XXXXXXXXX"

[pagination]
  pagerSize = 100


[frontmatter]
  lastmod = ['lastmod', ':git', ':fileModTime']
```
