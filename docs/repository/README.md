# Repository

*A mostly reasonable approach to repositories.*

## Table of Contents

1. [Structure](#structure)

## Structure

```markdown
.
|   .gitattributes
|   .gitignore
|   LICENSE
|   README.md
|   {name}.sln
|
+---build
+---docs
|   \---assets
|           project-title.png
|
+---lib
+---samples
+---src
\---tests
```

- `build` - Any scripts related to building the project, this is **NOT** an output
- `docs` - Any documentation files and assets
- `lib` - Any dependencies that must be local, and cannot be instaleld from an online package manager
- `samples` - Any projects used to provide an example or demonstration
- `src` - Any projects related to the source code
- `tests` - Any projects related to testing
