# UTIOM Framework — Unified Threat-Informed Operations Model

**UTIOM (Unified Threat-Informed Operations Model) is a practitioner framework for designing and operating modern Security Operations and Incident Response as a unified, threat-informed system.**

The UTIOM Framework connects strategy, threat modeling, detection engineering, response execution, and continuous improvement into one lifecycle.

It is built on management principles, engineering discipline, and operational execution, and is intended to help organizations move beyond tool-driven, alert-centric security operations.

> **Incident Response is not a phase. It is the operating mode of Security Operations.**

Threat intelligence, hunting, detection engineering, monitoring and containment are not separate functions. They are expressions of incident response at different distances from impact. UTIOM unifies them into one continuous lifecycle instead of fragmented workflows and teams.

**Current release:** v1.1 (August 2026) · **Website:** [utiom.de](https://utiom.de) · **Licence:** CC BY-SA 4.0 (framework) / Apache-2.0 (tools)

---

## The lifecycle

Seven phases across three pillars. Each phase consumes and produces knowledge, and the output of one becomes the input to the next.

**Vision → Strategy → Crown Jewels → Threat Visibility → Threat Detection → Response → Continuous Improvement**

### Leadership and governance

- **Vision** — Why the SOC exists and how success is measured
- **Strategy** — Threat profiling, risk prioritisation, capability roadmap
- **Crown Jewels** — Critical asset mapping, threat modelling, attack paths

### Engineering and enablement

- **Threat Visibility** — Telemetry engineered outward from crown jewels
- **Threat Detection** — Detection-as-code, versioned, tested, traceable

### Operations and analysis

- **Response** — Pre-engineered playbooks, tiered containment, automation
- **Continuous Improvement** — Kaizen loops feeding back into the whole lifecycle

---

## What the UTIOM Framework is

- A threat-informed operating model for Security Operations and Incident Response
- A way to translate governance and strategy into day-to-day SOC and IR execution
- An engineering-driven approach to visibility, detection, and response
- A continuous improvement system treating security operations as a living product
- A set of free, self-hosted assessment tools

## What the UTIOM Framework is not

- Not a compliance framework
- Not a vendor model
- Not a replacement for standards such as NIST, ISO, or SANS guidance

---

## Standards alignment

The UTIOM Framework does not replace established standards. It operationalises them.

| Standard | Relationship |
| --- | --- |
| **NIST CSF 2.0** | CSF defines what good looks like; UTIOM defines the operating model that delivers it. Vision and Strategy map to Govern, Crown Jewels to Identify, the engineering phases to Detect and Respond. |
| **SOC-CMM** | SOC-CMM measures how mature a SOC is; UTIOM provides the mechanism to become mature. |
| **DORA** | DORA mandates operational resilience; UTIOM operationalises it through crown-jewel-driven risk management, tiered response and structured incident classification. |
| **MITRE ATT&CK / DeTT&CT** | ATT&CK describes adversary behaviour and DeTT&CT measures coverage; UTIOM anchors both to crown jewels so coverage is prioritised by business consequence rather than technique count. |
| **TID-CMM** | The Threat-Informed Detection Capability Maturity Model measures the engineering pillar specifically. Developed alongside UTIOM. Publishing separately. |
| **ISO 27001, TOGAF, COBIT** | Governance, architecture vision and control objectives feed the Vision and Strategy phases. |

---

## Repository contents

- Core documentation describing the UTIOM lifecycle and principles
- Practitioner-oriented explanations of threat modeling, detection engineering, and incident response
- A self-assessment and maturity model aligned with the framework
- Practical examples and scenarios
- The free edition of the UTIOM framework book

| File | Description |
| --- | --- |
| `UTIOM-Overview.md` | Entry point — what the model is and why |
| `UTIOM-Lifecycle.md` | The seven phases in detail |
| `Threat-Modeling.md` | Crown jewels, attack paths, threat profiling |
| `Detection-Engineering.md` | Detection-as-code practice |
| `Incident-Response.md` | Structured response and containment |
| `Continuous-Improvement.md` | Kaizen loops and feedback |
| `Assessment-UTIOM-Maturity-Model.md` | Staged maturity model |
| `SOC-Operating-Example.md` | Worked operating example |
| `Cloud-Identity-Threat-Scenario.md` | Applied cloud/identity scenario |

## Assessment tools

Four browser-based instruments. No backend, no database, no analytics, no signup — answers stay in your browser.

| Tool | Scope | Question it answers |
| --- | --- | --- |
| [Maturity assessment](https://utiom.de/maturity.html) | 45 criteria, staged across 6 levels | Where are we, honestly? |
| [Capability assessment](https://utiom.de/capability.html) | 93 indicators, 10 domains | What should we fix first? |
| [Metrics calculator](https://utiom.de/metrics.html) | 67 metrics, leading + lagging | Did the fix work? |
| [Improvement roadmap](https://utiom.de/roadmap.html) | Combines all three | So what do we actually do about it? |

The complete toolkit ships as static HTML with a Dockerfile, so it can run entirely inside your own network.

## Downloads

- [UTIOM Framework Book v1.1 (PDF)](https://utiom.de/utiom-framework-v1.1.pdf)
- [Assessment workbook (XLSX)](https://utiom.de/utiom-assessment-workbook.xlsx)
- [Complete toolkit (ZIP)](https://utiom.de/utiom-assessment-toolkit.zip)

Versioned copies are also attached to each [GitHub Release](https://github.com/ReZaAdineH/UTIOM/releases).

---

## How to use this repository

1. Read `UTIOM-Overview.md` and `UTIOM-Lifecycle.md` to understand the model.
2. Use the assessment materials, or the online tools, to evaluate current operational maturity.
3. Adapt the model to your organisation's context and constraints.
4. Provide feedback or suggestions through Issues or Discussions.

---

## Licence

The UTIOM Framework is fully open. Two licences apply, because documentation and software need different terms:

- **Framework content** — all `.md` files, the framework book, diagrams and assessment criteria — is licensed under **[Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/)**. See [`LICENSE`](LICENSE).
- **Software** — the assessment tools, scripts and Dockerfile — is licensed under the **[Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)**. See [`LICENSE-CODE`](LICENSE-CODE).

Full detail, including how to attribute, is in [`LICENSING.md`](LICENSING.md).

The names **"UTIOM"**, **"UTIOM Framework"** and **"Unified Threat-Informed Operations Model"** identify the canonical framework published at [utiom.de](https://utiom.de). See [`TRADEMARK.md`](TRADEMARK.md) for the naming policy that applies to forks and derivative works.

## Contributing

Practitioner review, critique and discussion are welcome. See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Citation

```
Adineh, R. (2026). UTIOM Framework — Unified Threat-Informed Operations Model
(Version 1.1). Licensed CC BY-SA 4.0. https://utiom.de
```

Machine-readable metadata is in [`CITATION.cff`](CITATION.cff).

## Author

**Reza Adineh** — Germany-based cybersecurity architect with over fifteen years designing and leading security operations centres across banking, cloud and hybrid environments. Also the creator of the STRATA and TID-CMM frameworks, and the Realistic SIEM Maturity Model.

[LinkedIn](https://www.linkedin.com/in/rezaadineh/) · [utiom.de](https://utiom.de)
