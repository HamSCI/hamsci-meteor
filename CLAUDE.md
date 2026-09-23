# HamSCI Meteor Scatter Working Group

## Project Overview
The HamSCI Meteor Scatter Working Group coordinates amateur radio operators, citizen scientists,
and professional researchers who use meteor scatter observations to advance meteor science and
meteor scatter communications. Its main activity is the Meteor Scatter QSO Party (MSQP): during
target meteor showers, operators work MSK144 on 10 m and 6 m (some on 2 m) and upload WAV
recordings of their decodes to Zenodo for analysis. The audience is amateur operators taking part
in the MSQP, volunteers analyzing its data, and meteor and propagation researchers.

This repository holds the working group's public website and the group's shared work. It
combines two HamSCI scaffolds:

- the working group website template
  ([`HamSCI/hamsci-wg`](https://github.com/HamSCI/hamsci-wg)), which supplies `docs/`,
  `Gemfile`, and the GitHub Pages workflow, and
- the AI project template
  ([`HamSCI/ai_project_template`](https://github.com/HamSCI/ai_project_template)), which supplies
  this file, `.claude/`, and `ai/`.

**Co-leaders**: Dr. Rob Suggs, NN4NT (NASA Marshall Space Flight Center Amateur Radio Club) and
Dr. Jay Weitzen, AC1SN (University of Massachusetts Lowell)
**Collaborators**: MSQP participants and working group members; see the meeting minutes
**HamSCI Working Group**: Meteor Scatter Working Group (kickoff meeting 9 September 2026)
**Institution**: [to be confirmed; the University of Scranton hosts the mailing list]
**Funder**: [to be confirmed]
**Project period**: September 2026 onward
**Website**: https://hamsci.github.io/hamsci-meteor
**Mailing list / meetings**: HamSCI-Meteor@scranton.edu (being set up); weekly Zoom meeting,
link distributed on the mailing list

## Project Goal
Use meteor scatter observations, collected mainly through the MSQP, to test how meteor echo
power and duration depend on wavelength and meteor speed, to improve prediction of meteor scatter
communications, and to answer the operator's question of whether 10 m outperforms 6 m.

## Related repositories

| Repository | Contents |
|---|---|
| [`HamSCI/MSQP`](https://github.com/HamSCI/MSQP) | MSQP research questions, reading material (McKinley chapters, Weitzen and Ralston, Balis et al.), Zenodo upload guide |
| [`HamSCI/meteor-scatter`](https://github.com/HamSCI/meteor-scatter) | MSK144 ping recorder and decoder for ka9q-radio (SIGMOND client) |
| [HamSCI project 1](https://github.com/orgs/HamSCI/projects/1) | MSQP project board (human-curated; read only) |

## Standing Rules

These two are binding on every HamSCI project and are imported here so they load into context
automatically:

@.claude/rules/ai-governance.md
@.claude/rules/hamsci-data.md

Two further rule files are optional, and are scoped by their own `paths:` frontmatter to the
file types they govern:

- `.claude/rules/latex-writing.md` applies to `.tex`, `.bib`, `.cls`, and `.sty` files
- `.claude/rules/python-code.md` applies to `.py`, `pyproject.toml`, and `requirements*.txt`

Delete whichever the project does not use. To have one of them load unconditionally instead, add
an `@` import line for it above.

### Project-specific data rules

- **MSQP material names real stations.** Kickoff slides and participant spreadsheets carry
  callsigns, grid squares, and sometimes decimal-degree station coordinates. Publish callsigns
  and grid squares at 4 or 6 characters at most; never copy decimal coordinates onto the site.
- **Do not publish the Zoom link or passcode** on the website. HamSCI's own working group pages
  do not; the link goes out on the mailing list.
- **Do not name students** or describe their academic work on the site without their consent.
- `references/` holds source material (for example the kickoff slides). It is not published by
  the site build, but anything committed there is public on GitHub. Decide per file.

## Repository Structure

```
hamsci-meteor/
├── CLAUDE.md                     ← this file; project instructions for Claude
├── README.md                     ← working group description and setup checklist
├── CITATION.cff                  ← make the repository citable
├── Gemfile                       ← Jekyll dependencies
├── .gitignore
├── .claude/
│   ├── settings.json
│   ├── commands/commit.md        ← /commit workflow
│   └── rules/
│       ├── ai-governance.md      ← required
│       ├── hamsci-data.md        ← required
│       ├── latex-writing.md      ← delete if no LaTeX
│       └── python-code.md        ← delete if no Python
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/pages.yml       ← builds and deploys the website
├── ai/
│   ├── ai_usage_log.md           ← mandatory AI session log
│   └── GETTING_STARTED.md        ← delete once the project is running
├── docs/                         ← the public website (Jekyll source)
│   ├── _config.yml               ← site title, baseurl, and header_pages (nav order)
│   ├── index.md, 1_about.md, 2_mission.md, msqp.md, 3_goals.md,
│   │   4_minutes.md, 5_resources.md, 6_results.md
│   ├── _bibliography/            ← jekyll-scholar .bib files
│   ├── _includes/
│   └── assets/images/
├── hardware/                     ← board layouts, 3D printing files, editable sources
├── references/                   ← source material for the site (kickoff slides)
└── src/                          ← analysis scripts, or pointers to the software repos
```

## The Website

`docs/` is the source of a Jekyll site built with the `minima` theme and the `jekyll-scholar`
plugin, deployed to GitHub Pages by `.github/workflows/pages.yml` on every push to `main`.

**Everything committed under `docs/` is published on the public web.** Treat AI-drafted page copy
as published output: a human reviews it before it is committed, and the AI-use rules in
`.claude/rules/` apply to it in full. Roster and station pages need particular care, because
callsigns and grid squares identify real operators (`.claude/rules/hamsci-data.md`).

- Pages carry `layout`, `title`, and `permalink` front matter. The header nav order is set
  explicitly by `header_pages` in `docs/_config.yml`; add a new page there or it will not appear
  in the nav.
- Internal links use `{{ '/path/' | relative_url }}` so they resolve under the `baseurl`.
- Bibliographies live in `docs/_bibliography/` and are rendered by `jekyll-scholar`. Cite only
  work that has been verified against the actual source. MSQP station datasets are linked as a
  Zenodo community search rather than listed one by one, because each shower adds more.
- `docs/_config.yml` carries the site `title`, `description`, and `baseurl`. The `baseurl` must
  match the repository name for links to resolve.
- Build locally with `cd docs && bundle install && bundle exec jekyll serve`.
- Do not edit `_site/`; it is generated output and is gitignored.
- **Minutes**: add each meeting to the top of `docs/4_minutes.md`, and update action-item status
  there as items close.

## Working Conventions

**Session notes.** Keep one dated notes file per working session in `notes/`, named
`YYYY-MM-DD_<topic>.md`, recording what was decided, why, what it depends on, and what is still
open. Write them for a reader with no context, which in practice means a future Claude session
and a future you.

**Commits.** Use the `/commit` command. It logs the AI session, commits submodules first, then
commits the main repo. Prefix AI-assisted commits with `[AI-assisted]`. Reference tracking
issues (`refs #N`, or `closes #N` only when completion is yours to declare).

**Never push without explicit instruction.** Never force-push or hard-reset. Fetch and verify
remote state before any push. A push to `main` republishes the website.

**Project boards and issue status are human-curated.** Read them freely; propose changes and
name the exact command rather than running it.

## Submodules (optional)

If the project includes submodules (an Overleaf manuscript, a separate code repository, a
hardware design repo), the commit and push order is fixed:

1. Commit **inside** the submodule
2. Commit the updated submodule pointer in this repo
3. Push the submodule
4. Push this repo

Never the reverse at either stage. A parent pushed ahead of its submodule looks correct on the
machine that did it and breaks for every clone, because the recorded pointer names a commit no
remote has. Verify before pushing a parent:

```bash
git -C <submodule> branch -r --contains HEAD   # empty output = local only; push the submodule first
```

The `/commit` workflow auto-detects submodules via `git submodule status`.

## AI Governance

Every substantive AI session is logged in `ai/ai_usage_log.md` **before** the work is committed.
Use `/commit`, which enforces the ordering. The full policy stack is in
`.claude/rules/ai-governance.md`, which is imported above. Published outputs, including the
website, disclose AI use where AI produced or substantially shaped their content; the site's
disclosure is on the About page.
