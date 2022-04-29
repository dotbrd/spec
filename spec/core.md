# objects
The core primitive of the dotboard organisation system is the *object*.
Objects earned their name by virtue of there not being a better name that
I could come up with.

## structure
An object is any folder on a filesystem that adheres to the following
properties:

- Its name can be anything
- It can contain anything, but
- It **must** contain one file starting with a dot (`.`), followed by a
  sequence of lowercase characters representing the object's *type*

Example:

```
board
├── .board
├── list-one
├── list-two
└── media
```

The parent folder shown here is an object of type `board`. Incidentally, this
project derives its name from the unique identifier of this object:
`.board` -> `dotboard`

## information storage
An object stores information in a combination of the following:

- The contents of files
- The names of files
- Other objects within the object

This means that plain folders within objects are ignored by default.

## types
Every object has an associated type. Each type refers to a specification, which
dictates what information the object can and/or must store, and how. The basic
types that are required to make the core specification complete are:

- `board`
- `list`
- `todo`
- `data`

You can read more about them in the files that carry their name.

# conventions
- Objects should, generally, not require a particular name, so people using
  this system can name them anything and get the filesystem structure clear to
  themselves, and computer-generated dotboard projects do not need to worry
  about naming that much.
- `.type` files should generally not *require* having any content.
