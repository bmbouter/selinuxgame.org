---
number: 1
title: Enable/Disable/Status
description: Learn how enable, disable, and check the status of SELinux
attribution_url: https://selinuxproject.org/page/NewUsers
next_tutorials: ['file_contexts']
---

<p style="padding-top:30px">
  <h2>Is SELinux Installed?</h2>
</p>

The following Operating Systems include SELinux by default

* Red Hat Enterprise Linux 4+
* Fedora 2+
* Hardened Ubuntu
* Hardened Gentoo

It is also available for Debian as an add-on.

<p style="padding-top:30px">
  <h2>How do I know if SELinux is on?</h2>
</p>

If you use Red Hat Enterprise Linux or Fedora it is enabled by default. To see
whether it is actively enforcing the policy you can run `getenforce`:

```
[root@localhost ~]# getenforce
Enforcing
```

If it says Enforcing (as above) your system is being protected by SELinux. If
it says permissive SELinux is enabled but is only logging failed accesses, not
denying them. If it says Disabled then SELinux is not enabled on your system. 

<p style="padding-top:30px">
  <h2>Tools</h2>
</p>

* [`getenforce`](https://linux.die.net/man/8/getenforce) will show if SELinux
is Enforcing, Permissive, or Disabled.

* [`setenforce`](https://linux.die.net/man/8/setenforce) modifies if SELinux
is running or not.
