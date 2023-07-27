# Counts in [[Normal Mode ]]

**Counts are numbers which let you multiply the effect of a [[Normal Mode Operators|command]]**. You can use them by prefixing any command with a count like so:

```text
{count}{command}
```

For instance:

- **`2w`** allows us to move the cursor 2 words forward.
- **`5j`** changes your cursor position to 5 lines below.
- **`3;`** lets you go to the next third occurrence of a character.
- **`2/baby`** sends you flying to the second occurrence of `baby` in a document.

In general, use **`{count}{motion}`** to multiply a motion **`{count}`** times.