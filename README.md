# ansible-role-vagrant-go-dev [![Build Status][travis.svg]][travis]

An Ansible role for a Vagrant-based Go development setup.

Available on Ansible Galaxy at [`naftulikay.vagrant-go-dev`][galaxy].

## Requirements

A Vagrant machine which is an operating system/architecture supported by Go, which should almost always apply.

## Role Variables

<dl>
  <dt><code>vagrant_user</code></dt>
  <dd>The username of the Vagrant user, defaults to <code>vagrant</code></dd>
  <dt><code>go_package</code></dt>
  <dd>The full Go package name for your project, e.g. <code>github.com/naftulikay/go-test</code>.</dd>M
</dl>

> Please see the upstream [`naftulikay.vagrant-base`][vagrant-base] and [`naftulikay.go-dev`][go-dev] roles for
additional supported variables.

## Dependencies

 - [`naftulikay.vagrant-base`][vagrant-base]: Provides base Vagrant configuration.
 - [`naftulikay.go-dev`][go-dev]: Provides a basic Go development environment.

## Example Playbook

Install a Go development environment within the Vagrant machine:

```
---
- hosts: all
  roles:
    - role: vagrant-go-dev
      go_package: github.com/naftulikay/ansible-role-vagrant-go-dev
```

## LICENSE

MIT.

 [travis]: https://travis-ci.org/naftulikay/ansible-role-vagrant-go-dev
 [travis.svg]: https://travis-ci.org/naftulikay/ansible-role-vagrant-go-dev.svg?branch=master
 [galaxy]: https://galaxy.ansible.com/naftulikay/vagrant-go-dev/
 [vagrant-base]: https://galaxy.ansible.com/naftulikay/vagrant-base/
 [go-dev]: https://galaxy.ansible.com/naftulikay/go-dev/
