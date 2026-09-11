# Changelog

## [3.0.0] - 2026-09-11

### Overview

First release of the **IONOS CLOUD DBaaS MariaDB v2** Python SDK, generated from
version `2.0.0` of the DBaaS MariaDB API.

This SDK is published to the same PyPI project as the v1 SDK,
`ionoscloud-dbaas-mariadb`, as a major version bump, and keeps the same import
path (`import ionoscloud_dbaas_mariadb`). Upgrading with
`pip install -U ionoscloud-dbaas-mariadb` therefore replaces the v1 client with
the v2 client under an unchanged import — the API surface differs, see
*Breaking changes* below.

To stay on v1, pin `ionoscloud-dbaas-mariadb<3`. The v1 SDK remains available from
[sdk-python-dbaas-mariadb](https://github.com/ionos-cloud/sdk-python-dbaas-mariadb).

### Features

- **ClustersApi** — `clusters_post` (create), `clusters_get` (list),
  `clusters_find_by_id` (retrieve), `clusters_put` (ensure) and
  `clusters_delete` (delete).
- **BackupsApi** — `backups_get` (list), `backups_find_by_id` (retrieve).
- **BackupLocationsApi** *(new in v2)* — `backuplocations_get`,
  `backuplocations_find_by_id`.
- **VersionsApi** *(new in v2)* — `versions_get`, `versions_find_by_id`.
- Regional endpoints, defaulting to `https://mariadb.de-txl.ionos.com/v2`.
- Bearer (JWT) token authentication and HTTP basic authentication.
- Pydantic v2 models.

### Breaking changes vs. the v1 SDK (2.x)

**Operations**

- `clusters_patch` (`PATCH /clusters/{clusterId}`) is replaced by `clusters_put`
  (`PUT /clusters/{clusterId}`), which has ensure semantics and takes a
  `ClusterEnsure` with a required `id`.
- `clusters_restore` is removed. Restoring is now done at create/ensure time via
  the cluster's `restoreFromBackup` property.
- `cluster_backups_get` (per-cluster backup listing) is removed; use
  `backups_get`.

**Renamed models**

| v1 | v2 |
| --- | --- |
| `CreateClusterRequest` / `CreateClusterProperties` | `ClusterCreate` / `Cluster` |
| `PatchClusterRequest` / `PatchClusterProperties` | `ClusterEnsure` / `Cluster` |
| `ClusterResponse` / `ClusterList` | `ClusterRead` / `ClusterReadList` |
| `Connection` | `MariadbClusterConnection` |
| `DBUser` | `MariadbUser` |
| `State` | `MariadbClusterStates` |
| `BackupProperties` | `ClusterBackup` |
| per-status-code error models (`ClustersGet400Response` … `ClustersGet503Response`) | a single `Error` / `ErrorMessagesInner` |

**Renamed and restructured cluster properties**

- `mariadbVersion` → `version`
- `displayName` → `name`
- `connections` (a list of at most one `Connection`) → `connection`, a single
  `MariadbClusterConnection`; its `cidr` field is now `primaryInstanceAddress`
- `fromBackup` → `restoreFromBackup`
- `instances` changes type: it was an integer (1–5); it is now an
  `InstanceConfiguration` object. The former sibling fields `cores`, `ram` and
  `storageSize` move inside it, alongside `count`

**Newly required by the API**

- A cluster now requires `name`, `version`, `instances`, `connection`,
  `maintenanceWindow` and `backup`
- `backup` now requires both `location` and `retentionDays` (`retentionDays` is
  new; in v1 `backup` carried only an optional `location`)
- Initial credentials now include a `database` name alongside `username`

  Note: model fields in this SDK are generated as optional, so these
  requirements are enforced by the API, not by client-side validation.

**New cluster properties**

- `logsEnabled`, `metricsEnabled`

### Requirements

- Python >= 3.9, < 4.0
