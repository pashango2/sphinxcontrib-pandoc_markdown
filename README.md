sphinxcontrib-pandoc-markdown
=============================

It is an extension that you can use Markdown with Sphinx.


## Install

```
pip install sphinxcontrib-pandoc-markdown
```

## Requirement

[pandoc](http://pandoc.org/)


## Usage

Write the following in sphinx's `conf.py`.

```python
from sphinxcontrib.pandoc_markdown import MarkdownParser

source_suffix = [source_suffix, '.md']
source_parsers = {
   '.md': MarkdownParser,
}
```

## Future

### eval_rst
Can embed reStructuredText.

````
``` eval_rst
* This is a bulleted list.
* It has two items, the second
  item uses two lines.
```
````

### math

Inline math.
```
Since Pythagoras, we know that $a^2 + b^2 = c^2$.
```

Code block.

````
``` math
(a + b)^2 = a^2 + 2ab + b^2
(a - b)^2 = a^2 - 2ab + b^2
```
````

### note, warning, todo

````
```note
This is note.
```

```warning
This is warning.
```

```todo
This is todo.
```
````

### mermaid

````
```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
````

