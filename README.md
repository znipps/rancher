# Rancher

Rancher is an open source project that provides a complete platform for operating Docker in production. It provides infrastructure services such as multi-host networking, global and local load balancing, and volume snapshots. It integrates native Docker management capabilities such as Docker Machine and Docker Swarm. It offers a rich user experience that enables devops admins to operate Docker in production at large scale.

## Latest Release

* Beta - v1.6.10 - `rancher/server:latest` - Read the full release [notes](https://github.com/rancher/rancher/releases/tag/v1.6.10).

* Stable - v1.6.10 - `rancher/server:stable` - Read the full release [notes](https://github.com/rancher/rancher/releases/tag/v1.6.10).

To get automated notifications of our latest release, you can watch the announcements category in our [forums](http://forums.rancher.com/c/announcements), or subscribe to the RSS feed `https://forums.rancher.com/c/announcements.rss`.

## Installation

Rancher is deployed as a set of Docker containers.  Running Rancher is as simple as launching two containers.  One container as the management server and another container on a node as an agent.  You can install the containers in following approaches.

* [Manually](#launching-management-server)
* [Terraform](https://github.com/rancher/terraform-modules)
* [Puppet](https://github.com/nickschuch/puppet-rancher) (Thanks @nickschuch)
* [Ansible](https://github.com/joshuacox/ansibleplaybook-rancher)
* [SaltStack](https://github.com/komljen/rancher-salt)

### Requirements

* [Supported Docker version](http://rancher.com/docs/rancher/v1.6/en/hosts/#supported-docker-versions)
* Any modern Linux distribution with a [supported Docker version](http://rancher.com/docs/rancher/v1.6/en/hosts/#supported-docker-versions). (Ubuntu, RHEL/CentOS 7 are more heavily tested.) Rancher also works with [RancherOS](https://github.com/rancher/os).
* RAM: 1GB+

### Launching Management Server

    docker run -d --restart=unless-stopped -p 8080:8080 rancher/server

The UI and API are available on the exposed port `8080`.

### Using Rancher

To learn more about using Rancher, please refer to our [Rancher Documentation](http://docs.rancher.com/).

## Source Code

This repo is a meta-repo used for packaging.  The source code for Rancher is in other repos in the rancher organization.  The majority of the code is in https://github.com/rancher/cattle.

## Support, Discussion, and Community
If you need any help with Rancher or RancherOS, please join us at either our [Rancher forums](http://forums.rancher.com/), [#rancher IRC channel](http://webchat.freenode.net/?channels=rancher) or [Slack](https://slack.rancher.io/) where most of our team hangs out at.

Please submit any **Rancher** bugs, issues, and feature requests to [rancher/rancher](//github.com/rancher/rancher/issues). 

Please submit any **RancherOS** bugs, issues, and feature requests to [rancher/os](//github.com/rancher/os/issues).

For security issues, please email security@rancher.com instead of posting a public issue in GitHub.  You may (but are not required to) use the GPG key located on [Keybase](https://keybase.io/rancher).

# License

Copyright (c) 2014-2016 [Rancher Labs, Inc.](http://rancher.com), portions Copyright © 2017 [Rancher Labs, Inc.](http://rancher.com) and HNA Ecological Technology Group Co., Ltd. See [copyright details.](COPYRIGHT_DETAILS.md)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
