# Engineering Standards

## Boundaries and interoperability

Projects own their source, data, versioning, tests and release lifecycle independently of NextDeveloper. Prefer explicit versioned contracts, documented APIs/events and modular boundaries. Java with Spring Boot is the default for new JVM services, not a constraint on suitable research or upstream software. Choose service boundaries based on workload and domain; avoid premature microservices. Document decisions and exceptions in ADRs. No shared database dependencies across independent services without an explicit reviewed agreement.

## Two production tracks

- **Native development:** Requirements and acceptance tests precede implementation; document API contracts, error behavior, migrations, observability and reproducible builds.
- **Open-source adaptation:** Evaluate maintenance, security, provenance and license compatibility; preserve upstream history, attribution and licenses; prefer supported extension points, adapters and a separate presentation layer. Pin validated versions, stage upstream updates, execute contract and regression tests; keep patches explicit when unavoidable. Do not promise compatibility without verification.

## Human-centered design

Research users and tasks, design alternatives, validate an approved product-specific visual identity and interaction model; avoid default AI-dashboard styling or copying proprietary interfaces. Accessibility, localization, keyboard operation, usability and meaningful feedback are acceptance criteria, not optional decorations. Disclose AI assistance truthfully.

## Verification and release

Maintain versioned requirements and acceptance criteria; run independent functional, unit, integration, security, dependency/license, performance and accessibility checks as applicable. Record actual results and limitations. Do not fabricate test evidence. For new Java services prefer repeatable Maven/Gradle commands usable with or without GitHub Actions. Require independent review and human release approval according to [AI-GOVERNANCE.md](AI-GOVERNANCE.md).

## Operational continuity

Use provider-neutral repository, project, task and AI interfaces. GitHub Projects, Issues, repositories, pull requests and Actions are the initial online adapters. A local Git forge (Forgejo or GitLab assessed by pilot), metadata exports, independent CI and cached dependencies support outage recovery. Verify backups, restoration and synchronization before claiming offline operation. Store sensitive information separately and keep deployed infrastructure configuration out of public repositories.

## Bilingual repository documentation

- Every HCC project repository must provide a root `README.md` in English (the default and canonical version) and `README.tr.md` in Turkish.
- Both files must link to each other near the top: `[English](README.md) · [Türkçe](README.tr.md)`.
- Keep the purpose, scope, status, standards, navigation, permissions, and limitations equivalent in both languages. When a README changes materially, update both in the same reviewed change. Review translation accuracy and links; never imply a different approval, license, security, or implementation status in a translation.
- Apply this standard to new repositories at initialization and to existing repositories during their next documentation review. Do not change repository visibility, licensing, or software behavior merely to adopt this standard.
- English remains authoritative if translations diverge; correct discrepancies through the normal human-reviewed process. This requirement covers root project READMEs; translate other documentation as appropriate to its audience and risk.
