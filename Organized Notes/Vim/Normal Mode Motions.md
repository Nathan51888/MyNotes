# Motions in [[Normal Mode]]

Motions are how you move around in [[Vim]], they are commands that when typed moves the cursor around with high speed and precision.

### Basics
- ``hjkl`` - move left, down, up and right^[moves the cursor by one space]
- ``gg`` - go to top of the file
- ``G`` - go to end of file
- ``{line}gg`` - go to specific line
- ``%`` - jump between the matching `({[]})`

### Move by Word
- ``w`` - move to beginning of next word
- ``b`` - move to beginning of previous word
- ``e`` - move to end of next word
- ``ge``^[``g`` is toggle] - move to end of previous word

> *Capitalized equivalents* above move in [[WORD]] format

### Find Character
- ``f{character}`` - find next occurrence of character in a line
- ``F{character}`` - find previous occurrence of character in a line
- ``t{character}`` - move until next occurrence of character in a line
- ``T{character}`` - move until previous occurrence of character in a line
- ``;`` - *repeat* same search forwards
- ``,`` - *repeat* same search backwards

### Find Pattern
- ``/{pattern}`` - search forwards in file
- ``?{pattern}`` - search backwards in file
- ``*``,``#`` - search word under cursor forwards/backwards
- ``n``,``N`` - jump to next/previous match
- `gn`,`gN`

>[!info] **`gn`** works as follows:
>
> 1. If you are on top of a search match, it selects the match in [[Visual mode]].
> 2. If you are in [[Visual mode]], it extends your current selection until the end of the next match.
> 3. If you are in _Operator-pending mode_, **it operates on the next match**.

### Moving Horizontally
- ``0`` - move to the beginning of line
- ``^`` - move to the first *non-blank character* of line
- ``$`` - move to the end of line
- ``g_`` - move to the *non-blank character* of line

### Moving Vertically
- `gk`,`gj` - navigate wrapped lines
- ``{`` - jumps entire paragraph upwards
- ``}`` - same but downwards
- ``CTRL + D`` - move down half a page by scrolling
- ``CTRL + U`` - move up half a page by scrolling

### Moving Semantically
- ``gd`` - jump to definition of whatever is under your cursor
- ``gf`` - jump to a file in an import