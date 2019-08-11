# Repository

_A mostly reasonable approach to repositories._

## Table of Contents

- [Structure](#structure)
- [Basic Rules](#basic-rules)
- [Version Control](#version-control)

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

## Basic Rules

### REPO_BR1: _Name repositories using lower-case and kebab-case_

An exception to this is a `GitHub User Pages` repository, which expects to be named `{username}.github.io`.

#### DO

```
awesome-project
```

#### DON'T

```
Awesome-Project
```

```
awesomeproject
```

```
AwesomeProject
```

```
Awesome.Project
```

## Version Control

### REPO_VC1: _Prefer Git_

### REPO_VC2: _Protect `master` branch_