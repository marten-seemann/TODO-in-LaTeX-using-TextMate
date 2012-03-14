Does exactly the same as the original [TextMate TODO bundle](https://github.com/textmate/todo.tmbundle), instead of analyzing the (self defined) LaTeX commands *\todo{}* and *\fixme{}*

You can define *\todo* like this:

    \newcommand{\todo}[1]{\textcolor{red}{\textbf{ToDo: }\nolinebreak#1\xspace}}

In the future I'm going to add a LaTeX package as well as a syntax highlighting of these two commands in the TextMate LaTeX bundle.