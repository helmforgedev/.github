# HelmForge

Reusable open source Helm charts for Kubernetes workloads.

HelmForge publishes charts in two formats:

- Helm repository: `https://repo.helmforge.dev`
- OCI registry: `oci://ghcr.io/helmforgedev/helm`

## What You Will Find Here

- production-oriented Helm charts for common self-hosted and infrastructure workloads
- chart documentation and usage examples
- CI-tested templates with local runtime validation in `k3d`
- Artifact Hub distribution and GitHub Container Registry publishing

## Main Repositories

- [charts](https://github.com/helmforgedev/charts): source repository for all Helm charts
- [site](https://github.com/helmforgedev/site): public documentation website

## Popular Charts

- [postgresql](https://github.com/helmforgedev/charts/tree/main/charts/postgresql)
- [mysql](https://github.com/helmforgedev/charts/tree/main/charts/mysql)
- [redis](https://github.com/helmforgedev/charts/tree/main/charts/redis)
- [rabbitmq](https://github.com/helmforgedev/charts/tree/main/charts/rabbitmq)
- [keycloak](https://github.com/helmforgedev/charts/tree/main/charts/keycloak)
- [minecraft](https://github.com/helmforgedev/charts/tree/main/charts/minecraft)
- [komga](https://github.com/helmforgedev/charts/tree/main/charts/komga)
- [flowise](https://github.com/helmforgedev/charts/tree/main/charts/flowise)

## Quick Start

### Helm repository

```bash
helm repo add helmforge https://repo.helmforge.dev
helm repo update
helm search repo helmforge/
helm install my-release helmforge/<chart-name>
```

### OCI

```bash
helm install my-release oci://ghcr.io/helmforgedev/helm/<chart-name>
```

## Documentation

- Website: https://helmforge.dev
- Chart docs: https://helmforge.dev/docs/charts
- Artifact Hub: https://artifacthub.io/packages/search?repo=helmforge

## Contributing

Contributions are welcome in the chart source repository:

- [helmforgedev/charts](https://github.com/helmforgedev/charts)

Please follow the repository contribution guide and PR workflow documented there.
