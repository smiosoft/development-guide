# Repository

_A mostly reasonable approach to repositories._

- [Visual Studio Solution](./visual-studio-solution)

## Table of Contents

- [Basic Rules](#basic-rules)
- [Structure](#structure)

## Basic Rules

### REPO-BR1: _Name repositories using lower-case and kebab-case_

#### DO

```
awesome-project
```

#### DON'T

```
Awesome-Project
```

```
AwesomeProject
```

```
Awesome.Project
```

An exception to this is a `GitHub User Pages` repository, which expect `{username}.github.io`.

## Structure

```
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
- `docs` - Any documentation files
  - `.assets` - Any assets used in documentation
- `lib` - Any dependencies that must be local, and cannot be installed from an online package manager
- `samples` - Any projects used to provide an example, or for demonstration purposes
- `src` - Any projects related to the source code
- `tests` - Any projects related to testing
