---
description: Requirements for official support from the Rocket.Chat team
---

# Official support limitations

## Introduction

In order to obtain official support from our team, we have a minimum set of requirements. These requirements are necessary for us to access essential system information, to provide an SLA, to answer questions, or to provide a solution for the problem.

Only installations matching these minimum requirements can be covered by our SLAs and our paid Support Policy, some requirements may vary depending on the installation size as described in the following sections.

## Environment

In order to isolate external issues of missing or outdated dependencies, specific operational system issues, or problems during the manual installations we limited our official support to only installations using our Docker Images that follows our [Getting Support](../getting-support.md) guide.

We may expand this in the future once we find other options suitable for the above isolation.

### Why Docker?

[Docker](https://www.docker.com/) is widely used to package applications in containers and distribute them as images, providing abstraction and isolation layers from the OS \(operational system\). It allows the application to be shipped with a specific version of the OS compatibility layer and his own dependencies already installed and configured.

We require the installation to run the Docker image provided by the Rocket.Chat team, this makes it possible to isolate external factor. It ensures that the support request refers to our application and not to the following factors.

1. Problems during the compilation process
2. Problems during the installation process
3. Missing or outdated dependencies
4. Installation of non-official versions

Rocket.Chat's own cloud uses our official Docker images, which makes this installation method the most widely tested version. This ensures we can provide quick fixes and a more efficient way to reproduce problems leading to the most efficient support flow possible.

{% page-ref page="docker-containers/" %}

### Scalability

The usage of Docker-compatible containers orchestration/management systems such as Kubernetes, Rancher, or OpenShift can facilitate scaling of containerized Rocket.Chat instances making it possible to distribute load among different physical bare-metal servers or virtual machines.

Rocket.Chat's own cloud uses this approach to manage cloud-hosted instances with a high level of reliability and flexibility, we leverage the same expertise to provide documentation on how to configure and deploy scaled installations.

We require, for **scaled installations** \(with more than **one instance** or more than **2000 users**\), to be orchestrated and/or managed with one of the following:

1. SUSE Rancher
2. Red Hat Openshift
3. Kubernetes and Helm \(Managed by a cloud platform such as AWS, Google Cloud, etc, or self-managed\)
4. docker-compose

At this time, no other containers orchestration/management technologies will be supported by our Support team for any issues related to **scaled installations**.

### Monitoring

We require monitoring for all supported installations. All installations must continually collect [Metrics](https://github.com/RocketChat/Rocket.Chat.Metrics) regarding the installation's instances and database. Rocket.Chat supports the industry-standard Prometheus + Grafana monitoring stack. Grafana dashboards required for support are available in the [Metrics](https://github.com/RocketChat/Rocket.Chat.Metrics) repository.

### Hardware requirements

The minimum hardware requirements are described in the [Minimum Requirements](minimum-requirements.md) page, the support is limited to installations matching those requirements.

{% page-ref page="minimum-requirements.md" %}

## Data access

We do not require access to the servers, instances or databases to provide support, but we may require access to the logs if we consider them necessary to identify the problem.

Types of logs we may require:

1. Server logs
2. Web browser logs
3. Mobile logs

## Versions

Rocket.Chat cuts a new release every single month, please check the [Getting Support](../getting-support.md) for more information about the release cycles and make sure you are running a supported version before contacting support.

{% page-ref page="../getting-support.md" %}



