# Visual Mode in [[Vim]]

_Visual mode_ uses the same [[Normal Mode Motions|motions]] you use in [[Normal Mode]] to select and edit text.

It works in the opposite way of [[Normal Mode]]. In [[Normal Mode]] you first define the operator and then a motion that represents some text to which to apply that operator:

```text
{operator}{count}{motion}
```

In _Visual mode_, however, you select the text first and **then** you type the operator:

```text
{trigger visual mode}{motion}{operator}
```