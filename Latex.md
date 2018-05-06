# Latex tutorial

[Reference](https://www.sharelatex.com/learn/Learn_LaTeX_in_30_minutes)

## Very begining

### Class
The class(the type of document) is declared in the first line of code.
```
\documentclass{article}
\documentclass{book}
```

### Preamble
Everything before *\begin{document}* is the preamble.

```
# Parameters in the square brackets must be comma-separated
# (9pt, 11pt, 12pt), (letterpaper, a4paper, legalpaper)
\documentclass[12pt, letterpaper]{article}

# Encoding, uusally utf-8
\usepackage[utf8]{inputenc}

# Title
\title{document name}

# Author
\author{LWW}

# Thanks
\title{learn \thanks{funded by the ShareLaTeX team}}

# Date
\date{February 2014}
\date{\today}
```

Details:
[Page size and margins](https://www.sharelatex.com/learn/Page_size_and_margins)

### Body

Begin and end the content
```
\begin{document}

# To print the information (title, author, and date) on the document. In the __body__ of the documents
\maketitle

content..._body_ of the document

# Comments
% This line here is a comment. It will not be printed in the document.

\end{document}
