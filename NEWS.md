# Release notes

## 0.4.0

Improvements:

 - mesos-master, mesos-slave: Use fully qualified host names.
 - Generate Ansible role documentation from YAML files so they are always up to
   date.
 - marathon-lb: Upgrade to version 1.1.1.
 - common: Disable IPv6 on all cluster nodes.
 - New glusterfs role which adds persistent storage across nodes.

## 0.3.0

Improvements:

 - common: Add fully qualified domain name in `/etc/hosts`.
 - mesos-dns: Make the resolver list configurable. Defaults to `8.8.8.8`.

Fixes:

 - zookeeper: Handle removal of nodes.
 - java, chronos-sync: CentOS support.

## 0.2.0

Improvements:

 - mesos-slave: Support CentOS 6.5 with docker containerizer.
 - Add support for Mesos agent and framework authentication.
 - Enable HTTP authentication for Marathon and Chronos.

Fixes:

 - mesos-dns: Remove `netinfo` from `IPSources` to fix Docker tasks becoming
   unreachable.
 - mesos-slave: Store logs in `/var/log/mesos` and state files in `/log/mesos`
   so they can be analyzed after rebooting a node.
 - docker-engine: Use APT repo key hosted on apt.dockerproject.org

## 0.1.0

First official release based on Mesos version 0.25.0.

The main features are:

 - Mesos master running Marathon 0.13.0 and Chronos 2.4.0
 - Mesos agent with Docker containerizer and cgroups isolation enabled
 - Mesos DNS 0.5.1 for core service discovery
 - Marathon load balancer using HAProxy for SSL and proxying to internal
   applications
