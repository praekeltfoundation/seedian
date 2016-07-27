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

