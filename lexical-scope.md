# what is scope in JS?
scope in JS means the space within which we can access a variable or a function. scope of a variable means where can we access the variable. Scope is directly depended on the lexical environment

# what is lexical scope?
lexical means in-order or in heirarchy. Now scope in JS is directly related to lexcal environment. Whenever an EC is created a lexical environment is also created
Lexical = local memory + reference to the lexical env of the parent, inside the memory component. A fn can be lexically inside its parent

# how does lexical environment work?
whenever an EC is created a lexical env is also created inside the memory component of EC. It contains the reference of its parent ie. the lexical env of current scope points to the lexical
env of its parent. The parent's memory component in turn also points to the lexical env of its own parent

# what does the lexical env of global EC contain?
'null' because the lexical env of global space has no parent to point to

# what is scope chain?
Definition: The linking of lexical environments when JS engine cannot find the variable or a fn inside its own lexical environment
Explanation: It is a chain of lexical env and parent references and it defines whether a variable or fn is present inside the scope or not. It is a mechanism of searching variables and fn
inside the parent's lexical scope in case JS could not find it in current local memory space. In this case JS engine moves to the lexical env of its parent. Eventually jumping to the global 
scope and if still not finds it in global scope then throws an error "variable not defined" because global EC lexical scope points to null and the chain terminates which means that the entity
is not present in the scope chain
