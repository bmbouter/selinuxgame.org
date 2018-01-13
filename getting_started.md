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

{% for scenario in site.scenarios %}
   {{ scenario.slug }}
{% endfor %}

   This environment represents multiple VMs. The VMs are all listed
   above with their current state. For more information about a specific VM, run `vagrant status NAME`.

   ```

4. Play a [Scenario]({{ site.baseurl }}{% link scenarios.md %}).


<p class="message">
  If your `vagrant status` does not show all of the above scenarios, your
  Vagrantfile is out of date. You can update your local Vagrantfile with wget
  as done in step 2 safely at any time.
</p>
