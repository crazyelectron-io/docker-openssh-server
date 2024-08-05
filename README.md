# Kubernetes sidecar OpenSSH server

Based on the [LinuxServer.io](https://linuxserver.io) image [docker-openssh-server](xxx) which uses Alpine Linux.

I needed this for VSCode remote SSH to access Longhorn volmes in Kubernetes. The Linuxserver.io version uses Alpine Linux that does not support `libc`. VSCode Remote SSH happens to need that, so I adapted it to use the Ubuntu image.Also added a TCP forwarding option which is also needed for VSCode.

This version only supports amd64 architecture. 

## Application Setup

All parameters and configuration documented in the original version are applicable to this for.
One parameters was added: `TCP_FORWARDING` which can be `true` or `false` (default is `false`) to enable or disable SSH TCP forwarding for VSCode Remote SSH support.

## Versions

* **04.08.2024:** - Initial Release.
