# Repository

_A mostly reasonable approach to repositories._

1. [Basic Rules](#basic-rules)
1. [Naming](#naming)

## Basic Rules

### _Structure_

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

### _Protect `master` branch_

Ensure that commits are not made directly to the `master` branch, and undergo a code review process.

### _Prefer squash and merge_

When merging pull requests, prefer to squash and merge; this results in a cleaner commit log and efficient history navigation, whilst also taking away pressure from development branches.

This facilitates freedom to experiment, revert, cherry-pick, commit often with preferred messages, as well as increasing the confidence of non-developers or non-technical team members to contribute.

### _Avoid committing commented out code_

Version control provides the ability to review past changes, there is no need to pollute the code base and its history.

### _Avoid committing TODO comments_

These comments can easily become out-of-date; they are not an effective way of tracking and storing related discussions.

Use appropriate project management tools and services, there is no need to pollute the code base and its history.

## Naming

### _Name repositories using lower kebab case_

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
