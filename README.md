# abonicell.github.io

Personal academic website of Andrea Bonicelli. GitHub Pages turns the Markdown (`.md`)
files into web pages automatically every time you commit a change.

## Which file is which

| Page | File you edit |
|---|---|
| Home (bio, links, contact) | `index.md` |
| Experience & Education | `experience.md` |
| Publications | `publications.md` |
| Teaching & Mentoring | `teaching.md` |
| Grants & Funding | `grants.md` |
| Service & Outreach | `service.md` |
| Top menu, site title | `_config.yml` |
| Colours, fonts, spacing | `assets/style.css` |
| Page frame (menu + footer) | `_layouts/default.html` — you shouldn't need to touch this |

## How to edit a page

Open the `.md` file on GitHub, click the pencil icon, change the text, click **Commit changes**.
The site updates within 1–2 minutes.

Leave the block between the two `---` lines at the top of each file as it is.

### Adding an entry (job, grant, talk…)

Copy an existing entry and change it. Each entry is two lines — the date in `*stars*`, then
the details indented by two spaces:

```markdown
- *03/2025 – present*
  **Job title** — Institution, City, Country
```

The first `*italic*` text in an entry is shown as the small grey date line.

### Markdown cheat-sheet

| You type | You get |
|---|---|
| `**bold**` | **bold** |
| `*italic*` | *italic* |
| `[text](https://link)` | a link |
| `## Heading` | section heading (blue) |
| `### Heading` | sub-heading (small, grey) |
| `- item` | list entry |
| `1. item` | numbered list (good for publications) |

## Adding a new page

1. Create a new file, e.g. `projects.md`, starting with:

   ```markdown
   ---
   layout: default
   title: Projects
   permalink: /projects/
   ---

   # Projects
   ```

2. Add it to the menu in `_config.yml`:

   ```yaml
     - title: Projects
       url: /projects/
   ```

## Publishing (first time)

1. Create a public repository named exactly `abonicell.github.io`.
2. Upload all files and folders (keep `_layouts` and `assets` as folders).
3. Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
4. The site appears at https://abonicell.github.io. If a build fails, the **Actions** tab shows a red ✗ and the error.
