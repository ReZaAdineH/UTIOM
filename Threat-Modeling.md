Threat-Modeling.md

# Threat Modeling in UTIOM

## Purpose
In the Unified Threat-Informed Operations Model (UTIOM), threat modeling is a core operational design activity. Its purpose is to translate threat intelligence, business context, and architectural realities into concrete, testable threat scenarios that directly inform visibility, detection, and response engineering.

Threat modeling in UTIOM is not performed as a one-time risk assessment. It is a continuous capability that evolves alongside the organization, its assets, and its adversaries.

---

## Inputs
Threat modeling in UTIOM is driven by the following inputs:

- Crown Jewels and business-critical assets
- System and identity architecture (on-prem, cloud, SaaS)
- Threat intelligence reports and adversary tradecraft
- Historical incidents and near-miss events
- Regulatory and operational constraints

---

## Method
UTIOM applies a scenario-driven threat modeling approach focused on attacker behavior and attack paths rather than abstract risks.

The process includes:

1. Identifying realistic adversaries and motivations
2. Mapping attacker goals to business impact
3. Decomposing attacks into attack trees and paths
4. Mapping attack steps to MITRE ATT&CK techniques
5. Identifying expected evidence at each step
6. Assessing current prevention, visibility, detection, and response coverage

This process produces **detection stories**, not isolated alerts.

---

## Attack Trees and Attack Paths
Attack trees are used to explore all realistic paths an adversary could take to reach a defined objective.

For each attack path, UTIOM explicitly documents:
- Preconditions and assumptions
- Required attacker capabilities
- Possible variations and bypass techniques
- Expected telemetry and observable signals
- Points of control, visibility, and detection

Attack trees are living artifacts and are revisited as architectures, controls, or threat intelligence change.

---

## Coverage Analysis
For each modeled attack path, UTIOM evaluates:

- Where the organization is protected
- Where visibility exists but detection is missing
- Where detection exists but response is unclear
- Where blind spots and gaps remain

This analysis directly feeds Threat Visibility Engineering and Threat Detection Engineering activities.

---

## Outputs
The outputs of threat modeling in UTIOM include:

- Prioritized threat scenarios
- Detection stories and investigation hypotheses
- Visibility and logging requirements
- Detection engineering backlogs
- Response playbook requirements
- Inputs to purple teaming and validation exercises

---

## Continuous Improvement
Threat modeling is continuously refined through:
- Incident post-mortems
- Purple team exercises
- Detection validation and tuning
- Changes in threat landscape
- Architectural evolution

Threat modeling is therefore both a design-time and run-time activity within UTIOM.

---

## Relationship to Other UTIOM Stages
Threat modeling acts as a bridge between:
- Crown Jewels and Threat Visibility Engineering
- Threat Intelligence and Detection Engineering
- Incident Response and Continuous Improvement

It ensures that security operations remain threat-informed, intentional, and aligned with real-world adversary behavior.


## Example Threat Scenario
(Identity compromise → cloud lateral movement → persistence)


## Relationship to TID-CMM

UTIOM leverages the Threat-Informed Detection Capability Maturity Model (TID-CMM) to assess and evolve the effectiveness of detection capabilities derived from threat modeling.

While UTIOM defines the operational lifecycle and design flow, TID-CMM provides a structured way to measure how well threat-informed detection is implemented across people, process, technology, and services.

Within the context of threat modeling:

- Threat scenarios and attack paths define **what should be detected**
- Detection stories define **how detection should work**
- TID-CMM evaluates **how mature and reliable those detections actually are**

TID-CMM enables organizations to move from ad-hoc or reactive detections toward engineered, validated, and continuously improved detection capabilities aligned with real adversary behavior.

Threat modeling outputs in UTIOM therefore act as direct inputs to TID-CMM assessment and improvement planning.


### Threat Modeling and Detection Maturity

As threat modeling evolves in UTIOM, detection maturity progresses accordingly:

- Low maturity: Threat modeling exists only as documentation or risk narratives
- Medium maturity: Threat scenarios are mapped to detection logic with partial validation
- High maturity: Threat scenarios are continuously validated through detection testing, purple teaming, and feedback loops

TID-CMM provides the structure to assess and guide this progression in a measurable and repeatable way.

