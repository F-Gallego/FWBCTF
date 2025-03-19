---
icon: material/code-json
---

# Embedding external files

When [Snippets] is enabled, content from other files (including source files)
can be embedded by using the [`--8<--` notation][Snippets notation] directly
from within a code block:

```` markdown
``` title="file.sh"
;--8<-- "file.sh"
```
````

<div class="result" markdown>

``` title="file.sh"
#!/bin/bash
#
for entry in ls
do
  echo $entry
done
exit 0
```

</div>

  [Snippets notation]: https://facelessuser.github.io/pymdown-extensions/extensions/snippets/#snippets-notation

