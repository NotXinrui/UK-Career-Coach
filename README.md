<p align="center">
  <img src="assets/banner.svg" alt="UK Career Coach: audit your application, write it yourself" width="100%">
</p>

# UK Career Coach

<-- Use AI to beat the AI world! -->
An open skill for UK job applications. It evaluates a job description against your profile, maps keyword gaps, recommends which CV version to use, and proofreads. 

**Version** v0.1.0 · **Language** English (British) · **Works with** Claude, Gemini CLI

## What it does

| Give it | It returns |
|---|---|
| A job description (pasted or linked) | A five-part fit assessment, an ATS keyword gap list, and a salary check against current sources |
| A CV | Before and after suggestions, a recommended CV version, and consistency checks |
| A cover letter request | Three questions first, then a five-paragraph outline with prompts. Prose only if you ask |
| A CV or letter to proofread | Spelling, tense, passive voice, vague numbers and formatting issues, as before and after pairs |
| Counts by application stage | A plain reading of what the funnel shows, and what it cannot show |

## Principles

1. **AI audits; you author.** Facts, claims and final wording stay with you.
2. **Never invent.** No new achievements, tools, titles, numbers or dates. Gaps are reported, not filled.
3. **Blockers first.** Citizenship, clearance, seniority and pay mismatches are flagged before anything else.
4. **Your data stays yours.** The skill reads a profile you keep locally. Nothing personal ships in this repository.

## Repository layout

```
.
├── README.md
├── assets/                     banner and social preview image
├── docs/funnel.png             the author's application funnel (n = 1)
└── skills/uk-career-coach/
    ├── SKILL.md                rules and workflows the coach follows
    └── references/
        ├── profile-template.md         your facts; fill in locally, never publish
        ├── cv-tracks-template.md       defines your CV versions
        ├── cover-letter-structure.md   outline and prompts only
        └── keyword-library.md          starter keywords and ATS rules
```

## Install

Download `uk-career-coach-v0.1.0.zip` from the [latest release](../../releases/latest). The zip contains the skill folder only, which is what Claude.ai expects.

| Where | How |
|---|---|
| Claude.ai | Turn on code execution, then upload the zip in Settings under Skills (menu names change; see Anthropic's help centre) |
| Claude Code | Unzip into `~/.claude/skills/` (personal) or `.claude/skills/` (per project) |
| Gemini CLI | Unzip into `~/.gemini/skills/` or `.gemini/skills/` |
| Gemini app | No native skill support. Create a Gem and paste the contents of `SKILL.md` into its instructions |

Custom skills do not sync between products, so install them separately where you use them. Checked on 25 October 2026; these routes change, so confirm against the official documentation.

## Use it

1. Copy `references/profile-template.md`, fill it in, and **keep it local**. The `.gitignore` already excludes `profile.md` and `my-profile.md`.
2. Define two to four CV versions using `cv-tracks-template.md`.
3. Paste a job description and ask, for example: *"Assess this role against my profile and tell me which CV version to use."*

## Limitations

- **Market data goes stale.** The skill asks for current sources and dates; verify anything it cites.
- **Keyword banks are seeds.** Confirm them against real job descriptions before relying on them.
- **ATS behaviour varies by employer.** Optimising wording is not the same as presenting your experience accurately; the skill treats accuracy as the constraint.

## Privacy and responsibility

Do not commit your filled-in profile, CVs or employer-confidential material. This skill is not career, legal or immigration advice; check right-to-work and visa rules with official sources. It is an independent project and is not affiliated with or endorsed by Anthropic or Google.

## Feedback

If you use it, open an issue describing what worked and what did not, including failures. Real use is more informative than stars.

## Licence

See [LICENSE](LICENSE).
