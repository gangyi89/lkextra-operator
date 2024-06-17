# LKExtras Operator

The LKExtras operator is a Kubernetes operator designed to extend the functionality of Linode Kubernetes Engine (LKE). It provides automatic node taint management, amongst other features, simplifying cluster administration tasks.

## Features

- **Automated node taint management**: LKExtras automatically manages node taints in a Linode Kubernetes cluster. When you scale up a node pool, LKExtras automatically applies the necessary taints, reducing manual overhead.

## Getting Started

### Prerequisites

- A running Kubernetes cluster
- Helm 3 installed

### Installing the Chart

To install the chart with the release name `my-release`:

\```bash
helm repo add lkextras https://<chart-repository>
helm install my-release lkextras/lkextras
\```

> **Tip**: List all releases using `helm list`

## Configuration

The following table lists the configurable parameters of the LKExtras chart and their default values.

| Parameter | Description | Default |
|--|--|--|
| `image.repository` | Image repository | `lkextras.azurecr.io/lkextras-operator` |
| `image.pullPolicy` | Image pull policy | `IfNotPresent` |
| `image.tag` | Image tag | `"0.0.1"` |
| `imagePullSecrets` | Image pull secrets (for private repositories) | `[]` |
| `tolerations` | Tolerations for the LKExtras operator pod | `[]` |
| `affinity` | Node affinity settings for the LKExtras operator pod | `{}` |
| `nodePools` | A list of node pools to manage | `[]` |

Refer to the [values.yaml](values.yaml) file for examples of how to set these parameters.

## Roadmap
