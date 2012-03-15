For installing this functionality, unfortunately you have to perform two steps manually.

The first step is the installation of the [./TODO in LaTeX.tmbundle](TODO in LaTeX.tmbundle) bundle. This bundle adds the capability to create a ToDo list from your LaTeX document by search for the *\todo{}* and *\fixme{}* commands.

The second step is the modification of the LaTeX TextMate Bundle. The [./Latex ToDo.tmLanguage](Latex ToDo.tmLanguage) adds two new scopes so that syntax highlighting the *\todo{}* and *\fixme{}* commands becomes possible. If you can live without this highlighting, you can completely skip this step.

# Step 1
Just doubleclick on the [./TODO in LaTeX.tmbundle](TODO in LaTeX.tmbundle). TextMate will install it automatically. After installation, a bundle called *TODO in LaTeX* should appear in your bundle list.

# Step 2
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