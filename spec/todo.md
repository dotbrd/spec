# todo object
## tldr
A todo object contains a file called `todo.md`, where you can write a title
and description for the todo using markdown syntax.

You can also add any amount of sublists by including `list` objects containing
`todo` objects. Alternatively, you can include one markdown checklist at the
end of the `todo.md` file, for simple use.

Attachments (files) are stored in no more than one `data` object,
conventionally called `attachments`.

idea: Labels can be represented by putting the labels, each on different lines,
in a file called `labels.txt`.

idea: Deadlines can be represented by putting the datetimes
(`datetime`), each on different lines, in a file called `when.txt`.
Alternatively, you can put the deadline right below the title in `todo.md`,
followed by a newline.

idea: Assignees can be represented by putting the assignees
(`[name] <[email]>`), each on different lines, in a file called `who.txt`.

## fields
- title
- description
- internal todos
- attachments
- idea: labels
- idea: deadlines
- idea: assignees

### title
`todo.md`:
Whatever follows the first singular hash that starts a line,
plus optional whitespace, up until an unescaped newline character.

Basically: The first markdown title in the `todo.md` document.

### description
`todo.md`:
All of the text below the first line that starts with one hash.

Basically: Everything that follows the first markdown title in the `todo.md`
document.

As much as possible, when the description references other files, they should
be within the `attachments` directory.

### internal todos
Any object of type `list` that contains one or more objects of type `todo`.

Basically: Every list of todos within a todo is considered an sub-todo list.

Alternatively: For very simple todos, include a markdown checklist at the end
of `todo.md`.

### attachments
Zero or one objects of type `data` that contain one or more files.

Basically: A non-empty data directory.

### idea: labels
`labels.txt`: Every line.

Basically: Every line contains one label that is associated with this to-do.

### idea: deadlines
`when.txt`: `[datetime]` on every line.

Basically: Every line contains one datetime.

Alternatively: A single deadline can be included in the todo.md file, by
putting the line `[deadline]` right after the title, followed by a newline or
EOF.

### idea: assignees
`who.txt`: `[name] <[email]>` on every line.

Basically: Every line contains one name and one email address.

## files
- todo.md
- idea: labels.txt
- idea: who.txt
- idea: when.txt

### todo.md
```
# [title]
[description]
```

### idea: labels.txt
```
[label] +
```

### idea: who.txt
```
[name] <[email]> +
```

### idea: when.txt
```
[label]: [datetime] | [datetime] +
```

## objects
- `list` objects containing `todo` objects.
