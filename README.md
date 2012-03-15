Does exactly the same as the original [TextMate TODO bundle](https://github.com/textmate/todo.tmbundle), instead of analyzing the (self defined) LaTeX commands *\todo{}* and *\fixme{}*

You can define *\todo* like this:

    \newcommand{\todo}[1]{\textcolor{red}{\textbf{ToDo: }\nolinebreak#1\xspace}}

Please refer to the INSTALL file for installation instructions. I know, following these steps it's a bit annoying, but I couldn't figure out an easier way. If you know how, please contact me!
