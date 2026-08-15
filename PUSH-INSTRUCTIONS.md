# UTIOM repo — what to push and how

Everything in this folder is ready to drop into `github.com/ReZaAdineH/UTIOM`. Nothing here deletes or rewrites your existing content — the README keeps your structure, your sections and your wording, with additions rather than replacements.

## What's in this pack

| File | Status | Note |
| --- | --- | --- |
| `README.md` | **Replaces** `ReadME.md` | Your text preserved; added lifecycle, standards table, tools, licence section, citation |
| `LICENSING.md` | New | Explains the two-licence split and how to attribute |
| `TRADEMARK.md` | New | Naming policy — open content, governed name |
| `CONTRIBUTING.md` | New | Inbound licensing terms + what contributions are wanted |
| `CITATION.cff` | New | GitHub renders a "Cite this repository" button from this |
| `LICENSE` | **You generate** — step 3 | Must be official CC BY-SA 4.0 text |
| `LICENSE-CODE` | **You generate** — step 3 | Official Apache-2.0 text |

I deliberately did **not** write the two licence files myself. Legal text must be byte-exact from the source or it stops being that licence — step 3 pulls both from the official origin.

---

## Route A — command line (recommended)

Run these from your local clone of the repo.

### Step 1 — get the clone and back up

```bash
git clone https://github.com/ReZaAdineH/UTIOM.git
cd UTIOM
git checkout -b open-source-setup
```

Working on a branch means nothing on `main` changes until you're happy.

### Step 2 — rename ReadME.md to README.md

⚠️ **macOS gotcha:** the default Mac filesystem is case-insensitive, so `git mv ReadME.md README.md` will fail or silently do nothing. Use the two-step rename:

```bash
git mv ReadME.md readme-tmp.md
git mv readme-tmp.md README.md
```

Verify it took:

```bash
git status
```

You should see `renamed: ReadME.md -> README.md`. If it shows anything else, stop and check before continuing.

### Step 3 — fetch the official licence text

```bash
curl -L -o LICENSE https://creativecommons.org/licenses/by-sa/4.0/legalcode.txt
curl -L -o LICENSE-CODE https://www.apache.org/licenses/LICENSE-2.0.txt
```

Then **check both files actually contain full legal text**, not an HTML error page:

```bash
head -5 LICENSE
head -5 LICENSE-CODE
wc -l LICENSE LICENSE-CODE
```

`LICENSE` should be several hundred lines and start with "Creative Commons Attribution-ShareAlike 4.0 International". `LICENSE-CODE` should be ~200 lines and start with "Apache License / Version 2.0, January 2004". If either is short or looks like HTML, use the Route B fallback in step 3b below.

### Step 4 — copy in the new files

Copy `README.md`, `LICENSING.md`, `TRADEMARK.md`, `CONTRIBUTING.md` and `CITATION.cff` from this pack into the repo root, overwriting `README.md`.

### Step 5 — commit and push

```bash
git add -A
git commit -m "Establish explicit open-source licensing and project governance

- Split licensing: CC BY-SA 4.0 for framework content, Apache-2.0 for tooling
- Replace ambiguous LICENSE listing with official licence text
- Add LICENSING.md, TRADEMARK.md, CONTRIBUTING.md, CITATION.cff
- Rename ReadME.md to README.md and align to v1.1
- Standardise naming on UTIOM Framework"
git push -u origin open-source-setup
```

Then open the pull request GitHub offers you, review the diff, and merge into `main`.

If you'd rather skip the branch, replace steps 1 and 5 with a direct commit on `main` — but the branch costs you thirty seconds and lets you see the whole change as a diff first.

### Step 3b — fallback if curl didn't work

Use the GitHub web UI: **Add file → Create new file**, type `LICENSE` as the filename, and a **"Choose a license template"** button appears on the right. Pick *Creative Commons Attribution Share Alike 4.0 International*. GitHub inserts the official text.

For `LICENSE-CODE`, do the same trick with the filename `LICENSE`, choose *Apache License 2.0*, copy the inserted text, then rename the file to `LICENSE-CODE` before committing.

---

## Route B — entirely in the browser

If you'd rather not touch the command line:

1. Go to the repo, click `ReadME.md`, click the pencil icon, and change the filename field to `README.md`. Replace the body with this pack's `README.md`. Commit.
2. **Add file → Create new file** for each of `LICENSING.md`, `TRADEMARK.md`, `CONTRIBUTING.md`, `CITATION.cff` — paste the contents, commit each.
3. Open the existing `LICENSE` file, delete its contents, and paste the official CC BY-SA 4.0 text (get it via the template trick in step 3b). Commit.
4. Create `LICENSE-CODE` with the Apache-2.0 text.

---

## After the push — repo settings

These are as important as the files. All are in the repo's **About** panel (the gear icon top-right of the sidebar).

### 1. Fix the description

Your current one reads:

> Unified Threat Informed Operations framework model, is an operation threat informed model for unify Incident response across 3 main domain of Management, Engineering and Operations.

The canonical expansion is **Unified Threat-Informed Operations Model** — hyphenated, that exact word order, no "Framework" appended to it. Search engines and AI models reward exact repetition of an entity name; three different spellings across your properties dilutes it. Replace with:

> UTIOM Framework — the Unified Threat-Informed Operations Model. A lifecycle operating model unifying management intent, engineering discipline and operational execution across Security Operations and Incident Response.

**Two names, two jobs.** Use *UTIOM Framework* freely in prose, titles and headings — acronym plus category noun, the same shape as *MITRE ATT&CK Framework*. Keep *Unified Threat-Informed Operations Model* untouched as the acronym expansion. That expansion is the exact string Gemini reproduces in the first sentence of its answer; appending "Framework" to it would break the match and read as "Model Framework".

### 2. Set the website field

`https://utiom.de` — you already have this. Keep it.

### 3. Add missing topics

You have good ones. Add these, which are currently missing and are high-traffic:

`utiom` · `utiom-framework` · `soc` · `detection-engineering` · `security-operations` · `nist-csf` · `mitre-attack` · `dora` · `purple-team` · `blue-team` · `cybersecurity-framework`

`utiom` and `utiom-framework` matter most — they make the repo findable by the term itself.

### 4. Enable Discussions

**Settings → General → Features → Discussions.** Your CONTRIBUTING.md points people there, and it gives practitioners a place to argue with the model without opening an Issue.

---

## Version alignment

Your repo is on v1.0 while utiom.de is on v1.1. Right now someone finding you through GitHub gets the older framework, which makes "which version is canonical?" ambiguous.

**Add v1.1, don't remove v1.0.** Same reasoning as the SlideShare deck — existing URLs may already be cited somewhere.

1. Upload `UTIOM Framework Guide Book-v1.1.pdf` and `UTIOM assessment toolkit V1.1.zip` alongside the v1.0 files.
2. Consider moving the v1.0 files into an `archive/` folder in a *later* commit, with a note in the README.

## Cut a real Release

You have a tag but no release. Releases give you permanent, versioned download URLs and get indexed far better than loose repo files.

**Releases → Create a new release.** Tag `v1.1`, title "UTIOM v1.1 — August 2026", attach the PDF, XLSX and toolkit ZIP, and paste the v1.1 changelog from utiom.de as the body.

## Get a DOI (optional but high value)

Deposit the v1.1 PDF on [Zenodo](https://zenodo.org). It's free, it gives you a permanent DOI, and Zenodo can auto-archive every GitHub release. A DOI is the strongest possible signal that UTIOM is a real, citable, established thing rather than one person's website — which is exactly the corroboration gap we identified earlier.

Once you have the DOI, add it to `CITATION.cff` (there's an empty `orcid` field there too — worth getting an [ORCID iD](https://orcid.org), it's free and takes five minutes).

---

## Verify when you're done

- [ ] Repo sidebar shows a detected licence, not "View license"
- [ ] `README.md` renders (not `ReadME.md`)
- [ ] A "Cite this repository" button appears in the sidebar
- [ ] `LICENSE` contains full legal text, several hundred lines
- [ ] `LICENSE-CODE` contains the full Apache-2.0 text
- [ ] Description uses "UTIOM Framework" and the exact expansion "Unified Threat-Informed Operations Model"
- [ ] `utiom` and `utiom-framework` are in the topics list
- [ ] Discussions tab is visible
- [ ] Every link in the README resolves

---

## One decision I made for you

You didn't say which way you wanted to go on CC BY vs CC BY-SA, so I aligned everything to **CC BY-SA 4.0** — because that's what utiom.de and the v1.1 book already say. Consistency across your properties was the higher priority, and "keep the integrity" pointed the same way.

If you'd rather switch to plain **CC BY 4.0** for wider adoption — easier for vendors and consultancies to build on, at the cost of losing the copyleft protection against enclosure — it's a small change: swap the `LICENSE` file, and update the three references in `README.md`, `LICENSING.md` and `CITATION.cff`. Tell me and I'll regenerate the pack. Just change utiom.de at the same time, so the two never disagree.
