# Repository

_A mostly reasonable approach to repositories._

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
|   \---.assets
|           project-title.png
|
+---lib
+---samples
+---src
\---tests
```

- `build` - Any scripts related to building the solution, this is **NOT** an output folder
- `docs` - Any documentation files
  - `.assets` - Any assets used in documentation
- `lib` - Any dependencies that must be local, and cannot be installed from an online package manager
- `samples` - Any projects used to provide an example, or for demonstration purposes
- `src` - Any projects related to the source code
- `tests` - Any projects related to testing