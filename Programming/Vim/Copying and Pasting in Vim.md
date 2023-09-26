# Copying and Pasting in [[Vim]]

**Copy and paste**. Doesn’t sound like much excitement, does it? You are probably accustomed to using your mouse to select some text, copying or cutting it, and then pasting it somewhere else. That’s it. Not so much to get excited about.

Vim makes copying, cutting a tad bit more exciting by:

- giving you shiny operators and commands you can use in combination with all the motions you’ve learn thus far and by,
- providing a handful of registers where you can save stuff for later which can enable interesting workflows and help you recover text when you delete it by mistake

The two main commands for copying and pasting are **`y`** and **`p`**. Why use **`y`** to **c**opy instead of **`c`**, you may wonder? Well, if you remember from earlier chapters **`c`** is already taken, it is the **change** command. And thus, the Vi engineers had to come up with a colourful way to describe copying and came up with **y**ank. So in Vim you don’t copy stuff, you **yank** it (great naming… SO visceral). **`p`** stands for **p**ut but we can safely ignore that and keep calling it **p**aste. Because we’re indomitable rebels like that, and care nothing about what other people may think of us.

![Vim copy paste commands](https://www.barbarianmeetscoding.com/images/vim-copy-paste-commands.jpg "Vim copy paste commands")

## YANKING

**`y`** is an [[Normal Mode Operators|operator]]. You can combine it with any of the motions and text-objects you’ve learned to yank stuff to your heart’s desire:

- **`yl`** **y**anks a **l**etter,
- **`yaw`** **y**anks a **w**ord,
- **`yas`** **y**anks a **s**entence
- **`yi(`** **y**anks everything within **`(`** and so on…

If you double **`y`** as in **`yy`** you get **a linewise operator** like with **`dd`** and **`cc`** and yank a whole line. The **`Y`** command also yanks a complete line. I prefer to use **`yy`** but feel free to choose whichever you want.

## PASTING

In order to paste things you use the **`p`** command and its variants:

- **`p`** pastes something after the cursor
- **`P`** pastes something before the cursor
- **`gp`** same as **`p`** but puts the cursor after the pasted selection
- **`gP`** same as **`P`** and puts the cursor after the pasted selection

That’s an astounding amount of pasting flexibility right there.

Pasting in Vim is kind of special and the behavior of **`p`** and **`P`** depend on whether you’ve yanked characters or lines. If you’ve yanked **characters** then pasting will put those characters after or before the cursor (no surprises there). If you’ve yanked **lines**, however, pasting will put those lines after or before the line where the cursor is resting on.

![Vim useful copy pasting](https://www.barbarianmeetscoding.com/images/vim-useful-copy-pasting.jpg "Vim useful copy pasting")

**Want to duplicate a line?** It is as easy as typing **`yyp`**. _Want to n-plicate a line?_ It is as simple as typing **`yy{count}p`**. Yes! Counts also work with yank and pasting because they’re just commands! (sorry… Got way too excited just there).

If **`y`** copies stuff… How do you cut stuff in Vim? **Aha! Here comes a surprise!**

## CUTTING STUFF IN VIM

_Do you remember `d` and `c` from 10-ish minutes ago?_ Well, when I said that they deleted text into oblivion **I LIED!** They actually **cut** things. They were cutting text all along and you didn’t even notice. Text that you can later paste if that is what you want (**mindblown**).

**Want to swap some characters?** Type **`dlp`** (or **`xp`**). _Want to swap a couple of lines?_ Type **`ddp`**.

Excellent! So now you’ve boosted your knowledge with yanking, cutting and pasting in Vim. But there’s one element left that we haven’t even touched yet: **Registers**.

## MULTI-COPYING AND CUTTING WITH REGISTERS

Registers are like a special clipboard where you can save multiple things at once. The following registers are super useful:

- The **unnamed register** **`"`** is where you copy and cut stuff to, when you don’t explicitly specify a register. The default register if you will.
- The **named registers** **`a-z`** are registers you can use explicitly to copy and cut text at will
- The **yank register** **`0`** stores the last thing you have yanked (copied)
- The **cut registers** **`1-9`** store the last 9 things you cut by using either the delete or the change command

The **named registers** let you save bits of texts for later pasting. You can explicitly save on a register by using the following command:

```text
"{name of register}y{motion}
"{name of register}d{motion}
"{name of register}c{motion}
```

For instance, **`"ayas`** yanks a sentence and stores it in register **`a`**. Now if you want to paste it somewhere else, you can type **`"ap`**. Alternatively, using the capitalized version a register (i.e. **`A`** instead of **`a`**) appends whatever you copy or cut into that register.

The **yank register** lets you have access to what you copied last via the **`y`** command. This is helpful because deletes and changes don’t overwrite this register like they do the unnamed register.

The **cut registers** give you access to the last 9 things you deleted or changed. This is great if there’s some text that you deleted earlier and which you want to recover.

At any point in time, you can use the `:reg` command to see what is in your registers. Or you can type `:reg {register}` to inspect the contents of a specific register.

## PASTING IN INSERT MODE

All the commands we’ve seen thus far operate in _Normal mode_. What if you want to paste something when you’re in _Insert mode_? Well you can do that as well. Using `CTRL-R {register}` you can paste the contents of a register after the cursor:

- **`CTRL-R "`** pastes the contents of the unnamed register
- **`CTRL-R a`** pastes the contents of register **`a`**
- **`CTRL-R 0`** pastes the contents of the yank register

This being Visual Studio Code means that you can also rely on your system copy and pasting keys to paste text in **Insert Mode** [on-mac](https://www.barbarianmeetscoding.com/boost-your-coding-fu-with-vscode-and-vim/copy-paste/#fn-on-mac). That will probably be the most convenient for you in the majority of cases.

A final tip. Using _Insert mode_ to paste from a register removes the limitation of line-wise yanking and pasting. So using this method, you can yank a line and then paste it just after the cursor. Now go and enjoy some real copying and pasting!