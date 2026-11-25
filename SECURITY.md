# Security Policy

## Security and Safety at CIRNETLAB

CIRNETLAB develops a multi-platform STEM and engineering learning ecosystem spanning circuit design, simulation, scientific computing, programming, embedded systems, physical laboratories, and educational workflows.

Security, privacy, reliability, and physical safety are fundamental engineering requirements. CIRNETLAB distinguishes software correctness from electrical safety and does not treat successful builds, simulations, or RTL tests as proof of safe physical operation.

## Supported Versions

Security reports are welcome for actively maintained repositories, current development branches, and published releases that are explicitly supported by their maintainers.

Development builds and experimental components, including `0.x` and pre-release versions, may change without notice and must not be assumed production-ready. Archived, superseded, or unsupported versions do not receive guaranteed security updates. Report issues that may also affect maintained versions, and identify the exact affected Git revision, release, or artifact whenever possible.

## Security Scope

Relevant security and safety issues include:

| Domain | Examples |
| --- | --- |
| Identity, access, and data | Authentication or authorization bypass, session compromise, privilege escalation, unauthorized access to projects, captures, or educational records. |
| APIs, contracts, and clients | REST, WebSocket, RPC, schema or NCAP parsing vulnerabilities; injection, unsafe deserialization, replay, and cross-boundary validation failures. |
| Simulation and execution | Untrusted input handling, worker isolation failures, resource exhaustion, unsafe process execution, or compromised result integrity. |
| Hardware and embedded systems | Unauthorized device control, unsafe routing or energization, interlock or watchdog bypass, failed Stop, stale permits, or unsafe firmware and bitstream handling. |
| Supply chain and infrastructure | Compromised dependencies, build or CI/CD workflows, exposed credentials, artifact tampering, integrity verification failures, and insecure deployment configurations. |

Ordinary defects and feature requests without a security, privacy, integrity, or physical safety impact should use the repository's regular issue tracker.

## Reporting a Vulnerability

Use the affected repository's **Security → Advisories → Report a vulnerability** option when GitHub private vulnerability reporting is available. If multiple repositories are affected, submit a single private report to the primary affected repository and identify the other components.

If private reporting is unavailable, open a minimal public issue requesting a private security contact. Do not include vulnerability details, exploit code, sensitive data, credentials, or hardware safety bypass instructions in that issue. Wait for a private reporting channel before sharing sensitive evidence.

A useful report includes:

- Affected repositories, versions, Git revisions, and artifact digests, if known.
- A concise description, prerequisites, affected trust boundaries, and potential impact.
- Minimal, safe reproduction steps and sanitized logs or evidence.
- For hardware issues, the relevant board, firmware, hardware profile, and observed safety behavior, if safely available.
- Suggested mitigations or fixes, if available.

Never include live secrets, personal information, private educational records, or unnecessary third-party data.

## Responsible Research and Physical Safety

Conduct research only on systems and hardware you own or are explicitly authorized to test. Prefer isolated environments, synthetic data, virtual stations, and non-energized test setups. Do not disrupt shared services, access other users' data, exceed authorized privileges, or bypass physical protection.

For Lab-First systems, safety and correctness remain independent. Unknown or unsafe electrical conditions must prevent energization. Hardware routing must not repair or replace a learner's actual circuit wiring. A Stop request is not proof of safe shutdown; unconfirmed cleanup requires quarantine.

If a potential physical hazard is identified, stop the affected experiment using approved safety procedures, notify the responsible operator, and report the issue privately. Do not reproduce hazardous conditions on live equipment. Unverified physical capabilities must remain unavailable.

## Coordinated Disclosure

Maintainers will aim to acknowledge reports, assess their security and safety impact, coordinate remediation, and communicate relevant mitigations. Response times and patch availability depend on severity, reproducibility, affected components, and maintainer resources; no fixed service-level agreement is promised.

Please coordinate public disclosure with the maintainers to allow reasonable time for mitigation. Security advisories and reporter credit may be provided where appropriate and with the reporter's consent. This policy does not constitute a bug bounty or authorization to test third-party systems.

## Security Principles

CIRNETLAB's engineering practices prioritize least privilege, explicit trust boundaries, bounded execution, canonical contracts, dependency and artifact integrity, reproducible verification, and fail-safe hardware control. Git revisions and SHA-256 digests establish traceability and integrity; they do not alone establish trust or electrical safety.

This organization-wide policy applies to repositories maintained by [CIRNETLAB](https://github.com/cirnetlab). Repository-specific policies may add requirements for their respective domains.

## Repository security baseline

For each maintained repository, owners should review access and MFA, least-privilege workflow permissions, branch protection and review, dependency/advisory monitoring, secret scanning where available, and private vulnerability reporting where supported. Review pinned dependencies and third-party artifacts before releases. Never commit secrets; revoke and rotate exposed credentials, assess affected artifacts, and preserve incident evidence securely. Separate actual vulnerability remediation and settings changes from this documentation policy. Document checks as PASS, FAIL, BLOCKED or NOT_RUN against an exact revision. No security feature is claimed enabled by this document.
