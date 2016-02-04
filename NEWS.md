# Release notes

## 0.2.0

Improvements:

 - mesos-agent: Support CentOS 6.5 with docker containerizer.
 - Add support for Mesos agent and framework authentication.
 - Enable HTTP authentication for Marathon and Chronos.

Fixes:

 - mesos-dns: Remove `netinfo` from `IPSources` to fix Docker tasks becoming
   unreachable.
 - mesos-agent: Store logs in `/var/log/mesos` and state files in `/mnt/mesos`
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