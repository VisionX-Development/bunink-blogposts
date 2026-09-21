# bunink-blogposts

The blog of **[bun.ink](https://bun.ink/?utm_source=github&utm_medium=blog_repo&utm_campaign=readme)** — a browser-based writing app that keeps your texts as Markdown in your own GitHub repository. Every post here is published at [bun.ink/blog](https://bun.ink/blog).

**Start reading:** [Contents](CONTENTS.md) · [Deutsch](de/) · [English](en/)

## Why this repository exists

The posts are written *in* bun.ink and saved straight to this repository — the same way the [handbook](https://github.com/VisionX-Development/writing-with-bunink) is. Drafts live on branches, the published text is whatever `main` says, and the commit history shows how each article got there.

The website does not read from here at runtime. A sync in bun.ink's (private) source repository pulls `main`, translates what changed, pushes the English versions back, and ships both languages with the next deploy.

## How it is organised

```
de/          the posts, in German — the source of truth
en/          the English translation — generated, never edited by hand
```

| File | What it tells you |
|---|---|
| [CONTENTS.md](CONTENTS.md) | Every post, newest first, with its files and its URL — generated |
| [DOCUMENTS.md](DOCUMENTS.md) | What a single post file looks like inside |
| [AGENTS.md](AGENTS.md) | The short version of all of the above, for AI agents |

German is the authoring language; English is generated from it. Further languages can be added as sibling directories.

## Contributing

Corrections are welcome — open an [issue](../../issues), or a pull request against the German source in `de/`. Please do not send changes to `en/`: it is generated, and the next sync would overwrite them.

For feature requests and bug reports about the app itself, use the [bun.ink roadmap repository](https://github.com/VisionX-Development/bunink-roadmap) instead. Security problems go to [info@bun.ink](mailto:info@bun.ink), never a public issue.

## Licence

The posts are published under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — use them, translate them, quote them, with attribution. See [LICENSE](LICENSE).
