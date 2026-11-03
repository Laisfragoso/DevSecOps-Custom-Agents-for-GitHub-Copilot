# DevSecOps Custom Agents for GitHub Copilot

This repository contains a set of custom agents designed for **GitHub Copilot Chat in Visual Studio Code**. These agents support a practical DevSecOps workflow by helping development and security teams analyze vulnerabilities, validate security findings, remediate risks, and improve code quality.

The agents are designed to work together as a structured pipeline, covering the complete lifecycle from vulnerability discovery to secure and maintainable code delivery.

---

## DevSecOps Workflow

```text
Orca Security Vulnerability Report Agent
                    ↓
        Security Code Reviewer Agent
                    ↓
                Coding Agent
```

Each agent specializes in a specific phase of the DevSecOps lifecycle.

---

## Orca Security Vulnerability Report Agent

### Purpose

The Orca Security Vulnerability Report Agent analyzes vulnerability reports exported from security platforms such as Orca Security and transforms raw findings into actionable remediation plans for development teams.

### Capabilities

- Analyze vulnerability CSV exports.
- Validate report structure and finding consistency.
- Classify findings by severity and category.
- Prioritize remediation efforts based on risk.
- Distinguish between:
  - Real vulnerabilities
  - False positives
  - Third-party component findings
  - Repository governance findings
  - Docker findings
  - Infrastructure as Code (IaC) findings
- Generate technical remediation reports.
- Provide evidence-based recommendations.
- Support vulnerability triage processes.

### Primary Outcome

Transforms large volumes of security findings into structured, prioritized remediation guidance for development teams.

---

## Security Code Reviewer Agent

### Purpose

The Security Code Reviewer Agent acts as an Application Security (AppSec) specialist focused on validating vulnerabilities and guiding secure remediation directly in source code, infrastructure definitions, and DevOps pipelines.

### Capabilities

- Perform secure code reviews.
- Validate scanner findings before remediation.
- Identify potential false positives.
- Map vulnerabilities to OWASP and CWE standards.
- Review:
  - Application code
  - Docker configurations
  - Infrastructure as Code (IaC)
  - CI/CD pipelines
  - Dependency management
- Assess vulnerabilities such as:
  - SQL Injection
  - Cross-Site Scripting (XSS)
  - CSRF
  - SSRF
  - Path Traversal
  - Command Injection
  - Broken Authentication
  - Broken Access Control
  - IDOR/BOLA
  - Insecure Deserialization
  - Server-Side Template Injection (SSTI)
- Recommend secure remediation strategies.
- Generate validation and regression tests.
- Preserve application functionality while improving security.

### Primary Outcome

Provides validated, evidence-based security remediation with minimal impact on application behavior.

---

## Coding Agent

### Purpose

The Coding Agent focuses on maintainability, readability, refactoring, testing, and overall code quality improvements after security concerns have been addressed.

### Capabilities

- Refactor existing code.
- Improve readability and maintainability.
- Reduce technical debt.
- Simplify overly complex implementations.
- Generate unit and regression tests.
- Perform targeted bug fixes.
- Apply minimal and surgical code changes.
- Preserve existing project architecture and coding standards.
- Avoid unnecessary abstractions and overengineering.

### Core Principles

#### Think Before Coding

- Understand requirements before implementing changes.
- Avoid assumptions.
- Request clarification when necessary.

#### Simplicity First

- Implement only what is required.
- Prefer the smallest possible solution.
- Avoid speculative enhancements.

#### Surgical Changes

- Modify only the necessary code.
- Preserve project conventions.
- Avoid unrelated refactoring.

#### Goal-Driven Execution

- Focus on measurable outcomes.
- Verify behavior after every change.
- Use tests whenever possible.

### Primary Outcome

Produces cleaner, simpler, and more maintainable code without introducing unnecessary complexity.

---

## Combined Value

Together, these agents establish a complete DevSecOps workflow:

| Phase | Agent | Objective |
|---------|---------|------------|
| Discovery & Triage | Orca Security Vulnerability Report Agent | Analyze and prioritize vulnerabilities |
| Validation & Remediation | Security Code Reviewer Agent | Validate and remediate security findings |
| Optimization & Quality | Coding Agent | Improve maintainability and code quality |

---

## Benefits

### Security

- Faster vulnerability triage
- Reduced false positives
- Consistent security reviews
- OWASP-aligned remediation guidance

### Quality

- Cleaner codebases
- Reduced technical debt
- Improved maintainability
- Better testing practices

### Productivity

- Standardized review process
- Faster remediation cycles
- Consistent developer guidance
- Improved collaboration between Security and Engineering teams

---

## Installation

Copy the agent files into the local GitHub Copilot agents directory:

```text
C:\Users\<username>\.copilot\agents
```

After installation, restart Visual Studio Code to load the agents.

---

## Intended Audience

These agents are designed for:

- Application Security Engineers
- DevSecOps Engineers
- Security Champions
- Software Developers
- Technical Leads
- Platform Engineering Teams
- Engineering Managers

They provide a practical and repeatable approach to integrating security and code quality into daily development workflows.
