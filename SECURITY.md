# Security Policy

## Reporting vulnerabilities

Do not file exploitable vulnerabilities, credentials, confidential logs or personal data in public issues or pull requests. Use the affected repository's private vulnerability reporting facility when enabled. If unavailable, request a secure reporting channel from the repository maintainer without posting sensitive details. Provide affected versions, impact, minimal reproduction and remediation suggestions through the authorized channel. Coordinate disclosure with maintainers; do not test systems without authorization.

## Development and publication requirements

- Treat inputs and third-party source, packages, scripts and workflows as untrusted. Isolate execution with ephemeral environments, minimal filesystem and network access, bounded resources and no production credentials.
- Separate developer, reviewer and deployment identities. Protect default branches; require independent evidence and human release authorization. Keep security policy and trusted CI outside agent authority.
- Use least-privilege task-specific credentials and secret storage; never commit actual keys, live configurations or sensitive data. Rotate exposed credentials immediately and assess Git history, artifacts and logs before publication.
- Review dependencies and licenses, pin reviewed build dependencies and CI actions, and generate a component inventory. Require risk-appropriate tests and block release on unresolved critical vulnerabilities.
- Public source code and reproducible architecture are encouraged; sensitive operational details and active undisclosed vulnerabilities remain restricted. Reassess temporary restrictions periodically.
- Back up Git history, LFS objects, project and review metadata, release artifacts and dependencies separately. Encrypt and restrict backups, test restoration and offline builds, and reconcile changes without overwriting divergent history.

This document sets requirements, not a guarantee or evidence of deployed controls. Each project must document its actual support scope, security capabilities and private reporting channel before release.
