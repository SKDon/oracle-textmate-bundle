# Installing #

See the [Installation Guide](InstallationGuide.md) for details on installing this bundle.

# Syntax #

The included syntax does not rely on the SQL bundle distributed with TextMate (which is mainly aimed at just SQL content, whereas this bundle is designed more for PL/SQL.

The syntax distinguishes various keywords, etc for highlighting.  A number of internal Oracle functions have been included.  These are expected to be the ones most used in order not to overrun the configuration.  If you find there are functions you use which are not included, you can use the Bundle Editor to add them.  Just scroll to the appropriate section in the syntax and add them to the regular expression.

I use variables starting _pi`_`_, _po`_`_ and _pio`_`_ for function and procedure parameters and _l`_`_ for local variable, so these are identified in the syntax, too.  Feel free to alter these definitions to suit your coding style.

# Indentation #

The indentation rules will indent `BEGIN`, `IF` and `LOOP` blocks.  The `EXCEPTION` keyword will be at the same level as the surrounding `BEGIN` block with the exception bodies indented one level.  This is to enable full auto-indenting to work correctly.

Multi-line procedure and function calls and multi-line declarations will not be indented.  I have yet to determine a suitable definition which will allow this consistently.

# Folding #

Folding is enabled for `BEGIN`, `IF` and `LOOP` blocks.

# Symbols #

Package, function and procedure names will all be added to the symbol list.  This means you can quickly and easily navigate between them using the symbol selector in the status bar at the bottom of the edit window.

# Commands #

A number of commands have been defined.  These are based on the Oracle bundle created by [Jesper Hvirring Henriksen](http://productive.dk/2006/09/25/oracle-bundle-for-textmate-preview.html).

## Search Oracle Docs for Selection or Word ##

This command searches for the selected text (or the current word if there is no selection) in the online [Oracle documentation](http://www.oracle.com/pls/db111/db111.homepage).

## Run Script ##

This command runs the current file using SQL\*Plus.

## Run Selection or Line ##

This command takes the selected text (or the current line if there is no selection) and runs it in SQL\*Plus.

## Describe Selection or Word ##

This command takes the selected text (or the current word if there is no selection) and runs a `describe` on it in SQL\*Plus.

## Open SQL\*Plus ##

This command starts an interactive SQL\*Plus session in a Terminal window.

## Find Procedure ##

This command will search for a procedure or function in a package body with the name of the current word.  If it is found, the file containing it is shown and the cursor moves to the start of the procedure or function.

# Importing Files #

If you drag a file from the Finder into an edit window, the contents of that file will be imported at the point you release the mouse button.

# Tab Triggers #

The following Tab Triggers are defined.  Note that some of these reflect my own coding usage and style, but these are easily customised for your own use.

The trigger for each is shown here in brackets against the name.

## New Procedure [proc

&lt;TAB&gt;

] ##

Inserts a snippet consisting of a stub for a new procedure.

## New Function [func

&lt;TAB&gt;

] ##

Inserts a snippet consisting of a stub for a new function.

## begin ... end [begin

&lt;TAB&gt;

] ##

Inserts a `BEGIN` ... `EXCEPTION` ... `END` block.

## if ... else ... end [ife

&lt;TAB&gt;

] ##

Inserts an `IF` ... `ELSE` ... `END IF` block.

## if ... end [if

&lt;TAB&gt;

] ##

Inserts an `IF` ... `END IF` block.

## elsif ... [e

&lt;TAB&gt;

] ##

Inserts an `ELSIF` section.

## loop ... end [loop

&lt;TAB&gt;

] ##

Inserts a `LOOP` ... `END LOOP` block.

## log print [print

&lt;TAB&gt;

] ##

Inserts a call to a log routine for information messages.

## log debug [debug

&lt;TAB&gt;

] ##

Inserts a call to a log routine for debug messages.

## log error [error

&lt;TAB&gt;

] ##

Inserts a call to a log routine for error messages.

## fail [fail

&lt;TAB&gt;

] ##

Inserts an `IF` block based on a failure result code.

## success [success

&lt;TAB&gt;

] ##

Inserts an `IF` block based on a success result code.

# Templates #

There are two templates available.  One for creating a package spec file and one for creating a package body file.