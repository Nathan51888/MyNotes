# [[WORD]]

A *word* in [[Vim]] is either:
- A sequence of letters, digits and numbers
- A sequence of non-blank characters

A **WORD** includes special characters like ``,``,``(``,``{`` and etc:

	this is a WORD: Iam_A_WORD(WORD) 
	this function call sum(2,3) is also a WORD 
	this array [1,2,3,4,5] is a WORD as well

In general, *word* motions allow for more precise changes while **WORD** motions allow for faster movement.