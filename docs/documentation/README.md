# Documentation

_A mostly reasonable approach to documentation._

## Table of Contents

1. [Basic Rules](#basic-rules)

## Basic Rules

### (DOC-BR1) Prefer to store and reference local assets

When possible store assets in the `.assets` folder; not only is it faster but there is no dependency on the external hosting.

_DO_

```markdown
![Development Guide](./docs/.assets/project-title.png)
```

_DON'T_

```markdown
![Development Guide](https://i.imgur.com/EpXBaDQ.jpg)
```
