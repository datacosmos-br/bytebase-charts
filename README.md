# bytebase-charts

Datacosmos fork of the Bytebase Helm chart (`helm-charts/bytebase` in
[bytebase/bytebase](https://github.com/bytebase/bytebase)). The `datacosmos/charts`
branch carries only the chart; each push publishes it to
`oci://ghcr.io/datacosmos-br/bytebase-charts` (`.github/workflows/release-oci.yaml`).

| Version | Base | Change | Upstream |
|---|---|---|---|
| 1.1.4-dc1 | 1.1.4 (bytebase/bytebase@2fc5fe5aa36d) | `bytebase.autoscaling.enabled` omits `spec.replicas` | [bytebase/bytebase#21919](https://github.com/bytebase/bytebase/pull/21919) |

Retire the fork once upstream releases the change.
