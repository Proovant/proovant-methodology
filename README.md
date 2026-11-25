# Proovant Security Methodology

## Find it. Challenge it. Prove it.

Proovant is an AI-assisted smart contract security review agent designed to identify potential vulnerabilities, challenge candidate findings, and validate them through executable proof-of-concept tests.

Our approach combines specialised security analysis, adversarial review, and Foundry-based testing to make findings more reproducible and actionable.

[Website](https://www.proovant.com) · [Security Reviews](https://github.com/Proovant/proovant-security-reviews) · [X](https://x.com/Proovant_ai)

---

## Review Pipeline

### 1. Scope & Threat Model

We map the codebase, identify important contracts and value flows, and establish the threat model.

The goal is to understand what the system is intended to do, what assets it protects, and how an attacker might interact with it.

### 2. Parallel Security Analysis

Specialised analysis agents examine different vulnerability classes, including:

- Accounting and state consistency
- Access control and upgradeability
- External calls and interaction patterns
- State transitions and logic edge cases
- Oracle and economic-design risks
- Cross-component interactions
- Adversarial attack paths

The agents generate candidate leads. These are not automatically treated as confirmed findings.

### 3. Adversarial Validation

A separate validation stage challenges candidate findings.

It examines whether the issue is reachable, whether the claimed impact is realistic, and whether the behaviour is already addressed by the code or documented design.

Candidates that do not survive validation are rejected or marked unconfirmed.

### 4. Executable Proof of Concept

Surviving candidates are developed into Foundry tests where feasible.

A finding is considered confirmed by the engine only when its reproduction test passes under the documented assumptions.

A passing test demonstrates the described scenario in that test environment. It does not, by itself, guarantee exploitability on a live deployment.

### 5. Report & Review

Findings are documented with:

- Description and affected component
- Severity reasoning
- Impact and attack scenario
- Reproduction steps or PoC
- Assumptions and limitations
- Recommended remediation

A human reviews the report before delivery. Independent security researcher review may be included depending on the engagement scope.

---

## What We Aim to Deliver

- Clear, evidence-backed security findings
- Reproducible PoCs where feasible
- Practical remediation guidance
- Transparent assumptions and limitations
- A documented scope and reviewed code version

---

## Scope & Limitations

Proovant is AI-assisted security analysis. It does not guarantee that a codebase is vulnerability-free and does not replace a comprehensive independent security audit.

The engine may be less effective on:

- Deep cryptographic circuits and custom cryptography
- Complex cross-protocol integrations
- Issues requiring extensive live on-chain context
- Behaviours outside the agreed scope
- Scenarios that cannot be reproduced in the available test environment

Some PoCs may use mocks or simplified components. Reports should identify these assumptions and distinguish test-environment behaviour from verified live-system behaviour.

Results depend on the code version, scope, documentation, configuration, and available testing environment.

---

## Transparency

Proovant is AI-assisted and uses third-party language models as part of its analysis workflow.

The exact data-handling arrangements depend on the model provider and engagement configuration. Clients should confirm the applicable processing and retention terms before submitting sensitive code.

Each review should identify the code version reviewed, scope, date, and any material assumptions.

---

## Contact

For a smart contract security review:

[Request a review](https://www.proovant.com)

Website: https://www.proovant.com  
Email: info@proovant.com
