# Text Objects in [[Vim]]

Text objects are structured pieces of text that describe the parts in a document: words, sentences, quoted text, paragraphs, blocks, (HTML) tags, etc. You can use them in combination with [[Normal Mode Operators | operators]] to change a word, sentence, paragraph, etc.

The way that you specify a text object within a command is by combining the letter **`a`** (**a** text object plus whitespace) or **`i`** (**inner** object without whitespace) with a character that represents a text object itself:

![[Pasted image 20230727130259.jpg]]

```text
{operator}{a|i}{text-object}
```

- **`w`** for **w**ord
- **`s`** for **s**entence
- **`'`**, **`"`**, **`` ` ``** for quotes
- **`p`** for **p**aragraph
- **`b`** (or **`(`**, **`)`**) for block surrounded by **`()`,**
- **`B`** (or **`{`**, **`}`**) for block surrounded by **`{}`**
- **`<`**, **`>`** for a block surrounded by **`<>`**
- **`[`**, **`]`** for a block surrounded by **`[]`**
- **`t`** for tag.