---
icon: material/plus-circle
---

# Annotations

One of the flagship features of Material for MkDocs is the ability to inject
annotations – little markers that can be added almost anywhere in a document
and expand a tooltip containing arbitrary Markdown on click or keyboard focus.

## Usage

Annotations consist of two parts: a marker, which can be placed anywhere in
a block marked with the `annotate` class, and content located in a list below
the block containing the marker:

``` markdown
This is an interesting point, (1) and more interesting things.
{ .annotate }

1.  :man_raising_hand: I'm an annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be expressed in Markdown.
```

<div class="result" markdown>

This is an interesting point, (1) and more interesting things.
{ .annotate }

1.  :man_raising_hand: I'm an annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be written in Markdown.

</div>

#### in admonitions

The titles and bodies of [admonitions] can also host annotations by adding the
`annotate` modifier after the type qualifier.

``` markdown
!!! note annotate "Annotation inside admonition (1)"

    This is an interesting point, (2) and more interesting things. Making more
    topics. Other interesting points can be used to describe the idea
    in the sentence.

1.  :man_raising_hand: I'm an annotation!
2.  :woman_raising_hand: I'm an annotation as well!
```

<div class="result" markdown>

!!! note annotate "Annotation inside admonition (1)"

    This is an interesting point, (2) and more interesting things. Making more
    topics. Other interesting points can be used to describe the idea
    in the sentence.

1.  :man_raising_hand: I'm an annotation!
2.  :woman_raising_hand: I'm an annotation as well!

</div>

  [admonitions]: admonitions.md

