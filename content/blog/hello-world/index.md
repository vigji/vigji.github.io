---
title: "Hello, World"
date: 2026-02-26
description: "A first post, and a test of Tufte-style typography."
draft: false
---

{{< epigraph author="Edward Tufte" cite="The Visual Display of Quantitative Information" >}}
The commonality between science and art is in trying to see profoundly — to develop strategies of seeing and showing.
{{< /epigraph >}}

{{< newthought >}}This is a first post{{< /newthought >}} on a freshly rebuilt site. It exists mostly to test the typographic features of Tufte CSS, and partly because starting a blog without a first post feels like hanging an empty picture frame.

## Sidenotes and margin notes

The beauty of Tufte's layout is its generous margins.{{< sidenote >}}Sidenotes like this one are numbered and appear in the margin. On mobile, they collapse to inline toggles.{{< /sidenote >}} Margin notes work similarly but without numbers.{{< marginnote >}}This is a margin note — no number, just a quiet aside.{{< /marginnote >}}

The idea is simple: supporting information belongs in the periphery, not in the body text. Footnotes force the reader to bounce to the bottom of the page; sidenotes keep everything in view.

## Code

Here is a block of Python, since that is what I write most:

```python
import numpy as np

def heading_direction(velocities):
    """Integrate heading from angular velocities."""
    return np.cumsum(velocities) % (2 * np.pi)
```

## What to expect

I plan to write about data science, neuroscience, Python tooling, and the occasional stray thought. No schedule, no promises. Just writing when something feels worth sharing.
