dumb-refactorings.el
====================

some generic refactorings that aren&#39;t really that smart

Dependancies:
------------

- eproject
- popwin
- ido

Commentary:
----------

Some automated refactorings require a full AST tree of your entire project. Others can be
implemented in ways that are way more dumb, but still provide value.

bind the following functions to keys, or just call them via m-x

```
- dr/extract-variable   :: give the current region a name, create the variable right above it
                           and replace the region with the var name
- dr/inline-variable    :: take the current word the point is on, find what is on the other side
                           of the equals, delete the line, find the next instance of the variable,
                           and replace it with its definition
- dr/rename-in-project  :: do a regexp replace in multiple files for the given project
```
