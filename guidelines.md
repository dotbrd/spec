# specification for general ideas that apply to every object
There's no specific guidelines for this, but try to be as unambiguous as
possible.

# object specification
The specification for an object should look as follows:

```
# [type] object
## tldr
[short, human-readable explanation of the object]

## fields
- [one piece of data stored in the object]
- [another]
- [etc]

### [name of the first item in the list]
[file it is stored in]: [how it is stored there]

Basically: [more human-readable description]

### [name of the second item in the list]
[file it is stored in]: [how it is stored there]

Basically: [more human-readable description]

### [etc]
[etc]

## files
- [one of the files contained in the object]
- [another]
- [etc]

### [name of the first item in the list]
[example content of the file, using some templating syntax]

### [name of the second item in the list]
[example content of the file, using some templating syntax]

### [etc]
[etc]

## objects
- [description of an object contained in the object]
- [another]
- [etc]

optional:
### [name of the first item in the list]
[more detailed description]

optional:
### [name of the second item in the list]
[more detailed description]

optional:
### [etc]
[etc]
```
