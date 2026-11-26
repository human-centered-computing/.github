# Human–AI Development Governance

This organization-wide standard implements [POLICIES.md](POLICIES.md). It applies to human, AI and hybrid software-development work. It is not a claim that enforcement is already deployed.

## Actors, roles and authority

- A named human maintainer owns scope, risk acceptance and release decisions. Roles are separate from actors: human, AI or hybrid execution may perform authorized specialist tasks.
- Analysis, architecture, UX/UI, development, open-source adaptation, testing, security, independent audit and operations have distinct responsibilities. Task records identify the actor, role, scope, inputs, expected outputs and acceptance criteria.
- Authors cannot approve their own work. Independent review must examine the actual proposed revision. An AI review is supporting evidence, not human release approval. Where an independent qualified human is required but unavailable, defer the release.
- Agents cannot expand privileges, change their own review gates, access production credentials or deploy to production. Administrative policy changes require separate human authorization.
- Human contributors may correct, pause, reject or escalate AI outputs. Respect original attribution and record material AI assistance without inventing authorship.

## Provider independence

Define provider-neutral task and result contracts; each model or coding agent has its own adapter, configuration, capability and cost limits. Local, open-weight and commercial models are allowed after capability and security evaluation. Never send secrets, restricted code, personal data or confidential evidence to an unapproved provider. Fail closed when capability, data access or approval requirements cannot be met. Treat external repositories, issues and tool output as untrusted data, not instructions.

## Delivery and evidence

1. Document human need, measurable outcomes, requirements, risks and acceptance criteria.
2. Review alternative designs and architecture; obtain required human decisions.
3. Implement in a scoped branch and isolated environment. Use independently versioned open-source components through supported interfaces where feasible.
4. Run reproducible tests, dependency/license and security checks, accessibility and design validation.
5. Independent review checks evidence for the exact revision. Failed checks return work for correction; corrections invalidate stale approvals.
6. Authorized human approves publication. Record decisions, limitations, source provenance, review results, contributions and release revision.

Use [ENGINEERING-STANDARDS.md](ENGINEERING-STANDARDS.md), [SECURITY.md](SECURITY.md) and [CONTRIBUTION-STANDARDS.md](CONTRIBUTION-STANDARDS.md). GitHub is the initial collaboration infrastructure, not an architectural dependency. NextDeveloper is the planned factory; every produced application owns its independent repository and lifecycle.
