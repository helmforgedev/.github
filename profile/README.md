![HelmForge banner](./helmforge_banner.png)

# HelmForge

Open-source Helm charts, forged to last.

## Why HelmForge

- **Official upstream images** — every chart uses the image published by the application maintainers. No custom rebuilds, no proprietary layers.
- **MIT licensed, forever** — charts, CI, docs — everything is MIT. No open-core, no paid tiers, no license changes.
- **The open-source alternative to Bitnami** — no vendor lock-in, no abandoned free tier, no proprietary wrappers. Official images, real maintenance, free forever.
- **Pinned version tags** — explicit, immutable image tags. No `:latest`, no floating tags.
- **Cosign signed** — every OCI artifact is signed with Sigstore Cosign keyless signing.
- **Built-in S3 backup** — 20+ charts include automated backup to any S3-compatible endpoint.
- **Secure by default** — non-root containers, read-only filesystems, hardened security contexts.

## Install

```bash
helm repo add helmforge https://repo.helmforge.dev
helm repo update
helm install my-release helmforge/<chart-name>
```

Or via OCI:

```bash
helm install my-release oci://ghcr.io/helmforgedev/helm/<chart-name>
```

## Repositories

| Repository | Description |
|------------|-------------|
| [charts](https://github.com/helmforgedev/charts) | Source for all 56 Helm charts |
| [site](https://github.com/helmforgedev/site) | Documentation website ([helmforge.dev](https://helmforge.dev)) |

## Links

- **Website**: https://helmforge.dev
- **Charts catalog**: https://helmforge.dev/charts
- **Documentation**: https://helmforge.dev/docs
- **Comparison**: https://helmforge.dev/docs/comparison
- **Artifact Hub**: https://artifacthub.io/packages/search?repo=helmforge
