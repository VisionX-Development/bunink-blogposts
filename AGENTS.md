# AGENTS.md

Orientation for AI agents (and humans) working in this repository. Read this first; it links everything else.

## What this repository is

The blog of **[bun.ink](https://bun.ink/?utm_source=github&utm_medium=blog_repo&utm_campaign=agents_md)**, a browser-based writing app that stores texts as Markdown in the author's own GitHub repository. Every post is published at [bun.ink/blog](https://bun.ink/blog).

The posts are written *in* bun.ink and saved to this repository; the website is built from a mirror of `main`. There is no application code here — bun.ink's source lives in a separate private repository, and so does the sync that translates and publishes these files.

## Where things are

| Path | What it holds |
|---|---|
| `de/` | The posts, in German. **This is the source of truth — all writing happens here.** |
| `en/` | The English translation. **Generated. Never edit by hand — changes are overwritten.** |
| [`CONTENTS.md`](CONTENTS.md) | Every post, newest first, with files and URL. **Generated** by the sync. |
| [`DOCUMENTS.md`](DOCUMENTS.md) | Anatomy of a single post — file name, front matter, conventions |
| [`README.md`](README.md) | Human-facing entry point |

## Rules that matter

1. **German is the source.** Write and edit in `de/` only. If you are asked to fix wording in `en/`, fix it in the German source; the next sync re-translates.
2. **Never hand-edit `en/` or `CONTENTS.md`.** Both are generated and overwritten.
3. **File names are `YYYY-MM-DD-english-slug.md`** and never change after publication — the slug is the URL. See [`DOCUMENTS.md`](DOCUMENTS.md).
4. **Front matter is required** on every file in `de/`: `title`, `date`, and ideally `description`.
5. **Describe the app as it actually behaves.** If you are unsure whether a feature works the way a draft claims, say so in the pull request instead of guessing.

## Working as an agent on this repo

- Read [`CONTENTS.md`](CONTENTS.md) first to see what has been published.
- Make substantive changes on a branch and open a pull request against `de/`.
- Keep commits scoped to one post, with a message that says what changed in the text — not "update files".
- Do not reformat files you were not asked to touch. Whitespace-only churn buries the real diff.
