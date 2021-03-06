# Board object
## Tldr
A board object contains a bunch of lists of todos.

You can add a title and description using markdown syntax in `board.md`.

A picture can also be specified, by putting it in this object and calling it
`icon.[ext]`.

The order of the lists in the board is determined by their folder name:
sorted numerically if possible, alphabetically otherwise.

idea: Alternatively, you can specify the order of the lists by putting their
folder names in a file called `order.txt`, in the order that you want.

idea: Data associated with labels can be put in a filed called `labels.csv`,
containing one `labels` column, and other columns with the linked values.

## Fields
- title
- description
- icon
- lists
- ordering
- idea: label settings

### Title
`board.md`:
Whatever follows the first singular hash that starts a line,
plus optional whitespace, up until an unescaped newline character.

Basically: The first markdown title in the `board.md` document.

### Description
`board.md`:
All of the text below the first line that starts with one hash.

Basically: Everything that follows the first markdown title in the `board.md`
document.

### Lists
A set of list objects.

Basically: This object stores lists in an ordered list.

### Ordering
The lists are presumed to be in alphabetic order of the names of
the folders that represent them. If the names of all of the folders start with
digits, the ordering is presumed to be numeric. Conflict handling is
ambiguous.

Basically: Numeric or alphabetic ordering by folder name.

Altenatively: idea: Alternative ordering can be specified in `order.txt`. Each
line is to contain the name of one list object folder, and the order of the
lines determines the order of the lists.

### Idea: label settings
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

## Files
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

### Idea: order.txt
```
[folder name] +
```

### Idea: labels.csv
```csv
labels;		[colname one]; 	[colname two]; 	[etc]
[label];	[value one];	[value two]; 	[etc]
[etc] +
```

## Objects
- `list` objects.
