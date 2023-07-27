# Command line Mode in [[Vim]]

## EX commands
Starts with typing `:` to enter command line mode execute commands.

`:edit {relative-path-to-file}`,`:e` - open or create a file
`:write`,`:w` - save file
`:quit`,`:q` - close file
> **`:write`** will save a file but will fail if the file hasn’t changed or if it is readonly. Likewise **`:quit`** will close a file but will fail if the file has unsaved changes.

By adding `!` after `:` it forces a command to perform at all costs
- Use **`:write!`** (shorthand **`:w!`**) to save a file even if it’s been saved already or if it is readonly
- Use **`:quit!`** (shorthand **`:q!`**) to close a file without saving.

You can combine these commands to perform multiple actions:

- Use **`:wq`** to save and close a file

Or apply them to all the opened files at once:

- Use **`:wall`** (shorthand **`:wa`**) to save all files
- Use **`:qall`** (shorthand **`:qa`**) to close all files
- Use **`:wqall`** (shorthand **`:wqa`**) to save and close all files
- Use **`:qall!`** (shorthand **`:qa!`**) to close all files without saving

## Search commands
Starts with typing either `/` or `?` to enter command line mode to search patterns.
