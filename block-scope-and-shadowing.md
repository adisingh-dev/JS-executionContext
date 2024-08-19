# what is a block in JS? 🤔
✅ A block in JS is the code written in a set of curlies {} aka compound statement. it is used in a place where JS expects a single statement. It wraps-up or groups multiple statements
so that they can be used in a place where JS expects a single statement like in if block or while/for loops

# what is a block scope? 🤨
✅ block scope means what all variables and fn we can access inside a block

# what happens when var const and let variables are initialized in a block?
✅ in this case var variables are attached in the global window object when GEC is created and let/const variables are attached to a separate space ie. reserved for that block and are
inaccessible outside it as they are block scoped

# how are these variables accessed outside the block?
✅ as let/const variables are block scoped they cannot be accessed outside the block but var variables cank be accessed outside it because their scope is limited only to a fn

# how Chrome DevTools Represent TDZ? 🧐
✅ Global Scope: TDZ is tied to the "Script" scope.
✅ Block Scope: TDZ is tied to the specific block scope and Chrome will show this under the block's execution context.
