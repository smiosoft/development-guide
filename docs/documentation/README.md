# Documentation

_A mostly reasonable approach to documentation._

## Table of Contents

1. [Basic Rules](#basic-rules)
1. [Order](#order)

## Basic Rules

### (DOC-BR1) Prefer to store and reference local assets

When possible store static assets in the `.assets` folder; not only is it faster but there is no dependency on the external hosting.

_DO_

```markdown
![Development Guide](./docs/.assets/project-title.png)
```

_DON'T_

```markdown
![Development Guide](https://i.imgur.com/EpXBaDQ.jpg)
```

## Order

### (DOC-OR1) Repository README

1. Title
   - Prefer to use an asset exported from [assets/project-title](https://github.com/smiosoft/assets#project-title).
1. Badges
1. Separator
1. Short Description
1. Getting Started

```markdown
![{TITLE}](./docs/.assets/project-title.png)
[![{BADGE_TITLE}]({BADGE_LINK})]({URL})

---

_{SHORT_DESCRIPTION}_

## Getting Started
```
