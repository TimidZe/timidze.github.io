# timidze.github.io

Personal academic homepage, built with Jekyll and hosted on GitHub Pages at
<https://timidze.github.io>.

Single-page layout (centred column) with four sections — About Me, Research
Projects, Publications, Awards — plus one detail page per research project.

## Where to edit what

| What you want to change | File |
| --- | --- |
| Name, photo, affiliation lines, email, header links | `_config.yml` (`author:` block) |
| "About Me" text and section order | `index.md` |
| A research project (title, thumbnail, detail page text) | `_projects/*.md` |
| Publication list | `_data/publications.yml` |
| Awards list | `_data/awards.yml` |
| Fonts, colours, spacing, column width | `assets/css/style.css` |

Images go in `images/` (project figures in `images/projects/`), files such as a
CV PDF go in `files/`.

### Adding a research project

Create a new file in `_projects/`, e.g. `_projects/my-project.md`:

```markdown
---
title: "Project title"
subtitle: "One line shown next to the thumbnail on the home page"
order: 4                      # controls position in the list
image: /images/projects/my-project.png
caption: "Figure caption."
links:
  - name: "Paper"
    url: "https://..."
---

A few paragraphs describing the project. This is the detail page that the
thumbnail and the title on the home page link to.
```

## Local preview

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>.
