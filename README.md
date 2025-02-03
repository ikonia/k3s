# Puppet module for deploying k3s/kubernetes

[![License](https://img.shields.io/github/license/voxpupuli/puppet-k8s.svg)](https://github.com/voxpupuli/puppet-k8s/blob/master/LICENSE)

## Table of Contents

- [Description](#description)
- [Usage](#usage)
- [Examples](#examples)
- [Reference](#reference)

## Description

This module is very early development concept that installs, configures, and manages a K3s Kubernetes cluster built from
loose components, it's based from the Vopupuli K8 module as best practice for layout and actions in puppet NOT FOR PRODUCTION USE

Anyone is free to input this module is aspiring to solve the problem of K3 installs being a 'curl' command to an untrusted shell script


## Usage

DO NOT USE YET - PROBABLY DOESN'T WORK, LET ALONE STABLE


```puppet
class { 'k3s':
  role               => 'server',
  control_plane_url  => 'https://kubernetes.example.com:6443',
# generate_ca        => true, # Only set true temporarily to avoid overwriting the old secrets
# puppetdb_discovery => true, # Will use PuppetDB PQL queries to manage etcd and nodes
}
```

### Examples

For more in-detail examples see the examples.

- [Simple bridged setup](examples/simple_setup/Readme.md)
- [Cilium setup](examples/cilium/Readme.md)

## Reference

All parameters are documented within the classes. Markdown documentation is available in the [REFERENCE.md](REFERENCE.md) file, it also contains examples.
