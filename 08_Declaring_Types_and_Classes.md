8. Declaring Types and classes
Type declarations
a new name for an existing type can be defined using a type declaration.
Type declarations can be used to make other types easier to read. For example, given
type Pos = (Int,Int)
*** NOTE: can't be recursive
Data declarations
A completely new type can be defined by specifying its values using a data declaration.
data Bool = False | True
Bool is a new type, with two new values False and True.
