PURPOSE:

The Advanced Annotation Search plugin allows user to perform logical search operations on large ontologies (via Protege) to find the entities they need based on existing annotation information.

QUICK NOTICE:

You don't need quotes around anything expect if you're searching annotations for a multiple-word expression.

EXAMPLES:

#1
If you know some annotation contains a word or phrase, put that word or phrase in quotes ("") and click search. (e.g. "opercle", ""whatever you want"")

#2
If you know the comment of the entity you want to find contains the string "I like puppies", you can use the query (minus the outer quotations): "comment contains "i like puppies""

#3
If you know the entity has an "age" annotation and you know the age of the entity is greater than 3 but less than 9, you can type: "age > 3 and age < 9"

DEFINITIONS:

	TERM -> An text item that is either contained in quotations (""), or is a single word. (e.g. ""search plugin"", or "searchforme")
	ANNOTATION NAME -> The plain-text title of an annotation (e.g. "comment", "hasAge")
	OPERATOR -> Any item from the OPERATOR chart down below. An operator defines what type of search you're doing on an annotation
	VALUE -> The string or word you're searching for in an annotation
	LOGICAL OPERATOR -> An item from the LOGICAL OPERATOR chart below. These separate triples to allow for complex searches

SYNTAX:

->	capitalization DOES NOT MATTER. (if you think this should change, please contact me via email at mark.helenurm@usd.edu)
->	items in QUOTATIONS ("") are treated as single terms. If you're searching for a comment containing a string, PUT IT IN QUOTES!
->	specific search "terms" are done in triples.
->	A triple is in the format: [ANNOTATIONNAME] [OPERATOR] [VALUE]
->	the ANNOTATIONNAME is the type of annotation (e.g. comment, label, age, etc.)
->	ANNOTATIONNAME and VALUE should NEVER be any of the LOGICAL or normal OPERATORS described below
->	if VALUE happens to be the same as a OPERATOR or LOGICAL OPERATOR, put it in quotes ("")
->	the OPERATORS and their appropriate VALUES are described below

ALL OPERATORS:

the OPERATOR column describes the type of operation
the USE NAMES column describes the keywords you can use to reference the operator
the INPUT column describes what values are appropriate to use with it

OPERATOR			USE NAMES					INPUT VALUE
----------------------------------------------------------------------------------------------------------
contains			contains, ~					String Literals
doesn't contain			doesntcontain, !~				String Literals
equals				equals, isequalto, =, ==			Numbers, String Literals
doesn't equal			doesntequal, !=					Numbers, String Literals
greater than			greaterthan, >					Numbers
less than			lessthan, <					Numbers
greater than or equal to	greaterthanorequalto, gequalto, gequal, >=	Numbers
less than or equal to		lessthanorequalto, lequalto, lequal, <=		Numbers
-----------------------------------------------------------------------------------------------------------

LOGICAL OPERATORS: (these separate specific triple-terms)

->	the ORDER OF OPERATIONS corresponds to the positions on the chart below. (e.g. terms in parentheses are evaluated before AND operations, which are evaluated before OR operations, etc.)

LOGICAL OPERATOR		USE NAMES
----------------------------------------------------------
parentheses			(, )
and				&, &&, and
exclusive or			^, xor, exclusiveor
or				|, ||, or
----------------------------------------------------------


CONTACT INFO:

Email:	Mark.Helenurm@usd.edu

Bugs, comments, or complaints? Feel free to email!
