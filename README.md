# adgie.AI Skills

Free agent skills for curriculum work. Browse them here; download them from
[adgie.ai/skills-free](https://adgie.ai/skills-free).

## Layout

One package per directory, grouped by the agent it targets:

```
claude/<skill-name>/SKILL.md     required, and its frontmatter `name` must
                                 match the directory
claude/<skill-name>/...          references/, scripts/, assets/ as needed
```

## Publishing

This repository is the source of truth. Pushing to `main` runs
[`.github/workflows/publish-skills.yml`](.github/workflows/publish-skills.yml),
which zips every package, uploads it to Cloud Storage, and rebuilds the
catalogue at `skills/index.json`. Deleting a directory here removes the skill
from the catalogue on the next push.
