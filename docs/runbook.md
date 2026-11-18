# Runbook: boutique-productcatalogservice

- **Language:** Go
- **Owner:** @arch-beagel-test/storefront
- **Calls:** nothing

## It's down

1. `kubectl logs deploy/productcatalogservice --tail=200`
2. `kubectl rollout restart deploy/productcatalogservice`
3. If a dependency is failing, its runbook is in that repository's `docs/runbook.md`.

## Before changing who it calls

Read boutique-deploy `adr/cross/0002` and `0003`. A new call is a change to `protos/demo.proto` first.
