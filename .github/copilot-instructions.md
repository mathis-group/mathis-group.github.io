# Copilot Instructions for mathis-group.github.io

## Project Overview
This is a static website for the Mathis Group at ASU, built using Jekyll and the [Lab Website Template](https://greene-lab.gitbook.io/lab-website-template-docs). The site is primarily managed with Markdown, YAML, HTML (Liquid), and SCSS files.

## Key Structure
- **Content:**
  - `index.md`, `_members/`, `_posts/`, `blog/`, `projects/`, `research/`, `team/` — Main site content in Markdown.
  - `_data/` — YAML files for structured data (citations, members, projects, etc.).
  - `_includes/`, `_layouts/` — HTML/Liquid templates for site rendering.
  - `_styles/` — SCSS for custom site styling.
- **Custom Code:**
  - `_plugins/` — Custom Ruby plugins for Jekyll (e.g., `array.rb`, `file.rb`).
  - `_cite/` — Python scripts for citation management (`cite.py`, `util.py`).

## Developer Workflows
- **Local Build:**
  - Use `./.docker/run.sh` to build locally (requires Docker). Adjust line endings if you encounter issues.
- **Content Editing:**
  - Add or update Markdown files in `_members/`, `_posts/`, etc. for new content.
  - Update YAML files in `_data/` for structured data changes.
- **Custom Plugins:**
  - Ruby plugins in `_plugins/` extend Jekyll functionality. Review these for custom site logic.
- **Citation Management:**
  - Python scripts in `_cite/` manage citations. Dependencies are listed in `_cite/requirements.txt`.

## Conventions & Patterns
- **YAML Front Matter:** All content Markdown files use YAML front matter for metadata.
- **Data-Driven Content:** Many site sections (members, projects, citations) are generated from YAML in `_data/`.
- **SCSS Organization:** Custom styles are modularized in `_styles/` and imported via `all.scss`.
- **No JavaScript Build Step:** JS in `_scripts/` is used as-is; there is no bundler or transpiler.

## Integration Points
- **Jekyll:** Site is built and served by Jekyll (via Docker for local dev).
- **Lab Website Template:** Provides base layouts and structure; customizations are layered on top.
- **Python Citation Tools:** Used for managing and updating citation data.

## Examples
- To add a new member: create a Markdown file in `_members/` with appropriate front matter.
- To update citations: edit `_data/citations.yaml` and/or use `_cite/cite.py`.
- To add a new custom layout: create an HTML file in `_layouts/` and reference it in content front matter.

## References
- See `README.md` for build instructions.
- Review `_plugins/` and `_cite/` for custom logic.
- Consult the [Lab Website Template docs](https://greene-lab.gitbook.io/lab-website-template-docs) for base system details.
