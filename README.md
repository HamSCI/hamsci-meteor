# HamSCI Meteor Scatter Working Group

The HamSCI Meteor Scatter Working Group coordinates amateur radio operators, citizen scientists, and professional researchers who use meteor scatter observations to advance meteor science and meteor scatter communications. Its main activity is the [Meteor Scatter QSO Party (MSQP)](https://hamsci.org/msqp).

## [Visit the working group website](https://hamsci.github.io/hamsci-meteor)

**Co-leaders:** Dr. Rob Suggs, NN4NT (NASA Marshall Space Flight Center Amateur Radio Club) and Dr. Jay Weitzen, AC1SN (University of Massachusetts Lowell)
**Mailing list:** HamSCI-Meteor@scranton.edu (being set up)
**Meetings:** weekly on Zoom; the link is sent to the mailing list

## What is in this repository

| Path | Contents |
|---|---|
| `docs/` | The website (Jekyll), published to GitHub Pages on every push to `main` |
| `src/` | Analysis scripts, and pointers to [HamSCI/meteor-scatter](https://github.com/HamSCI/meteor-scatter) and [HamSCI/MSQP](https://github.com/HamSCI/MSQP) |
| `hardware/` | Hardware designs, if the group produces any |
| `references/` | Source material for the website |
| `CLAUDE.md`, `.claude/`, `ai/` | AI governance scaffolding from [HamSCI/ai_project_template](https://github.com/HamSCI/ai_project_template) |

To change the website, edit the Markdown pages in `docs/`. Build it locally with `cd docs && bundle install && bundle exec jekyll serve`. Questions and suggestions are welcome as [issues](https://github.com/HamSCI/hamsci-meteor/issues/new).

This repository was created from the HamSCI working group template ([HamSCI/hamsci-wg](https://github.com/HamSCI/hamsci-wg)), which also explains how HamSCI working groups are organized.

# Remaining setup

- [ ] [Select a license](https://choosealicense.com/non-software/) and add a LICENSE.txt file. Record the same license in `CITATION.cff`.
- [ ] Decide the authors for `CITATION.cff` (co-leaders' call), or delete the file if the repository should not be citable.
- [ ] Under Settings > Pages, set this repository to deploy via GitHub Actions (it runs the `pages.yml` workflow already in the repository).
- [ ] Verify that the site is published at https://hamsci.github.io/hamsci-meteor.
- [ ] Confirm the mailing list address once it is live, and remove "being set up" from the site and this README.
- [ ] Confirm the institution and funder fields in `CLAUDE.md`, then trim the policy tiers in `.claude/rules/ai-governance.md` to match: delete Tier 2 if no institution governs the work, Tier 3 if the project is unfunded. Tier 1 stays.
- [ ] Prune the optional rule files: `rm .claude/rules/latex-writing.md` if there will be no LaTeX, `rm .claude/rules/python-code.md` if there will be no Python. Remove the matching lines from `CLAUDE.md`.
- [ ] Optionally, replace the favicons in `docs/assets/images/favicon/` with meteor-scatter ones (generate at https://favicon.io/).
- [ ] To archive the group's work, [synchronize this repository to Zenodo](https://help.zenodo.org/docs/github/enable-repository/), publish a release, and add the DOI badge here.
- [ ] Delete `ai/GETTING_STARTED.md` once the group is comfortable with the AI workflow.

# AI Use in This Working Group

Working group repositories are public, and their websites more so. The governance scaffolding in `.claude/` and `ai/` makes the following the default:

- **Never fabricate.** No invented citations, data, numbers, callsigns, or attributions.
- **Humans own the science.** A human reviews AI output before it enters an artifact, including website copy, and the scientific claims are the authors'.
- **AI is not an author.** Never in an author block, an acknowledgment, or a `CITATION.cff`.
- **Log before you commit.** Every substantive session, in `ai/ai_usage_log.md`, with a real timestamp. The `/commit` command in Claude Code does this for you.
- **Disclose AI use in published outputs**, naming the tool and describing what it did. The website's disclosure is on its About page.
- **Protect contributors.** Operator personal data, fine-grained station locations, unpublished collaborator data, and ITAR/EAR-controlled material never go to an external AI tool. See [`.claude/rules/hamsci-data.md`](.claude/rules/hamsci-data.md).

The full policy stack, including the tiers for institutional and funder requirements, is in [`.claude/rules/ai-governance.md`](.claude/rules/ai-governance.md).
