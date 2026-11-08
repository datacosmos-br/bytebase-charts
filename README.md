# bytebase-charts

Datacosmos fork of the Bytebase Helm chart (`helm-charts/bytebase` in
[bytebase/bytebase](https://github.com/bytebase/bytebase)). The `datacosmos/charts`
branch carries only the chart. Like the other datacosmos-br chart forks, it is
published by hand to `oci://ghcr.io/datacosmos-br/bytebase-charts` (GitHub Actions
is disabled for this repository by the organization):

```sh
helm package helm-charts/bytebase --destination packages
helm push packages/bytebase-<version>.tgz oci://ghcr.io/datacosmos-br/bytebase-charts
```

A published version is never overwritten; every change gets the next `-dcN`.

| Version | Base | Change | Upstream |
|---|---|---|---|
| 1.1.4-dc1 | 1.1.4 (bytebase/bytebase@2fc5fe5aa36d) | `bytebase.autoscaling.enabled` omits `spec.replicas` | [bytebase/bytebase#21919](https://github.com/bytebase/bytebase/pull/21919) |
| 1.1.4-dc2 | 1.1.4-dc1 | chart README: single-replica and HA guidance conditional on autoscaling (review on #21919) | [bytebase/bytebase#21919](https://github.com/bytebase/bytebase/pull/21919) |

Retire the fork once upstream releases the change.
