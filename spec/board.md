# board object
## tldr
A board object contains a bunch of lists of todos.

You can add a title and description using markdown syntax in `board.md`.

A picture can also be specified, by putting it in this object and calling it
`icon.[ext]`.

## fields
- title
- description
- icon
- lists
- ordering
- idea: label settings

### title
`board.md`:
Whatever follows the first singular hash that starts a line,
plus optional whitespace, up until an unescaped newline character.

Basically: The first markdown title in the `board.md` document.

### description
`board.md`:
All of the text below the first line that starts with one hash.

Basically: Everything that follows the first markdown title in the `board.md`
document.

### lists
A set of list objects.

Basically: This object stores lists in an ordered list.

### ordering
The lists are presumed to be in alphabetic order of the names of
the folders that represent them. If the names of all of the folders start with
digits, the ordering is presumed to be numeric. Conflict handling is
ambiguous.

Basically: Numeric or alphabetic ordering by folder name.

Altenatively: idea: Alternative ordering can be specified in `order.txt`. Each
line is to contain the name of one list object folder, and the order of the
lines determines the order of the lists.

### idea: label settings
`labels.csv`: The values in columns other than `label`. Labels in the column
called `label`.

Basically: A CSV table with one column called `label`, and any amount of
columns by any other names associating data with the label.

Example:
```csv
label;		color;	priority
important;	red;	2
weekly;		blue;	0
daily;		cyan;	1
```

## files
- board.md
- icon.[ext]
- idea: order.txt
- idea: labels.csv

### board.md
```
# [title]
[description]
```

### icon.[ext]
Image content.

By convention, this file is a PNG, so ext will also be `png`.

### idea: order.txt
```
[folder name] +
```

### idea: labels.csv
```csv
labels; 		[colname one]; 	[colname two]; 	[etc]
[label name];	[value one];	[value two]; 	[etc]
[etc] +
```

## objects
- `list` objects.
