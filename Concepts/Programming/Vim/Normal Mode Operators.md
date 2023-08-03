# Operators in [[Normal Mode]]

**Operators are commands you can do from [[Normal Mode]] to edit texts and other functions.** 
You can use operators and motions together by following any of these patterns:

```text
{operator}{count}{motion}
{count}{operator}{motion}
```


**Basics**
- ``.`` - repeat the last command
- ``u`` - undo
- ``CTRL + r`` - redo

**[[Insert Mode]]** 
- ``i`` - insert before cursor
	 - ``I`` - insert at beginning of line
- ``a`` - insert after cursor
	 - ``A`` - insert at end of line
- `o` - insert a new line below
	- `O` - insert a new line above
- `gi` - puts you to the last change you made while in insert mode

**[[Visual Mode]]**
 - ``v`` - enter character visual mode
	 - ``V`` - enter line visual mode
	 - ``CTRL + v`` - enter visual block

**Editing**
 - ``x`` - delete character under cursor
	 - ``X`` - delete character before cursor
 - ``s`` - delete character under cursor and go into insert mode
 - ``r`` - replace single character on cursor
 - ``y`` - yank(copy)
	 - `yy` - yank whole line
 - ``p`` - paste
	 - `P` - paste before cursor
	 - `gp`,`gP` - puts the cursor after the pasted section
 - ``d`` - delete
	 - ``d{count}`` - delete up to line count
	 - ``dd`` - delete line
	 - ``D`` - delete from cursor to end of line
 - ``c`` - change[^1]
	 - `cc` - changes a complete line
	 - `C` - changes from the cursor until the end on the line

> *Yanking*, *pasting* over and *deleting* lines goes into the *same* clipboard(same as the cut function)

 - ``~`` - switch case for single character
 - ``g~`` - switch case between lower and upper case
	 - ``gu`` - switch to lower case
	 - ``gU`` - switch to Upper case
 - ``>`` - adds indentation
 - ``<`` - removes indentation
 - ``=`` - formats code

> *Double* an operator and it functions on a *whole line*, *Capital* versions makes it do an *alternate* version of its default behaviour.

**[[Text Objects]]**
- **`w`** for **w**ord
- **`s`** for **s**entence
- **`'`**, **`"`**, **`` ` ``** for quotes
- **`p`** for **p**aragraph
- **`b`** (or **`(`**, **`)`**) for block surrounded by **`()`,**
- **`B`** (or **`{`**, **`}`**) for block surrounded by **`{}`**
- **`<`**, **`>`** for a block surrounded by **`<>`**
- **`[`**, **`]`** for a block surrounded by **`[]`**
- **`t`** for tag.



[^1]: ``d`` and ``i`` combined in one key press