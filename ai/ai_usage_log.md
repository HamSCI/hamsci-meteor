# AI Usage Log: HamSCI Meteor Scatter Working Group

This log records every substantive AI-assisted session on the project "HamSCI Meteor Scatter Working Group".

Required by the HamSCI Generative AI Use Agreement, and by any institutional or funder policy
that applies to this project (see `.claude/rules/ai-governance.md`).

**This log is the source of truth for what AI did on this project.** A disclosure paragraph in a
manuscript, poster, website page, or software release summarizes this log truthfully. Keep it
current: an entry written from memory weeks later is not a record.

## Entry format

```
## [YYYY-MM-DD HH:MM TZ]
- **Tool**: Claude (Anthropic), <exact-model-id>
- **Session Purpose**: What the session set out to accomplish
- **Sections/Files Affected**: Specific files, sections, or documents touched
- **Nature of Contribution**: Draft / Edit / Analysis / Code generation / Research / Scaffolding
- **Human Review Status**: Reviewed and verified / Partially reviewed / Pending review
- **Git Hash**: <filled in after committing>
```

The date and time come from the system clock via `date`, never from an estimate. The `/commit`
command produces this format and appends it in the right order.

---

<!-- Append new entries below this line, newest at the bottom. -->


## [2026-09-23 14:51 UTC]
- **Tool**: Claude (Anthropic), claude-opus-5-5[1m]
- **Session Purpose**: Build out the working group website from the kickoff meeting slides
  (`references/Meteor_Scatter_Working_Group_Kickoff_Sept2026_RevA.pdf`, 9 September 2026), and
  merge in the `HamSCI/ai_project_template` governance scaffolding, following the precedent of
  `HamSCI/hamsci-raytracing` commit 8059027.
- **Sections/Files Affected**: `docs/_config.yml` (title, description, baseurl, header_pages),
  `docs/index.md`, `docs/1_about.md`, `docs/2_mission.md`, `docs/msqp.md` (new),
  `docs/3_goals.md`, `docs/4_minutes.md`, `docs/5_resources.md`, `docs/6_results.md`,
  `docs/_bibliography/{publications,datasets}.bib` (WWV/H template entries removed),
  `docs/assets/images/msqp_underdense_pings_nn4sa.png` (new, extracted from slide 10),
  `src/README.md`, `README.md`, `CITATION.cff`, `CLAUDE.md` (new), `.gitignore` (new),
  `.claude/` (new, copied unchanged from the AI project template), `ai/ai_usage_log.md` (new),
  `ai/GETTING_STARTED.md` (new, copied from hamsci-raytracing)
- **Nature of Contribution**: Draft (website copy from the kickoff slides, hamsci.org/msqp, and
  the HamSCI/MSQP repository); scaffolding. Callsigns checked against the FCC database via
  callook.info; citations checked against the papers' first pages; all external links checked to
  resolve. Station coordinates, personal email addresses, the Zoom link, and a student's name in
  the slides were deliberately left off the public site.
- **Human Review Status**: Pending review by the co-leaders and N. A. Frissell (W2NAF)
- **Git Hash**: c371b3c
