# ⚠️ Bank-Vaults is being migrated ⚠️

As we [announce](https://github.com/banzaicloud/bank-vaults/discussions/1878) a couple weeks ago, Bank-Vaults is being migrated to a [new GitHub organization](https://github.com/bank-vaults).

New contributions may not be accepted in this repository depending on the state of the migration. We suggest that you open an issue before sending pull requests.

Thank you for your cooperation and understanding!

<p align="center"><img src="docs/images/logo/bank-vaults-logo-vertical.svg" width="270"></p>

<p align="center">

  <a href="https://hub.docker.com/r/banzaicloud/bank-vaults/">
    <img src="https://img.shields.io/docker/automated/banzaicloud/bank-vaults.svg" alt="Docker Automated build">
  </a>

  <a href="https://hub.docker.com/r/banzaicloud/bank-vaults/">
    <img src="https://img.shields.io/docker/pulls/banzaicloud/bank-vaults.svg?style=shield" alt="Docker Pulls">
  </a>

  <a href="https://godoc.org/github.com/banzaicloud/bank-vaults">
    <img src="https://godoc.org/github.com/banzaicloud/bank-vaults?status.svg" alt="GoDoc">
  </a>

  <a href="https://circleci.com/gh/banzaicloud/bank-vaults">
    <img src="https://circleci.com/gh/banzaicloud/bank-vaults.svg?style=shield" alt="CircleCI">
  </a>

  <a href="https://goreportcard.com/badge/github.com/banzaicloud/bank-vaults">
    <img src="https://goreportcard.com/badge/github.com/banzaicloud/bank-vaults" alt="Go Report Card">
  </a>

  <a href="https://gitpod.io/#https://github.com/banzaicloud/bank-vaults">
    <img src="https://img.shields.io/badge/Gitpod-Ready--to--Code-blue?logo=gitpod" alt="Gitpod Ready-to-Code">
  </a>

  <a href="https://lgtm.com/projects/g/banzaicloud/bank-vaults/alerts/">
    <img alt="Total alerts" src="https://img.shields.io/lgtm/alerts/g/banzaicloud/bank-vaults.svg?logo=lgtm&logoWidth=18"/>
  </a>

</p>

*Bank Vaults is a thick, tricky, shifty right with a fast and intense tube for experienced surfers only, located on Mentawai. Think heavy steel doors, secret unlocking combinations and burly guards with smack-down attitude. Watch out for clean-up sets.*

*Bank-Vaults is an umbrella project which provides various tools for Vault to make using and operating Hashicorp Vault easier. It's a wrapper for the official Vault client with automatic token renewal and built-in Kubernetes support, dynamic database credential provider for Golang `database/sql` based clients. It has a CLI tool to automatically initialize, unseal, and configure Vault. It also provides a Kubernetes operator for provisioning, and a mutating webhook for injecting secrets.*

---

**Bank-Vaults** is a core building block of the **[Banzai Cloud Pipeline](https://github.com/banzaicloud/pipeline)** platform. Some of the usage patterns are highlighted through these blog posts:

**Securing Kubernetes deployments with Vault:**

- [Authentication and authorization of Pipeline users with OAuth2 and Vault](https://banzaicloud.com/blog/oauth2-vault/)
- [Dynamic credentials with Vault using Kubernetes Service Accounts](https://banzaicloud.com/blog/vault-dynamic-secrets/)
- [Dynamic SSH with Vault and Pipeline](https://banzaicloud.com/blog/vault-dynamic-ssh/)
- [Secure Kubernetes Deployments with Vault and Pipeline](https://banzaicloud.com/blog/hashicorp-guest-post/)
- [Vault Operator](https://banzaicloud.com/blog/vault-operator/)
- [Vault unseal flow with KMS](https://banzaicloud.com/blog/vault-unsealing/)
- [Monitoring Vault on Kubernetes using Cloud Native technologies](https://banzaicloud.com/blog/monitoring-vault-grafana/)
- [Inject secrets directly into pods from Vault](https://banzaicloud.com/blog/inject-secrets-into-pods-vault-revisited/)
- [Backing up Vault with Velero](https://banzaicloud.com/blog/vault-backup-velero/)
- [Vault replication across multiple datacenters on Kubernetes](https://banzaicloud.com/blog/vault-multi-datacenter/)
- [More blog posts about Bank-Vaults](https://banzaicloud.com/tags/bank-vaults/)

We use Vault across our large Kubernetes deployments and all the projects were `reinventing` the wheel. We have externalized all the codebase into this project and removed all the [Pipeline](https://github.com/banzaicloud/pipeline) and [Hollowtrees](https://github.com/banzaicloud/hollowtrees) dependencies thus this project can be used independently as a CLI tool to manage Vault, a Golang library to build upon (OAuth2 tokens, K8s auth, Vault operator, dynamic secrets, cloud credential storage, etc), Helm chart for a HA cluster, operator, mutating webhook and a collection of scripts to support some advanced features (dynamic SSH, etc).

>We take bank-vaults' security and our users' trust very seriously. If you believe you have found a security issue in bank-vaults, please contact us at security@banzaicloud.com.

Bank-Vaults is a core part of [Banzai Cloud Pipeline](https://github.com/banzaicloud/pipeline), a Cloud Native application and devops platform that natively supports multi- and hybrid-cloud deployments.

## Supported Kubernetes and Vault versions

This project aims to support the [latest supported Vault image versions](https://hub.docker.com/_/vault), and three Kubernetes minor versions excluding the latest one.

## Installing

You usually don't need to use the CLI directly, rather you should install the charts and create Vault instances with the operator and use the webhook inside Kubernetes to mutate Kubernetes resources.

To grab the `bank-vaults` and `vault-env` CLI binaries go to the [releases](https://github.com/banzaicloud/bank-vaults/releases) page and download them.

## Documentation

Read more about the usage of bank-vaults in the [detailed
Bank-Vaults documentation](https://banzaicloud.com/docs/bank-vaults/) and in our [blog posts about Bank-Vaults](https://banzaicloud.com/tags/bank-vaults/).

## Development

If you want to hack with bank-vaults please follow the [development
documentation](https://banzaicloud.com/docs/bank-vaults/contributing/).

## Bank-Vaults Support

If you encounter any problems that is not addressed in our documentation, [open an issue](https://github.com/banzaicloud/bank-vaults/issues) or talk to us on the [Banzai Cloud Slack channel #Bank-Vaults](https://banzaicloud.com/invite-slack/).

If you find this project useful, help us:

- Support the development of this project and star this repo! :star:
- If you use Bank-Vaults in a production environment, add yourself to the list of production [adopters](https://github.com/banzaicloud/bank-vaults/blob/main/ADOPTERS.md).:metal: <br>
- Help new users with issues they may encounter :muscle:
- Send a pull request with your new features and bug fixes :rocket:

### Engineering Blog

To be up-to-date with Bank-Vaults and the other open source and commercial [products of Banzai Cloud, read our blog](https://banzaicloud.com/blog/).

## Credits

Kudos to HashiCorp for open sourcing Vault and making secret management easier and more secure.

## License

Copyright (c) 2017-2021 [Banzai Cloud, Inc.](https://banzaicloud.com)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
