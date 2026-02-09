Detection-Engineering.md

# Detection Engineering in UTIOM

## Purpose
In the Unified Threat-Informed Operations Model (UTIOM), detection engineering is treated as a disciplined engineering practice rather than an alert configuration activity. Its purpose is to design, build, validate, and maintain reliable detection capabilities that reflect real adversary behavior and support effective incident response.

Detection engineering in UTIOM is driven by threat models, not by tool defaults or isolated indicators.

---

## Detection Engineering vs Detection Operations
UTIOM explicitly distinguishes between:

- **Detection Engineering**: The design, development, testing, and validation of detection capabilities
- **Detection Operations**: The day-to-day monitoring, investigation, and handling of detection outputs

This separation ensures that detection quality is addressed as an engineering concern, while operational execution remains focused on decision-making and response.

---

## Inputs to Detection Engineering
Detection engineering in UTIOM is informed by:

- Threat models and attack paths
- Crown jewel definitions and business impact
- Threat intelligence and adversary tradecraft
- Visibility and telemetry capabilities
- Incident response requirements and constraints

Each detection requirement is traceable to a modeled threat scenario.

---

## Detection Stories
UTIOM uses **detection stories** to guide detection design.

A detection story describes:
- The adversary behavior to be detected
- The sequence of actions and context
- Expected evidence and signals
- Investigation hypotheses
- Potential response actions

Detection stories replace isolated alerts with context-driven detection logic.

---

## Engineering Process
Detection engineering follows a structured process:

1. Derive detection requirements from threat models
2. Design detection logic based on available telemetry
3. Implement detection logic as versioned artifacts
4. Validate detections through testing and simulation
5. Deploy detections with clear operational context
6. Monitor performance and reliability

This process ensures repeatability and accountability.

---

## Validation and Testing
Validation is a mandatory component of detection engineering in UTIOM.

Validation methods include:
- Purple team exercises
- Simulation of attacker behavior
- Replay of known attack patterns
- Detection coverage analysis against attack paths

Detection failures are treated as engineering defects and trigger improvement activities.

---

## Integration with Incident Response
Detection engineering is tightly coupled with incident response.

Detections are designed to:
- Support rapid scoping and impact assessment
- Reduce uncertainty during response
- Align with response playbooks and decision authority
- Enable containment with minimal business disruption

Detection outputs must be actionable, not merely informational.

---

## Continuous Improvement
Detection engineering continuously evolves through:

- Feedback from incidents and near-misses
- Threat hunting outcomes
- Validation results and false negative analysis
- Changes in adversary behavior and techniques

Improvements are prioritized based on risk, impact, and operational value.

---

## Relationship to TID-CMM
UTIOM leverages the Threat-Informed Detection Capability Maturity Model (TID-CMM) to assess and guide detection engineering maturity.

TID-CMM evaluates:
- Alignment of detections with threat models
- Engineering rigor and validation practices
- Operational reliability and consistency
- Feedback and improvement mechanisms

TID-CMM ensures that detection engineering progresses from ad-hoc implementations to engineered, validated, and adaptive capabilities.

---

## Key Principles
- Detections are engineered, not configured
- Threat models define detection requirements
- Validation is mandatory
- Detection quality is measurable
- Improvement is continuous

---

## Outcome
Through disciplined detection engineering, UTIOM enables security operations to detect meaningful adversary behavior reliably and support effective, business-aware incident response.
