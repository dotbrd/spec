# List object
## Tldr
A list object contains a file called `list.md`, where you can write a title
and description for the list using markdown syntax.

You can add any amount of todos to the list by including todo objects.

The names of the folders of these todo objects determine the ordering: numeric
if possible, alphabetic otherwise.

idea: An alternative ordering can be specified by putting the names of todo
object folders in a file called `order.txt`, in the order that you want.

idea: Labels of this list can be represented by putting the labels, each on
different lines, in a file called `labels.txt`.

## Fields
- title
- description
- todos
- ordering
- idea: labels

### Title
`list.md`:
Whatever follows the first singular hash that starts a line,
plus optional whitespace, up until an unescaped newline character.

Basically: The first markdown title in the `list.md` document.

### Description
`list.md`:
All of the text below the first line that starts with one hash.

Basically: Everything that follows the first markdown title in the `list.md`
document.

### Todos
A set of todo objects.

Basically: This object stores todos in an ordered list - like a kanban column.

### Ordering
The todos are presumed to be in alphabetic order of the names of
the folders that represent them. If the names of all of the folders start with
digits, the ordering is presumed to be numeric. Conflict handling is
ambiguous.

Basically: Numeric or alphabetic ordering by folder name.

Altenatively: idea: Alternative ordering can be specified in `order.txt`. Each
line is to contain the name of one todo object folder, and the order of the
lines determines the order of the todos.

### Idea: labels
`labels.txt`: Every line.

Basically: Every line contains one label that is associated with this to-do.

## Files
- list.md
- idea: order.txt
- idea: labels.txt

### list.md
```
# [title]
[description]
```

### idea: order.txt
```
[folder name] +
```

### idea: labels.txt
```
[label] +
```

## Objects
- `todo` objects.
