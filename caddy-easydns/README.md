# Caddy Docker build with EasyDNS DNS module

[![Docker Hub](https://img.shields.io/badge/Docker%20Hub%20-%20advisorgee%2Fcaddy--EasyDNS%20-%20%230db7ed?style=flat&logo=docker)](https://hub.docker.com/r/advisorgee/caddy-EasyDNS)
[![GitHub](https://img.shields.io/badge/GitHub%20-%20advisorgee%2Fcaddy--EasyDNS%20-%20%23333?style=flat&logo=github)](https://ghcr.io/advisorgee/caddy-EasyDNS)


[![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/advisorgee/caddy-custom-easydns?label=Release)](https://github.com/advisorgee/caddy-custom-easydns/releases)
[![GitHub build status](https://img.shields.io/github/actions/workflow/status/advisorgee/caddy-custom-easydns/build.caddy-EasyDNS.yml?label=Build)](https://github.com/advisorgee/caddy-custom-easydns/actions/workflows/build.caddy-EasyDNS.yml)

This image is updated automatically by GitHub Actions when a new version of [Caddy](https://github.com/caddyserver/caddy) is released using the official [Caddy Docker](https://hub.docker.com/_/caddy) image and the following module:
- [**EasyDNS**](https://github.com/advisorgee/caddy-custom-easydns?tab=readme-ov-file#dns-modules): for EasyDNS DNS-01 ACME validation support | [anxuanzi/caddy-dns-EasyDNS](https://github.com/anxuanzi/caddy-dns-EasyDNS)

## Usage

Since this image built off the official Caddy Docker image, the same [volumes](https://docs.docker.com/storage/volumes/) and/or [bind mounts](https://docs.docker.com/storage/bind-mounts/), ports mapping, etc. can be used with this container. Additional [environment variables](https://caddyserver.com/docs/caddyfile/concepts#environment-variables) may be needed for the added module. Please, refer to the repository's [README](https://github.com/advisorgee/caddy-custom-easydns?tab=readme-ov-file#container-creation) file for further usage instructions.

Docker builds for all Caddy supported platforms available at the following container registries:
- [**Docker Hub**](https://hub.docker.com/r/advisorgee/caddy-EasyDNS) `docker pull advisorgee/caddy-EasyDNS:latest`
- [**GitHub Packages**](https://ghcr.io/advisorgee/caddy-EasyDNS) `docker pull ghcr.io/advisorgee/caddy-EasyDNS:latest`


### Tags

The following tags are available for the `advisorgee/caddy-EasyDNS` image:

- `latest`
- `<version>` (eg: `2.7.4`, including: `2.7`, `2`, etc.)


## License

Software under [GPL-3.0](https://github.com/advisorgee/caddy-custom-easydns/blob/main/LICENSE) ensures users' freedom to use, modify, and distribute it while keeping the source code accessible. It promotes transparency, collaboration, and knowledge sharing. Users agree to comply with the GPL-3.0 license terms and provide the same freedom to others.