# Ansible Role: NGINX Proxy

[![Build Status](https://travis-ci.com/KrautIT/ansible-role-nginx-proxy.svg?branch=master)](https://travis-ci.com/KrautIT/ansible-role-nginx-proxy)

This [Ansible](https://www.ansible.com/) role will set up an [NGINX](https://www.nginx.com/) proxy via [Docker Compose](https://docs.docker.com/compose/):

* Set up and launch [jwilder/nginx-proxy](https://github.com/jwilder/nginx-proxy):alpine
* Set up and launch [jrcs/letsencrypt-nginx-proxy-companion](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion):stable

## Parameters

See [defaults/main.yml](defaults/main.yml)

## Platforms

This role should work on most [Debian](https://www.debian.org/) and [Red Hat](https://www.redhat.com/) based Linux distributions.

Currently supported and tested Linux distributions:

* [CentOS](https://www.centos.org/) 7
* [Ubuntu](https://www.ubuntu.com/) 18.04

## Testing

Local testing can be done using [Docker](https://www.docker.com/), [InSpec](https://www.inspec.io/) and [Kitchen](https://kitchen.ci/).

See [requirements.yml](requirements.yml) for additional roles required for local testing.

```bash
bundle install
bundle exec kitchen test
```
## Notes

- By default, containers are run in ``the default `bridge````` network. You can customize this through `nginx_proxy_network`
