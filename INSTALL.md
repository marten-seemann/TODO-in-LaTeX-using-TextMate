For installing this functionality, unfortunately you have to perform three steps manually.

The first step is the installation of the LaTeX package which provides the needed commands.

The second step is the installation of the [./TODO in LaTeX.tmbundle](TODO in LaTeX.tmbundle) bundle. This bundle adds the capability to create a ToDo list from your LaTeX document by search for the *\todo{}*, *\todo\*{}*, *\fixme{}* and *\fixme\*{}* commands.

The third step is the modification of the LaTeX TextMate Bundle. The [./Latex ToDo.tmLanguage](Latex ToDo.tmLanguage) adds two new scopes so that syntax highlighting the *\todo{}* and *\fixme{}* commands becomes possible. If you can live without this highlighting, you can completely skip this step.

# Step 1
Install the LaTeX commands *\todo{}*, *\todo\*{}*, *\fixme{}* and *\fixme\*{}*. They are provided in the LaTeX package [todo_fixme.sty](TODO-in-LaTeX-using-TextMate/blob/master/todo_fixme.sty). Just copy this file into the folder where the .tex file resides or install it into the sty-directory (which one depends on your OS and your LaTeX package).

# Step 2
Just doubleclick on the [./TODO in LaTeX.tmbundle](TODO in LaTeX.tmbundle). TextMate will install it automatically. After installation, a bundle called *TODO in LaTeX* should appear in your bundle list.

# Step 3
Add the [./Latex ToDo.tmLanguage](Latex ToDo.tmLanguage) to TextMate by double clicking. Then open the Bundle Editor and move the language called *LaTeX ToDo* into the LaTeX Bundle.
Then edit the language *LaTeX* inside the LaTeX Bundle. Add the following line before the inclusion of *text.tex*.

    {	include = 'text.tex.latex.todo'; },

The last few lines of this language will then look somehow like this:

    			};
    		},
    		{	include = 'text.tex.latex.todo'; },
    		{	include = 'text.tex'; },
    	);
    }
    
Now close the Bundle Editor. You can now define the syntax highlighting in TextMate Preferences section *Fonts & Colors*. Color them whatever you like. The required Scope Selectors are:

    support.function.todo.todo.latex
    support.function.todo.fixme.latex    