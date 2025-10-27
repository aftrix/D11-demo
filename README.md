# Local DDEV Setup Guide (Mac)
We'll use OrbStack since it's the simplest of several options. OrbStack is not free for professional use, but several other options are open-source and free to use.

## Install OrbStack Docker Provider

With Homebrew installed, you can install OrbStack with one command:
```console
→ brew install orbstack docker
```
Launch OrbStack, accept the license agreement.
Confirm that you now have a Docker provider:
```console
→ docker version
```
## Install DDEV
```console
→ brew install ddev/ddev/ddev
```
Confirm that DDEV is installed:
```console
→ ddev -v
ddev version v1.24.8
```
## Run `mkcert -install`
Running `mkcert -install` is a one-time operation. It allows your browser to trust the HTTPS/TLS certificates served by DDEV.
```console
→ mkcert -install
```
## Start DDEV
```console
→ ddev start
```
## Install Drupal Setup
Run composer install:
```console
→ ddev composer install
```
## Default Admin User

User: `ddevadmin`

Pass: `DDEV_Admin_Pass`

# Launch Site
```console
→ ddev launch
# or automatically login with:
→ ddev launch $(ddev drush uli)
```
## Users

|                |Username                          |Password                         |
|----------------|-------------------------------|-----------------------------|
|Default|`ddevadmin`            |`DDEV_Admin_Pass`            |
