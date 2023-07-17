# [[Normal Mode]]
Is the default mode of [[Vim]].
Allows you to edit and move around the cursor but you can't type anything.
It's optimised for text editing and navigation within the code base.

> [!info]- Motions
Motions are how you move around in [[Vim]], they are commands that when typed moves the cursor around with high speed and precision.

---

## Commands:

> ##### Basic Commands:
> - ``hjkl`` - left, down, up and right^[moves the cursor by one space]
> - ``i`` - switch to [[Insert Mode]]

##### Move by word:
- ``w`` - move to beginning of next word
- ``b`` - move to beginning of previous word
- ``e`` - move to end of next word
- ``ge``^[``g`` is toggle] - move to end of previous word

> *Capitalized equivalents* above move in [[WORD]] format

##### Find character:
- ``f{character}`` - find next occurrence of character
- ``F{character}`` - find previous occurrence of character
- ``t{character}`` - move until next occurrence of character
- ``T{character}`` - move until previous occurrence of character
- ``;`` - *repeat* same search forwards
- ``,`` - *repeat* same search backwards

##### Moving Horizontally:
- ``0`` - move to the beginning of line
- ``^`` - move to the first *non-blank character* of line
- ``$`` - move to the end of line
- ``g_`` - move to the *non-blank character* of line

##### Moving Vertically:
- ``{`` - jumps entire paragraph upwards
- ``}`` - same but downwards
- ``CTRL + D`` - move down half a page by scrolling
- ``CTRL + U`` - move up half a page by scrolling


