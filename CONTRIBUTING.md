# Contributing to UTIOM

The UTIOM Framework is a practitioner framework. It gets better through practitioner review, disagreement, and field experience — not through polish. Contributions are welcome.

## What is most useful

In rough order of value:

1. **"This does not survive contact with reality."** Where the model breaks in a real SOC, with the constraint that broke it. This is the most valuable contribution there is.
2. **Worked examples** from environments not yet covered — OT, healthcare, public sector, MSSP, small teams without a dedicated SOC.
3. **Corrections** — factual errors, broken standards mappings, wrong metric formulas, outdated references.
4. **Clarity fixes** — a phase description that reads well to the author but not to a new reader.
5. **Assessment refinements** — criteria that are ambiguous, unscoreable, or that reward the wrong behaviour.

## What is out of scope

- Vendor or product recommendations. UTIOM stays vendor-neutral.
- Turning UTIOM into a compliance checklist. It operationalises standards; it does not replace or restate them.
- Renaming or restructuring the seven phases or three pillars without a strong operational argument. Stability of the model's vocabulary is a feature — people build on it.

## How to contribute

**For discussion, disagreement or a question:** open a [Discussion](https://github.com/ReZaAdineH/UTIOM/discussions) or an [Issue](https://github.com/ReZaAdineH/UTIOM/issues). You do not need a pull request to argue with the model. Please do argue with the model.

**For a concrete change:**

1. Fork the repository.
2. Create a branch: `git checkout -b your-change`.
3. Make the change. Keep it focused — one idea per pull request.
4. Commit with a clear message describing *why*, not just *what*.
5. Open a pull request explaining the operational reasoning behind the change.

## Style

- British or American English is fine; be consistent within a file.
- Plain language. If a sentence needs a second read, rewrite it.
- Keep the canonical vocabulary exact: *UTIOM Framework* in prose, *Unified Threat-Informed Operations Model* as the acronym expansion (hyphenated, never with "Framework" appended), the three pillars (Leadership and governance, Engineering and enablement, Operations and analysis), and the seven phases (Vision, Strategy, Crown Jewels, Threat Visibility, Threat Detection, Response, Continuous Improvement).
- Prefer text over images for anything a reader might need to search, copy or cite. Every diagram needs descriptive alt text.
- Claims about adversary behaviour, standards, or metrics should be traceable to a source.

## Licensing of contributions

By submitting a contribution you confirm that you have the right to submit it, and you agree it is licensed under the same terms as the part of the project it touches:

- **Documentation and framework content** — [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
- **Code and tooling** — [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)

Do not submit material you do not own, material under an incompatible licence, or anything confidential to your employer or a client. If you are contributing an example drawn from real work, anonymise it properly first — no organisation names, hostnames, IPs, or identifying detail.

## Recognition

Substantive contributors are credited in the release notes for the version their contribution ships in.

## Conduct

Be direct and be civil. Criticise the model as hard as you like; do not make it personal. Contributions that are abusive, or that use the project as a vehicle for vendor marketing, will be closed without discussion.
