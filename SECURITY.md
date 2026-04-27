# Security Policy

## Supported Versions

We provide security fixes for the **latest released version** of HelmForge-maintained
artifacts, including Helm charts, utility container images, MCP packages, and
documentation/runtime tooling.

Older versions are not actively maintained unless a maintainer explicitly marks a
release line as supported in the affected repository.

## Reporting a Vulnerability

If you discover a security vulnerability in any HelmForge repository or published
artifact, please report it responsibly.

**Do not open a public GitHub issue for security vulnerabilities.**

Instead, use one of the following methods:

1. **GitHub Security Advisories / Private Vulnerability Reporting** (preferred): use the affected repository's **Security** tab when available.
2. **Charts repository advisory**: for chart issues, [report a vulnerability in `helmforgedev/charts`](https://github.com/helmforgedev/charts/security/advisories/new).
3. **Email**: <berlofa@helmforge.dev> or <maicon.berloffa@gmail.com>

If you are unsure which repository is affected, use email and include as much
context as possible. Maintainers will route the report to the right repository.

### What to include

- Affected repository or artifact
- Chart, package, image, or version affected
- Description of the vulnerability
- Steps to reproduce (if applicable)
- Potential impact

### Response timeline

- **Acknowledgment**: within 72 hours
- **Initial assessment**: within 7 days
- **Fix or mitigation**: best effort, typically within 30 days depending on severity

## Scope

This organization-wide policy covers vulnerabilities in HelmForge-maintained
repositories and artifacts, including:

- Helm chart templates and default configurations
- Utility images and Docker packaging maintained by HelmForge
- MCP server, MCP tool packages, resources, prompts, and validation logic
- CI/CD workflows, release automation, and repository metadata
- Default `values.yaml` settings that introduce security risks

This policy does **not** cover:

- Vulnerabilities in upstream application images (report those to the upstream project)
- Misconfiguration by end users in their own `values.yaml` overrides
- Infrastructure or cluster-level security issues

## Security Best Practices

When deploying HelmForge charts in production:

- Always pin chart versions (`--version`)
- Review `values.yaml` defaults before deploying
- Use `securityContext` and `podSecurityContext` settings provided by each chart
- Enable network policies where your cluster supports them
- Use TLS for ingress endpoints
- Rotate credentials and secrets regularly

When using HelmForge utility images or MCP packages:

- Pin image tags and package versions
- Review runtime permissions, mounted credentials, and network access
- Keep dependencies updated through the published release process
