# list object
## tldr
A list object contains a file called `list.md`, where you can write a title
and description for the list using markdown syntax.

You can add any amount of todos to the list by including todo objects.

The names of the folders of these todo objects determine the ordering: numeric
if possible, alphabetic otherwise.

idea: Labels of this list can be represented by putting the labels, each on
different lines, in a file called `labels.txt`.

## fields
- title
- description
- todos
- ordering
- idea: labels

### title
`list.md`:
Whatever follows the first singular hash that starts a line,
plus optional whitespace, up until an unescaped newline character.

Basically: The first markdown title in the `list.md` document.

### description
`list.md`:
All of the text below the first line that starts with one hash.

Basically: Everything that follows the first markdown title in the `list.md`
document.

### todos
A set of todo objects.

Basically: This object stores todos in an ordered list - like a kanban column.

### ordering
The todos are presumed to be in alphabetic order of the names of
the folders that represent them. If the names of all of the folders start with
digits, the ordering is presumed to be numeric. Conflict handling is
ambiguous.

Basically: Numeric or alphabetic ordering by folder name.

Altenatively: idea: Alternative ordering can be specified in `order.txt`. Each
line is to contain the name of one todo object folder, and the order of the
line determines the order of the todos.

### idea: labels
`labels.txt`: Every line.

Basically: Every line contains one label that is associated with this to-do.

## files
- list.md
- idea: order.txt
- idea: labels.txt
- objects

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

## objects
- `todo` objects.
