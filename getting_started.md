---
layout: page
title: Getting Started
---
Getting started has two parts:

1. [Install Vagrant](https://www.vagrantup.com/downloads.html). To quote the
   Vagrant docs, "Installing Vagrant is extremely easy."

2. Download the SELinux Game Vagrant File which defines all of the Vagrant
   boxes.

   ```
   wget {{ site.baseurl }}{% link Vagrantfile %}
   ```

3. From the same Directory as `Vagrantfile`, run `vagrant status` which should
   display output listing the scenarios similar to:

   ```
   [user@localhost vagrant_test]$ vagrant status
   Current machine states:

   broken_antivirus          not created (libvirt)
   fresh_pulp                not created (libvirt)
   new_ways                  not created (libvirt)
   stayin_alive              not created (libvirt)

   This environment represents multiple VMs. The VMs are all listed
   above with their current state. For more information about a
   specific VM, run `vagrant status NAME`.
   ```

4. Play a [Scenario]({{ site.baseurl }}{% link scenarios.md %}).

If your `vagrant status` does not offer a scenario listed here, your
Vagrantfile is out of date. Update your Vagrantfile as done in step 2, which
can be done safely at any time.
