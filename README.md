# Caddy Docker Custom Builds
[![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/serfriz/caddy-custom-builds?label=Release)](https://github.com/serfriz/caddy-custom-builds/releases)
[![GitHub build status](https://img.shields.io/github/actions/workflow/status/serfriz/caddy-custom-builds/update-tag-release.yml?label=Auto-update)](https://github.com/serfriz/caddy-custom-builds/actions/workflows/update-tag-release.yml)
[![License](https://img.shields.io/github/license/serfriz/caddy-custom-builds?label=License)](https://github.com/serfriz/caddy-custom-builds/blob/main/LICENSE)

[Caddy](https://github.com/caddyserver/caddy) takes a [modular approach](https://caddyserver.com/docs/extending-caddy) to building Docker images, allowing users to include only the [modules](https://caddyserver.com/docs/modules/) they need. This repository aims to provide flexibility and convenience to run Caddy with specific combinations of modules by providing pre-built images according to the needs and preferences of the users.

All custom images are updated automatically when a [new version](https://github.com/caddyserver/caddy/releases) of Caddy is released using the official [Caddy Docker](https://hub.docker.com/_/caddy) image. This is done by using GitHub Actions to build and push the images for all Caddy supported platforms to Docker Hub, GitHub Packages and Quay container registries.

All commits and tags are signed with a GPG key to ensure their integrity and authenticity, and 2FA is enabled in the accounts involved in the management of this repository and the container registries.

## Builds

If you are looking for a specific custom build not available yet in this repository, please open a new [Issue](https://github.com/serfriz/caddy-custom-builds/issues) with your request. To make sure no broken or unsafe builds are created, the requested modules should be properly maintained and listed in the Caddy's [download page](https://caddyserver.com/download). Additional information and instructions can be found by clicking on the name of the Caddy images and modules listed below.

### Caddy Images:

- [**caddy-cloudflare**](https://github.com/serfriz/caddy-custom-builds/tree/main/caddy-cloudflare): includes Cloudflare DNS and IPs modules.
- [**caddy-cloudflare-crowdsec**](https://github.com/serfriz/caddy-custom-builds/tree/main/caddy-cloudflare-crowdsec): includes Cloudflare DNS/IPs and CrowdSec Bouncer modules.
- [**caddy-cloudflare-ddns**](https://github.com/serfriz/caddy-custom-builds/tree/main/caddy-cloudflare-ddns): includes Cloudflare Dynamic DNS and IPs modules.
- [**caddy-cloudflare-ddns-crowdsec**](https://github.com/serfriz/caddy-custom-builds/tree/main/caddy-cloudflare-ddns-crowdsec): includes Cloudflare Dynamic DNS/IPs and CrowdSec Bouncer modules.
- [**caddy-cloudflare-ddns-security**](https://github.com/serfriz/caddy-custom-builds/tree/main/caddy-cloudflare-ddns-security): includes Cloudflare Dynamic DNS/IPs and Caddy Security modules.
- [**caddy-crowdsec**](https://github.com/serfriz/caddy-custom-builds/tree/main/caddy-crowdsec): includes CrowdSec Bouncer module.
- [**caddy-duckdns**](https://github.com/serfriz/caddy-custom-builds/tree/main/caddy-duckdns): includes DuckDNS DNS module.
- [**caddy-duckdns-crowdsec**](https://github.com/serfriz/caddy-custom-builds/tree/main/caddy-duckdns-crowdsec): includes DuckDNS DNS and CrowdSec Bouncer modules.
- [**caddy-duckdns-ddns**](https://github.com/serfriz/caddy-custom-builds/tree/main/caddy-duckdns-ddns): includes DuckDNS Dynamic DNS module.
- [**caddy-duckdns-ddns-crowdsec**](https://github.com/serfriz/caddy-custom-builds/tree/main/caddy-duckdns-ddns-crowdsec): includes DuckDNS Dynamic DNS and CrowdSec Bouncer modules.
- [**caddy-ratelimit-dockerproxy-sablier**](https://github.com/serfriz/caddy-custom-builds/tree/main/caddy-ratelimit-dockerproxy-sablier): includes Rate Limit, Docker Proxy and Sablier modules.

### Modules:

- [**Cloudflare DNS**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#dns-modules): for Cloudflare DNS-01 ACME validation support | [caddy-dns/cloudflare](https://github.com/caddy-dns/cloudflare)
- [**Cloudflare IPs**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#cloudflare-ips): to retrieve Cloudflare's current [IP ranges](https://www.cloudflare.com/ips/) | [WeidiDeng/caddy-cloudflare-ip](https://github.com/WeidiDeng/caddy-cloudflare-ip)
- [**DuckDNS**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#dns-modules): for DuckDNS DNS-01 ACME validation support | [caddy-dns/duckdns](https://github.com/caddy-dns/duckdns)
- [**Dynamic DNS**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#dynamic-dns): updates the DNS records with the public IP address of your instance | [mholt/caddy-dynamicdns](https://caddyserver.com/docs/modules/dynamic_dns)
- [**CrowdSec Bouncer**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#crowdsec-bouncer): to blocks malicious traffic based on [CrowdSec](https://www.crowdsec.net/) decisions | [hslatman/caddy-crowdsec-bouncer](https://github.com/hslatman/caddy-crowdsec-bouncer)
- [**Rate Limit**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#rate-limit): implements both internal and distributed HTTP rate limiting | [mholt/caddy-ratelimit](https://github.com/mholt/caddy-ratelimit)
- [**Caddy Security**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#caddy-security): to add different authentication methods including MFA/2FA support | [greenpau/caddy-security](https://github.com/greenpau/caddy-security)
- [**Docker Proxy**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#docker-proxy): enables Caddy to be used for Docker containers via labels | [lucaslorentz/caddy-docker-proxy](https://github.com/lucaslorentz/caddy-docker-proxy)
- [**Sablier**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#sablier): to start your containers on demand and shut them down automatically | [acouvreur/sablier](https://github.com/acouvreur/sablier)
- [**GeoIP Filter:**](https://github.com/serfriz/caddy-custom-builds?tab=readme-ov-file#geoip-filter) to allow or block traffic from specific regions based on [Maxmind GeoLite2 database](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) | [porech/caddy-maxmind-geolocation](https://github.com/porech/caddy-maxmind-geolocation)

## Usage

Since all images from this repository are built off the official Caddy Docker image, the same [volumes](https://docs.docker.com/storage/volumes/) and/or [bind mounts](https://docs.docker.com/storage/bind-mounts/), ports mapping, environment variables, etc. can be used with this container. Please refer to the official [Caddy Docker](https://hub.docker.com/_/caddy) image and [docs](https://caddyserver.com/docs/) for more information on using Caddy.

Docker builds for all Caddy supported platforms are available at the following container registries:
- **Docker Hub** > `docker pull serfriz/<caddy-build-name>:latest`
- **GitHub Packages** > `docker pull ghcr.io/serfriz/<caddy-build-name>:latest`
- **Quay** > `docker pull quay.io/serfriz/<caddy-build-name>:latest`

To pull a specific build, replace `<caddy-build-name>` with the desired one. For example, to pull the `caddy-cloudflare` build from Docker Hub, use `docker pull serfriz/caddy-cloudflare:latest`.

### Tags

The following tags are available for all images:

- `latest`
- `<version>` (eg: `2.7.4`, including: `2.7`, `2`, etc.)

### Container Creation

Simply create the container using the `docker run` command, or a `docker-compose.yml` file including the necessary [environment variables](https://caddyserver.com/docs/caddyfile/concepts#environment-variables) depending on the modules used. The following blocks contain examples for both methods using `<caddy-build-name>` as the image name (replace it with the desired Caddy build name), and including all environment variables required by the modules listed above (some may not apply to your specific build).

#### Docker Run

```sh
docker run --rm -it \
  --name caddy \  # feel free to choose your own container name
  --restart unless-stopped \  # run container unless stopped by user (optional)
  -p 80:80 \  # HTTP port
  -p 443:443 \  # HTTPS port
  -p 443:443/udp \  # HTTP/3 port (optional)
  -v caddy-data:/data \  # volume mount for certificates data
  -v caddy-config:/config \  # volume mount for configuration data
  -v $PWD/Caddyfile:/etc/caddy/Caddyfile \  # to use your own Caddyfile
  -v $PWD/log:/var/log \  # bind mount for the log directory (optional)
  -v $PWD/srv:/srv \  # bind mount to serve static sites or files (optional)
  -e CLOUDFLARE_API_TOKEN=<token-value> \  # Cloudflare API token (if applicable)
  -e DUCKDNS_API_TOKEN=<token-value> \  # DuckDNS API token (if applicable)
  -e CROWDSEC_API_KEY=<key-value> \  # CrowdSec API key (if applicable)
  serfriz/<caddy-build-name>:latest  # replace with the desired Caddy build name
```

The volume and bind mounts can be adjusted to meet to your needs, `$PWD` is used to reference the current working directory, but you can replace it with your preferred path. The environment variables are only required if the modules used in the build require them.

The default [Caddyfile](https://github.com/caddyserver/dist/blob/master/config/Caddyfile) that is included inside the Docker container is just a placeholder to serve a static Caddy welcome page with some useful instructions. So you will most likely want to mount your own `$PWD/Caddyfile` to configure Caddy according to your needs (the file must already exist in the specified path before creating the container).

The [restart policy](https://docs.docker.com/config/containers/start-containers-automatically/#use-a-restart-policy) can be adjusted to your needs. The policy `unless-stopped` ensures the container is always running (even at boot) unless it is explicitly stopped by the user.

#### Docker Compose

```yaml
version: "3.7"
services:
  caddy:
    image: serfriz/<caddy-build-name>:latest  # replace with the desired Caddy build name
    container_name: caddy  # feel free to choose your own container name
    restart: "unless-stopped"  # run container unless stopped by user (optional) 
    ports:
      - "80:80"  # HTTP port
      - "443:443"  # HTTPS port
      - "443:443/udp"  # HTTP/3 port (optional)
    volumes:
      - caddy-data:/data  # volume mount for certificates data
      - caddy-config:/config  # volume mount for configuration data
      - $PWD/Caddyfile:/etc/caddy/Caddyfile  # to use your own Caddyfile
      - $PWD/log:/var/log  # bind mount for the log directory (optional)
      - $PWD/srv:/srv \  # bind mount to serve static sites or files (optional)
    environment:
      - CLOUDFLARE_API_TOKEN=<token-value>  # Cloudflare API token (if applicable)
      - DUCKDNS_API_TOKEN=<token-value>  # DuckDNS API token (if applicable)
      - CROWDSEC_API_KEY=<key-value>  # CrowdSec API key (if applicable)
volumes:
  caddy-data:
    external: true
  caddy-config:
```

Defining the data volume as [external](https://docs.docker.com/compose/compose-file/compose-file-v3/#external) makes sure `docker-compose down` does not delete the volume, but you may need to create it first using `docker volume create caddy-data`. This doesn't apply to bind mounts if you opt to use them instead of volumes.

### Graceful Reloads

Caddy does not require a full restart when the Caddyfile is modified. Caddy comes with a [caddy reload](https://caddyserver.com/docs/command-line#caddy-reload) command which can be used to reload its configuration with zero downtime.

When running Caddy in Docker, the recommended way to trigger a config reload is by executing the `caddy reload` command in the running container. First, you'll need to determine your container ID or name. Then, pass the container ID to docker exec. The working directory is set to /etc/caddy so Caddy can find your Caddyfile without additional arguments.

```sh
caddy_container_id=$(docker ps | grep caddy | awk '{print $1;}')  # use your container name if different from 'caddy'
docker exec -w /etc/caddy $caddy_container_id caddy reload
```

It is possible to create an [alias](https://phoenixnap.com/kb/linux-alias-command) for the `caddy reload` command to make it more convenient to use by adding the following line to your `~/.bashrc` or `~/.zshrc` file:
    
```sh
alias caddy-reload="docker exec -w /etc/caddy $(docker ps | grep caddy | awk '{print $1;}') caddy reload"
```

Once you have added the alias to the appropriate file, you will need to source it for the changes to take effect. You can do this by running `source ~/.bashrc` or `source ~/.zshrc` in your terminal. After this, you will be able to use the `caddy-reload` alias in your terminal sessions.

## Configuration

This section aims to provide some basic information on how to configure Caddy with the modules included in the custom builds, but it is not intended to be a comprehensive guide. All the examples are based on the official [Caddyfile](https://caddyserver.com/docs/caddyfile) syntax and the modules' documentation.

### DNS Modules

To make use of the different modules that provide DNS-01 ACME validation support at the server level, set the global [acme_dns](https://caddyserver.com/docs/caddyfile/options#acme-dns) directive in your `Caddyfile` using your DNS provider's name and the respective environment variable for the API token. The example shows the use case for Cloudflare DNS with the rest of the DNS providers commented out.

```Caddyfile
{
  acme_dns cloudflare {env.CLOUDFLARE_API_TOKEN} #  for Cloudflare
  # acme_dns duckdns {env.DUCKDNS_API_TOKEN} #  for DuckDNS
}
```

Alternatively, you can use the [`tls`](https://caddyserver.com/docs/caddyfile/directives/tls#tls) directive at each site. See the [caddy-dns/cloudflare](https://github.com/caddy-dns/cloudflare) module for additional details.

```Caddyfile
my.domain.tld {
  tls {
    dns cloudflare {env.CLOUDFLARE_API_TOKEN}  #  for Cloudflare
    # dns duckdns {env.DUCKDNS_API_TOKEN}  #  for DuckDNS
  }
}
```

#### Creating a Cloudflare API Token

You can generate a Cloudflare API token via the Cloudflare web dashboard through the following steps:

1. Login to your Cloudflare [Dashboard](https://dash.cloudflare.com/)
2. Go to [Account Profile](https://dash.cloudflare.com/profile) > [API Tokens](https://dash.cloudflare.com/profile/api-tokens)
3. Click "Create token" (Use the "Create Custom Token" option)
4. Grant the following permissions:
   - `Zone > Zone > Read`
   - `Zone > DNS > Edit`
5. Copy the token and use it as the `CLOUDFLARE_API_TOKEN` environment variable.

#### Creating a DuckDNS API Token

To generate a DuckDNS API token, login to your [DuckDNS](https://www.duckdns.org/) account, copy the token, and use it as the `DUCKDNS_API_TOKEN` environment variable. You can recreate the token by clicking on the three vertical lines in the top right corner next to your logged in email, and selecting the recreate token option.

### Cloudflare IPs

To restrict access to your server only to Cloudflare's IP ranges, add the [trusted_proxies](https://caddyserver.com/docs/caddyfile/options#trusted-proxies) directive to the [global options](https://caddyserver.com/docs/caddyfile/options), under servers, in your `Caddyfile`. For additional details, refer to [trusted_proxies/cloudflare](https://caddyserver.com/docs/json/apps/http/servers/trusted_proxies/cloudflare/) documentation and [WeidiDeng/caddy-cloudflare-ip](https://github.com/WeidiDeng/caddy-cloudflare-ip) repository.

```Caddyfile
{
  servers {
    trusted_proxies cloudflare {
      interval 12h
      timeout 15s
    }
  }
}
```

### Dynamic DNS

To keep your DNS records updated with the public IP address of your instance, add the [dynamic_dns](https://caddyserver.com/docs/modules/dynamic_dns) directive to the [global options](https://caddyserver.com/docs/caddyfile/options) in your `Caddyfile`. This module regularly queries a service for your public IP address and updates the DNS records via your DNS provider's API whenever it changes. For additional details and advanced configuration examples refer to [mholt/caddy-dynamicdns](https://github.com/mholt/caddy-dynamicdns) repository. The example shows the use case for Cloudflare DNS with the rest of the DNS providers commented out.

```Caddyfile
{
  dynamic_dns {
    provider cloudflare {env.CLOUDFLARE_API_TOKEN}  # for Cloudflare
    # provider duckdns {env.DUCKDNS_API_TOKEN}  # for DuckDNS
    domains {
      domain.tld
    }
  }
}
```

Using the option [dynamic_domains](https://github.com/mholt/caddy-dynamicdns#dynamic-domains), it can also be configured to scan through the domains configured in the Caddyfile and try to manage those DNS records.

### CrowdSec Bouncer

[CrowdSec](https://www.crowdsec.net/) is a free and open source security automation tool that uses local logs and a set of scenarios to infer malicious intent. In addition to operating locally, an optional community integration is also available, through which crowd-sourced IP reputation lists are distributed.

To make use of the CrowdSec Bouncer module, set the global [crowdsec](https://caddyserver.com/docs/modules/crowdsec) directive in your `Caddyfile`, and include it in every site you want to protect. For advanced usage, refer to the [hslatman/caddy-crowdsec-bouncer](https://github.com/hslatman/caddy-crowdsec-bouncer) repository.

```Caddyfile
{
  debug  # makes Caddy logs more detailed (optional)
  order crowdsec first  # forces the CrowdSec directive to be executed first
  crowdsec {
    api_url http://localhost:8080  # it should point to your CrowdSec API (it can be a remote URL)
    api_key {env.CROWDSEC_API_KEY}
  }
}

my.domain.tld {
  crowdsec
  log {
    output file /var/log/access.log  # the path should match the bind mount of the log directory
  }
}
```

#### Creating a CrowdSec API Key

To register the Caddy CrowdSec Bouncer to your API, you need to run the command below on the server where the CrowdSec API is installed, and use the generated API key `CROWDSEC_API_KEY` as environment variable when creating the Caddy container.

```sh
sudo cscli bouncers add caddy-bouncer
```

For additional details, refer to the [CrowdSec documentation](https://www.crowdsec.net/blog/introduction-to-the-local-api).

### Rate Limit

The [rate_limit](https://caddyserver.com/docs/modules/http.handlers.rate_limit#github.com/mholt/caddy-ratelimit) HTTP handler module lets you define rate limit zones, which have a unique name of your choosing. If a rate limit is exceeded, an HTTP error with status 429 will be returned. This error can be handled using the conventional error handling routes in your config.

Additional information and Caddyfile configuration examples can be found in the [mholt/caddy-ratelimit](https://github.com/mholt/caddy-ratelimit) repository.

### Caddy Security

This plugin implements different authentication methods: Form-Based, Basic, Local, LDAP, OpenID Connect, OAuth 2.0, SAML, including MFA/2FA with App Authenticators and Yubico (formerly `caddy-auth-portal`). It is also an authorization plugin for HTTP request authorization based on JWT/PASETO tokens (formerly `caddy-authorize`, `caddy-auth-jwt`), and manages credentials for various integrations.

Please, refer to the official [greenpau/caddy-security](https://authp.github.io/) documentation for additional details. Some configuration examples can also be found in the [authp/authp.github.io](https://github.com/authp/authp.github.io/tree/main/assets/conf) repository.

### Docker Proxy

The plugin scans Docker metadata, looking for labels indicating that the service or container should be served by Caddy. Then, it generates an in-memory Caddyfile with site entries and proxies pointing to each Docker service by their DNS name or container IP. Every time a Docker object changes, the plugin updates the Caddyfile and triggers Caddy to gracefully reload with zero downtime.

Additional information and Caddyfile configuration examples can be found in the [lucaslorentz/caddy-docker-proxy](https://github.com/lucaslorentz/caddy-docker-proxy) repository.

### Sablier

[Sablier](https://github.com/acouvreur/sablier) is a free and open-source software that can scale your workloads on demand following different strategies. Your workloads can be a docker container, a kubernetes deployment and more (see [providers](https://acouvreur.github.io/sablier/#/providers/overview) for the full list). This plugin provides an integration with Caddy.

Additional information and Caddyfile configuration examples can be found in the [acouvreur/sablier](https://acouvreur.github.io/sablier/#/plugins/caddy) documentation.

### GeoIP Filter

Allows Caddy to filter traffic based on the client's IP address location. This module needs access to the Maxmind GeoLite2 database which can be downloaded for free after creating an account. Additional information is available on [Maxmind official website](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data). You will specifically need the GeoLite2-Country.mmdb file, or the GeoLite2-City.mmdb if you're matching on subdivisions and metro codes.

Information and examples about the usage of this module can be found on the on the [Caddy website's plugin page](https://caddyserver.com/docs/modules/http.matchers.maxmind_geolocation) and the [porech/caddy-maxmind-geolocation](https://github.com/porech/caddy-maxmind-geolocation) repository.

## Contributing

Feel free to contribute, request additional Caddy images with your preferred modules, and make things better by opening an [Issue](https://github.com/serfriz/caddy-custom-builds/issues) or [Pull Request](https://github.com/serfriz/caddy-custom-builds/pulls).

## License

Software under [GPL-3.0](https://github.com/serfriz/caddy-custom-builds/blob/main/LICENSE) ensures users' freedom to use, modify, and distribute it while keeping the source code accessible. It promotes transparency, collaboration, and knowledge sharing. Users agree to comply with the GPL-3.0 license terms and provide the same freedom to others.