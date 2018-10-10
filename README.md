# Lambda-Calculus-Interpreter
A lambda calculus interpreter for a variant of lambda calculus PreL.


The BNF for PreL is as follows:

Program:
		{InputElement}
InputElement:
		Ignored
		Token
Ignored:
		(
		)
		Comment
		Whitespace
Comment:
		{ {CommentChar}	}
CommentChar:
		any	character	that	is	not	}
Whitespace:
any	character	recognized	by	Haskell's	Data.Char.isSpace
Token:
		Keyword
		Identifier
		Literal
		Operator
2
Keyword:
		(one	of)		
		if then else not \ . @
		
Identifier:
		AlphaChar	{AlphaChar} but	not	recognized	by	Keyword or	Literal
AlphaChar:
		any	character	recognized	by	Haskell's	Data.Char.isAlpha
Literal:
		Digit	{Digit}
		true
		false
Digit:
any character	recognized	by	Haskell's	Data.Char.isDigit
Operator:
		(one	of)
		+ - * / < <= > >= = /=
