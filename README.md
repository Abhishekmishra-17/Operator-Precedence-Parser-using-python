# Operator-Precedence-Grammar-
A grammar that is used to define mathematical operators is called an operator grammar or operator precedence grammar. Such grammars have the restriction that no production has either an empty right-hand side (null productions) or two adjacent non-terminals in its right-hand side.

# Example-

This is an example of operator grammar:
E->E+E/E*E/id 

However, the grammar given below is not an operator grammar because two non-terminals are adjacent to each other:

S->SAS/a 	 

A->bSb/b 

We can convert it into an operator grammar, though:

S->SbSbS/SbS/a

A->bSb/b  

This parser relies on the following three precedence relations: ⋖, ≐, ⋗

a ⋖ b This means a “yields precedence to” b.

a ⋗ b This means a “takes precedence over” b.

a ≐ b This means a “has same precedence as” b

# operator precedence parser-
An operator precedence parser is a bottom-up parser that interprets an operator grammar. This parser is only used for operator grammars. Ambiguous grammars are not allowed in any parser except operator precedence parser.

There are two methods for determining what precedence relations should hold between a pair of terminals:

The first method is to use the conventional associativity and precedence of operator.

The second method of selecting operator-precedence relations is first to construct an unambiguous grammar for the language, a grammar that reflects the correct associativity and precedence in its parse trees.
