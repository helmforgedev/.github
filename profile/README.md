<p align="center">
  <img src="./helmforge_banner.png" alt="HelmForge" width="960" />
</p>

<h1 align="center">HelmForge</h1>

<p align="center">
  Production-oriented Helm charts and Kubernetes packaging workflows built around official upstream images, explicit values contracts, and verifiable releases.
</p>

<p align="center">
  <a href="https://helmforge.dev"><strong>Website</strong></a>
  ·
  <a href="https://helmforge.dev/docs"><strong>Documentation</strong></a>
  ·
  <a href="https://repo.helmforge.dev"><strong>Helm Repository</strong></a>
  ·
  <a href="https://artifacthub.io/packages/search?repo=helmforge"><strong>Artifact Hub</strong></a>
  ·
  <a href="https://github.com/helmforgedev/charts"><strong>Charts</strong></a>
</p>

<p align="center">
  <a href="https://github.com/helmforgedev/charts/actions/workflows/ci.yml"><img src="https://github.com/helmforgedev/charts/actions/workflows/ci.yml/badge.svg" alt="Charts CI" /></a>
  <a href="https://github.com/helmforgedev/charts/actions/workflows/publish.yml"><img src="https://github.com/helmforgedev/charts/actions/workflows/publish.yml/badge.svg" alt="Charts Publish" /></a>
  <a href="https://www.apache.org/licenses/LICENSE-2.0"><img src="https://img.shields.io/badge/License-Apache--2.0-blue.svg" alt="License: Apache-2.0" /></a>
  <a href="https://artifacthub.io/packages/search?repo=helmforge"><img src="https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/helmforge" alt="Artifact Hub" /></a>
  <img src="https://img.shields.io/endpoint?url=https://repo.helmforge.dev/badges/charts-count.json" alt="Charts count" />
  <img src="https://img.shields.io/badge/Signed-GPG%20%2B%20Cosign-brightgreen" alt="GPG and Cosign signed" />
  <img src="https://img.shields.io/badge/Kubernetes-%3E%3D1.26-blue?logo=kubernetes" alt="Kubernetes >= 1.26" />
</p>

## What We Build

HelmForge is an open-source Helm chart ecosystem for teams that want standard Kubernetes, standard Helm, official upstream images, and practical day-2 operations without a proprietary chart or image layer.

The project currently maintains **62 Helm charts** across databases, messaging, identity, automation, CMS, analytics, AI tooling, networking, observability, and self-hosted applications. Charts are published through both a classic HTTPS Helm repository and OCI artifacts on GHCR.

Our design principle is simple:

> Use what upstream ships, make the Kubernetes contract explicit, and keep releases verifiable.

## Why HelmForge

- **Official upstream images** - charts prefer images published by the application maintainers, avoiding unnecessary rebuild layers and vendor-specific runtime wrappers.
- **Pinned image versions** - defaults use explicit tags instead of floating `latest` tags.
- **Apache-2.0 licensed** - project code, charts, documentation, and supporting tooling use a CNCF-aligned permissive license.
- **Signed releases** - packaged charts include GPG provenance and OCI artifacts are signed with Sigstore Cosign through GitHub Actions OIDC.
- **Values contracts** - every chart includes `values.yaml`, `values.schema.json`, examples, and CI scenarios.
- **Built-in backup patterns** - 38 charts include optional S3-compatible backup workflows.
- **Operator-aware boundaries** - documentation is explicit about what a chart manages and when a domain-specific operator is the better fit.
- **No open-core split** - charts, tests, docs, release automation, and examples are public.

## Install

Use the HTTPS Helm repository:

```bash
helm repo add helmforge https://repo.helmforge.dev
helm repo update
helm search repo helmforge/
helm install my-release helmforge/<chart-name> --version <version> -f values.yaml
```

Or pull directly from OCI:

```bash
helm install my-release oci://ghcr.io/helmforgedev/helm/<chart-name> --version <version> -f values.yaml
```

Browse the full catalog at [helmforge.dev/charts](https://helmforge.dev/charts) or [Artifact Hub](https://artifacthub.io/packages/search?repo=helmforge).

## Ecosystem

| Repository | Purpose |
|------------|---------|
| [charts](https://github.com/helmforgedev/charts) | Primary Helm chart repository, release automation, chart tests, schemas, and package metadata |
| [site](https://github.com/helmforgedev/site) | Documentation website at [helmforge.dev](https://helmforge.dev), chart catalog, roadmap, playground, and stack builder |
| [.github](https://github.com/helmforgedev/.github) | Organization profile and shared community health files |
| [fastmcp-server](https://github.com/helmforgedev/fastmcp-server) | Production-ready FastMCP server image with dynamic tool/resource/prompt loading |
| [fastmcp-tools](https://github.com/helmforgedev/fastmcp-tools) | Reusable MCP tool packages for GitHub, Kubernetes, HTTP, databases, and notifications |
| [kubectl](https://github.com/helmforgedev/kubectl) | Minimal multi-architecture kubectl image for Kubernetes operations |
| [strapi-base](https://github.com/helmforgedev/strapi-base) | Base Strapi image used by HelmForge Strapi deployments |
| [habs](https://github.com/helmforgedev/habs) | HelmForge Autonomous Bump System for validated image and chart update workflows |

## Project Signals

| Area | Current state |
|------|---------------|
| Charts | 62 chart packages |
| Stable charts | 58 stable charts |
| Backups | 38 charts with optional S3-compatible backup support |
| Distribution | HTTPS Helm repository and GHCR OCI registry |
| Release integrity | GPG provenance plus Sigstore Cosign signatures |
| Validation | Helm lint, strict lint, template rendering, helm-unittest, kubeconform, and Artifact Hub lint |
| Configuration | JSON Schema for every chart |
| License | Apache-2.0 |
| CNCF | Sandbox application preparation in progress |

## Community

HelmForge is preparing for CNCF Sandbox submission and is strengthening governance, maintainership, adoption tracking, and community health files as part of that process.

- [Governance](https://github.com/helmforgedev/charts/blob/main/GOVERNANCE.md)
- [Maintainers](https://github.com/helmforgedev/charts/blob/main/MAINTAINERS.md)
- [Adopters](https://github.com/helmforgedev/charts/blob/main/ADOPTERS.md)
- [Contributing](https://github.com/helmforgedev/charts/blob/main/CONTRIBUTING.md)
- [Code of Conduct](https://github.com/helmforgedev/.github/blob/main/CODE_OF_CONDUCT.md)
- [Security Policy](https://github.com/helmforgedev/.github/blob/main/SECURITY.md)

Public adopters currently include organizations using HelmForge charts in production for databases, application workloads, backups, identity, and platform services.

## Learn More

- Documentation: https://helmforge.dev/docs
- Chart catalog: https://helmforge.dev/charts
- Comparison with Bitnami and community charts: https://helmforge.dev/docs/comparison
- Roadmap: https://helmforge.dev/roadmap
- Artifact Hub: https://artifacthub.io/packages/search?repo=helmforge
- Public Helm repository: https://repo.helmforge.dev
