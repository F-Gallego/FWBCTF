---
icon: material/table-edit
---

# Data tables

Data tables can be used at any position in your project documentation and can
contain arbitrary Markdown, including inline code blocks, as well as [icons and
emojis]:

``` markdown
| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | :material-check:     Fetch resource  |
| `PUT`       | :material-check-all: Update resource |
| `DELETE`    | :material-close:     Delete resource |
```

<div class="result" markdown>

| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | :material-check:     Fetch resource  |
| `PUT`       | :material-check-all: Update resource |
| `DELETE`    | :material-close:     Delete resource |

</div>

  [icons and emojis]: icons-emojis.md

### Column alignment

If you want to align a specific column to the `left`, `center` or `right`, you
can use the [regular Markdown syntax] placing `:` characters at the beginning
and/or end of the divider.

=== "Left"

    ``` markdown hl_lines="2"
    | Method      | Description                          |
    | :---------- | :----------------------------------- |
    | `GET`       | :material-check:     Fetch resource  |
    | `PUT`       | :material-check-all: Update resource |
    | `DELETE`    | :material-close:     Delete resource |
    ```

    <div class="result" markdown>

    | Method      | Description                          |
    | :---------- | :----------------------------------- |
    | `GET`       | :material-check:     Fetch resource  |
    | `PUT`       | :material-check-all: Update resource |
    | `DELETE`    | :material-close:     Delete resource |

    </div>

=== "Center"

    ``` markdown hl_lines="2"
    | Method      | Description                          |
    | :---------: | :----------------------------------: |
    | `GET`       | :material-check:     Fetch resource  |
    | `PUT`       | :material-check-all: Update resource |
    | `DELETE`    | :material-close:     Delete resource |
    ```

    <div class="result" markdown>

    | Method      | Description                          |
    | :---------: | :----------------------------------: |
    | `GET`       | :material-check:     Fetch resource  |
    | `PUT`       | :material-check-all: Update resource |
    | `DELETE`    | :material-close:     Delete resource |

    </div>

=== "Right"

    ``` markdown hl_lines="2"
    | Method      | Description                          |
    | ----------: | -----------------------------------: |
    | `GET`       | :material-check:     Fetch resource  |
    | `PUT`       | :material-check-all: Update resource |
    | `DELETE`    | :material-close:     Delete resource |
    ```

    <div class="result" markdown>

    | Method      | Description                          |
    | ----------: | -----------------------------------: |
    | `GET`       | :material-check:     Fetch resource  |
    | `PUT`       | :material-check-all: Update resource |
    | `DELETE`    | :material-close:     Delete resource |

    </div>

  [regular Markdown syntax]: https://www.markdownguide.org/extended-syntax/#tables

### Import table from file

```html
{{ read_csv('path_to_table.csv') }}
```

## Aligning columns

Text columns will be aligned to the left [by default](https://github.com/astanin/python-tabulate#column-alignment), whilst columns which contain only numbers will be aligned to the right. You can override this behaviour using [tabulate](https://pypi.org/project/tabulate/)'s [custom column alignment](https://github.com/astanin/python-tabulate#custom-column-alignment). Example:

=== ":arrow_left: left"

    <code>\{\{ read_csv('tables/basic_table.csv', colalign=("left",)) \}\}</code>

    {{ read_csv('tables/basic_table.csv', colalign=("left",)) }}

=== ":left_right_arrow: center"

    <code>\{\{ read_csv('tables/basic_table.csv', colalign=("center",)) \}\}</code>

    {{ read_csv('tables/basic_table.csv', colalign=("center",)) }}

=== ":arrow_right: right"

    <code>\{\{ read_csv('tables/basic_table.csv', colalign=("right",)) \}\}</code>

    {{ read_csv('tables/basic_table.csv', colalign=("right",)) }}

## Sortable tables

If you use [mkdocs-material](https://squidfunk.github.io/mkdocs-material), you can configure [sortable tables](https://squidfunk.github.io/mkdocs-material/reference/data-tables/?h=tables#sortable-tables).

## Number formatting

You can use [tabulate](https://pypi.org/project/tabulate/)'s [number formatting](https://github.com/astanin/python-tabulate#number-formatting). Example:

=== ":zero:"

    <code>\{\{ read_fwf('tables/fixedwidth_table.txt', floatfmt=".0f") \}\}</code>

    {{ read_fwf('tables/fixedwidth_table.txt', floatfmt=".0f") }}

=== ":one:"

    <code>\{\{ read_fwf('tables/fixedwidth_table.txt', floatfmt=".1f") \}\}</code>

    {{ read_fwf('tables/fixedwidth_table.txt', floatfmt=".1f") }}

=== ":two:"

    <code>\{\{ read_fwf('tables/fixedwidth_table.txt', floatfmt=".2f") \}\}</code>

    {{ read_fwf('tables/fixedwidth_table.txt', floatfmt=".2f") }}

