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

<a id="bilingual-repository-documentation"></a>

## Four-language repository documentation

- Every HCC-owned repository and project/module README must support four languages: English (`README.md`, default and canonical), Turkish (`README.tr.md`), German (`README.de.md`), and Arabic (`README.ar.md`).
- Link all four language versions near the top: [English](README.md) · [Türkçe](README.tr.md) · [Deutsch](README.de.md) · [العربية](README.ar.md). Use equivalent relative paths within each README directory. Existing additional languages remain supported and must not be removed.
- Keep purpose, scope, status, standards, navigation, permissions, limitations and factual content equivalent. Material changes update all four versions in the same reviewed change. Preserve exact code, commands, identifiers, links and license notices; check Arabic right-to-left readability and terminology.
- For legacy long-form documents, a clearly labeled localized overview may be an interim navigation aid, not a completed translation. Record missing or incomplete translations and review them before declaring four-language parity.
- Apply to new projects at initialization, including first-party module and project READMEs. Preserve unmodified third-party upstream README files, original research/source archives and attribution; add separate HCC-owned documentation where necessary.
- English remains authoritative if translations diverge; correct discrepancies through the normal human-reviewed process. Adoption changes documentation only, never repository visibility, licensing, software behavior, permissions or deployment.
