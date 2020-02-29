# Repository

_A mostly reasonable approach to repositories._

1. [Basic Rules](#basic-rules)
1. [Naming](#naming)

## Basic Rules

### REPO_BR1: _Structure_

```txt
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
|
+---lib
+---samples
+---src
\---tests
```

- `build` - Any scripts related to building the solution, this is **NOT** an output folder
- `docs` - Any documentation related to the repository
  - `.assets` - Any repository scoped assets
- `lib` - Any dependencies that must be local, and cannot be installed from a hosted package manager
- `samples` - Any projects/files used to provide an example, or for demonstration purposes
- `src` - Any projects/files that make up the source code for the solution
- `tests` - Any projects/files related to testing the source code

### REPO_BR2: _Avoid committing commented out code_

Version control provides the ability to review past changes, there is no need to pollute the code base and its history.

## Naming

### REPO_NAME1: _Name repositories using lower kebab case_

An exception to this is a `GitHub User Pages` repository, which expects to be named `{username}.github.io`.

DO:

```txt
awesome-project
```

DON'T:

```txt
Awesome-Project
```

```txt
awesomeproject
```

```txt
AwesomeProject
```

```txt
Awesome.Project
```
