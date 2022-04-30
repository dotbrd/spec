# Spec
Specification for an open, filesystem-based standard for kanban-style project
management. Why?

- Filesystems are universal
- Potential for multiple backends
- Futureproof
- Human centered
- Simple
- ... (the list goes on)

You can find the specification in the `spec` folder.

# Usage
As this specification is filesystem based, you can use it from a file manager,
terminal, whatever. However, it is also meant to be machine-readable:
applications will be built to implement this specification and visualize the
organisational structure in gantt charts, kanban boards, calendars etc.
These applications will also be able to leverage the power of the filesystem
backend

- Git, for history and sharing with others
- Network shares, for real-time collaboration
- Regular, local filesystem for personal organisation? Why not!

# Get started
Check out `spec/intro.md` to get started with the specification.
