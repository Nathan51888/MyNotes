# Insert Mode in [[Vim]]
Allows you to write text like any other text editor.

**Within Insert Mode**
- ``ESC``, ``CTRL + ]``, ``CTRL + C`` - switch to [[Normal Mode]]
- `CTRL-h` lets you delete the last character you typed
- `CTRL-w` lets you delete the last word you typed
- `CTRL-u` lets you delete the last line you typed


## PASTING IN INSERT MODE

All the commands we’ve seen thus far operate in _Normal mode_. What if you want to paste something when you’re in _Insert mode_? Well you can do that as well. Using `CTRL-R {register}` you can paste the contents of a register after the cursor:

- **`CTRL-R "`** pastes the contents of the unnamed register
- **`CTRL-R a`** pastes the contents of register **`a`**
- **`CTRL-R 0`** pastes the contents of the yank register

This being Visual Studio Code means that you can also rely on your system copy and pasting keys to paste text in **Insert Mode** [on-mac](https://www.barbarianmeetscoding.com/boost-your-coding-fu-with-vscode-and-vim/copy-paste/#fn-on-mac). That will probably be the most convenient for you in the majority of cases.

A final tip. Using _Insert mode_ to paste from a register removes the limitation of line-wise yanking and pasting. So using this method, you can yank a line and then paste it just after the cursor. Now go and enjoy some real copying and pasting!