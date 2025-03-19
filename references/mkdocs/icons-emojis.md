---
icon: material/emoticon-happy-outline
---

# Icons, Emojis

One of the best features of Material for MkDocs is the possibility to use [more
than 10,000 icons][icon search] and thousands of emojis in your project
documentation with practically zero additional effort. Moreover, [custom icons
can be added] and used in `mkdocs.yml`, documents and templates.

The following icon sets are bundled with Material for MkDocs:

- :material-material-design: – [Material Design]
- :fontawesome-brands-font-awesome: – [FontAwesome]
- :octicons-mark-github-16: – [Octicons]
- :simple-simpleicons: – [Simple Icons]

### Using emojis

Emojis can be integrated in Markdown by putting the shortcode of the emoji
between two colons. If you're using [Twemoji] (recommended), you can look up
the shortcodes at [Emojipedia]:

``` title="Emoji"
:smile:
```

<div class="result" markdown>

:smile:

</div>
  [Twemoji]: https://github.com/twitter/twemoji
  [Emojipedia]: https://emojipedia.org/twitter/

### Using icons

Icons can be used similar to emojis, by referencing
a valid path to any icon bundled with the theme, which are located in the
[`.icons`][custom icons] directory, and replacing `/` with `-`:

``` title="Icon"
:fontawesome-regular-face-laugh-wink:
```

<div class="result" markdown>

:fontawesome-regular-face-laugh-wink:

</div>

  [custom icons]: https://github.com/squidfunk/mkdocs-material/tree/master/material/templates/.icons

#### with colors

When [Attribute Lists] is enabled, custom CSS classes can be added to icons by
suffixing the icon with a special syntax. While HTML allows to use [inline
styles], it's always recommended to add an [additional style sheet] and move
declarations into dedicated CSS classes:

<style>
  .youtube {
    color: #EE0F0F;
  }
</style>

=== ":octicons-file-code-16: `docs/stylesheets/extra.css`"

    ``` css
    .youtube {
      color: #EE0F0F;
    }
    ```

=== ":octicons-file-code-16: `mkdocs.yml`"

    ``` yaml
    extra_css:
      - stylesheets/extra.css
    ```

After applying the customization, add the CSS class to the icon shortcode:

``` markdown title="Icon with color"
:fontawesome-brands-youtube:{ .youtube }
```

<div class="result" markdown>

:fontawesome-brands-youtube:{ .youtube }

</div>

  [Attribute Lists]: ../setup/extensions/python-markdown.md#attribute-lists
  [inline styles]: https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/style
  [additional style sheet]: ../customization.md#additional-css

#### with animations

Similar to adding [colors], it's just as easy to add [animations] to icons by
using an [additional style sheet], defining a `@keyframes` rule and adding a
dedicated CSS class to the icon:

=== ":octicons-file-code-16: `docs/stylesheets/extra.css`"

    ``` css
    @keyframes heart {
      0%, 40%, 80%, 100% {
        transform: scale(1);
      }
      20%, 60% {
        transform: scale(1.15);
      }
    }
    .heart {
      animation: heart 1000ms infinite;
    }
    ```

=== ":octicons-file-code-16: `mkdocs.yml`"

    ``` yaml
    extra_css:
      - stylesheets/extra.css
    ```

After applying the customization, add the CSS class to the icon shortcode:

``` markdown
:octicons-heart-fill-24:{ .heart }
```

<div class="result" markdown>

:octicons-heart-fill-24:{ .mdx-heart }

</div>

  [colors]: #with-colors
  [animations]: https://developer.mozilla.org/en-US/docs/Web/CSS/animation

### Icons, emojis in sidebars :smile:

With the help of the [built-in typeset plugin], you can use icons and emojis
in headings, which will then be rendered in the sidebars. The plugin preserves
Markdown and HTML formatting.

## Icon Sizes

<div class="grid cards" markdown>

- :fortinet-FortiGate: Standard

    ```html
    :fortinet-FortiGate:
    ```

- :fortinet-FortiGate:{ .lg .middle } Large

    ```html
    :fortinet-FortiGate:{ .lg }
    ```

- :fortinet-FortiGate:{ .xl .middle } X-Large

    ```html
    :fortinet-FortiGate:{ .xl }
    ```

- :fortinet-FortiGate:{ .xxl .middle } XX-Large

    ```html
    :fortinet-FortiGate:{ .xxl }
    ```

- :fortinet-FortiGate:{ .xxxl .middle } XXX-Large

    ```html
    :fortinet-FortiGate:{ .xxxl }
    ```

</div>
