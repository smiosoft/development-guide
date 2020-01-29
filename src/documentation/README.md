# Documentation

_A mostly reasonable approach to documentation._

1. [Basic Rules](#basic-rules)
1. [Formatting](#formatting)

## Basic Rules

### DOC_BR1: _Prefer to store and reference local assets_

When possible store static assets in the `.assets` folder; not only is it faster but there is no dependency on the external hosting.

DO:

```markdown
![Development Guide](./docs/.assets/project-title.png)
```

DON'T:

```markdown
![Development Guide](https://i.imgur.com/EpXBaDQ.jpg)
```

## Formatting

### DOC_FORM1: _Repository README_

```markdown
# {Repository Title}

[![{BADGE_TITLE}]({BADGE_LINK})]({URL})

_{SHORT_DESCRIPTION}_

![{TITLE}](./docs/.assets/project-title.png)

![{SCREENSHOT}](./docs/.assets/project-screenshot.png)
```

1. Repository Title
1. Badges
1. Short Description
1. Project Title Image
    - Prefer to use an asset exported from [assets/project-title](https://github.com/smiosoft/assets#templates).
1. Project Screenshot Image
   - Prefer to use an asset exported from [assets/project-screenshot](https://github.com/smiosoft/assets#templates).
1. Content (as relevant)
   - Examples include: Getting Started, Installation, Usage, Contribution...etc
