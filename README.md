# davidcfrancis.github.io

Personal research website. Built with [Quarto](https://quarto.org) and rendered
by GitHub Actions on every push to `main`.

## Editing

Edit the `.qmd` files directly in the browser (press `.` on the repo page for a
full VS Code editor, or use the pencil icon on any file). Commit, wait ~2
minutes, and the Actions tab will show the rebuild.

| File | Contains |
|---|---|
| `index.qmd` | Landing page, bio, contact |
| `research.qmd` | Papers, grouped by stage |
| `code.qmd` | Replication packages and tools |
| `_quarto.yml` | Site title, nav bar, footer |
| `styles.scss` | Colors, type, paper-listing layout |

## Adding a paper

Copy an existing `.paper` block in `research.qmd` and edit it. The rail fields
are stage, year, and evidence base:

```
::: {.paper}
::: {.rail}
[Working paper]{.stage}
[2026]{.year}
[Firm panel · WBES]{.source}
:::
::: {}
### Title of the Paper
::: {.coauthors}
with Coauthor Name
:::
::: {.summary}
One or two sentences on the question and design.
:::
::: {.links}
[PDF](files/paper.pdf) · [Replication](https://github.com/davidcfrancis/repo)
:::
:::
:::
```

## Adding PDFs

Upload to `files/` and link as `files/name.pdf`. Keep paths stable once a link
has been cited anywhere.

## Adding a photo

Upload to `images/headshot.jpg`, then add this line at the top of `index.qmd`
below the front matter:

```
![](images/headshot.jpg){.headshot}
```

The `.headshot` class floats it right on desktop and stacks it on mobile.

## Custom domain

Add a `CNAME` file in the repo root containing the domain, then point an
ALIAS/A record at GitHub's Pages IPs from your registrar.

## Local preview (optional)

Requires Quarto installed. Not needed — GitHub renders on push.

```bash
quarto preview
```
