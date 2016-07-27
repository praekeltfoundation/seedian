# Seedian

Seedian is a Debian build which includes useful things for running Docker and
Mesos properly without having to give up having a useful userland.

This repo is a FAI config (and some related utilities) for generating Seedian
installations.


## Usage

Clone this repo to `/srv/fai` on a Debian machine with the `fai-server` package
installed.

Copy or symlink `/srv/fai/etc_fai` to `/etc/fai` so `fai` uses the configs from
the repo.

Create the nfsroot:
```
fai-setup -v
```
(See http://fai-project.org/fai-guide/#_create_the_nfsroot for more details.)

Create the partial repo mirror to put on the ISO:
```
fai-mirror -v -P /srv/fai/config/files/etc/apt/preferences/SEEDIAN -c FAIBASE,DEBIAN,SEEDIAN /srv/fai/fai_mirror
```

TODO: The hackery required to make an ISO the XenServer will grudgingly accept.


## Credits

Most of the configs in this repo started out as the FAI example configs. These
retain their original copyrights, etc.
