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

3. From the same Directory as `Vagrantfile`, run `vagrant up` which should
   display output like the following:

   ```
   [user@localhost vagrant_test]$ vagrant status
   Current machine states:

   broken_antivirus          not created (libvirt)
   fresh_pulp                not created (libvirt)
   new_ways                  not created (libvirt)
   stayin_alive              not created (libvirt)

   This environment represents multiple VMs. The VMs are all listed
   above with their current state. For more information about a specific VM, run `vagrant status NAME`.

   ```

4. Play a [Scenario]({{ site.baseurl }}{% link scenarios.md %}).


<p class="message">
  If you expect to see a scenario in your environment but don't, your
  Vagrantfile is likely out of date. You can replace your local Vagrantfile
  with the one from step 2 safely at any time.
</p>
